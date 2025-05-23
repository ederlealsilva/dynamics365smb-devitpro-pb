---
title: Creating FlowFields and FlowFilters
description: Examples of FlowFields and FlowFilters that are used to display the result of the calculation described in the CalcFormula property. 
author: SusanneWindfeldPedersen
ms.date: 06/20/2024
ms.topic: concept-article
ms.author: solsen
ms.reviewer: solsen
---

# Creating FlowFields and FlowFilters

This article describes the procedure and the properties used to create FlowFields and FlowFilters. 

A FlowField performs a set of calculations and displays the results immediately. A FlowFilter displays the results based on the user input to calculate the filtered values that affect the calculation of a FlowField. The FlowFields and FlowFilters aren't physical fields; these fields act as a virtual field, which doesn't actually exist in the database. They're a description of a calculation and a location for the result to be displayed which is typically derived in the [CalcFormula Property](properties/devenv-calcformula-property.md). 

For more information about the FlowField type, see [FlowFields overview](devenv-flowfields.md), and for more information about the FlowFilter type, see [FlowFilter Overview](devenv-flowfilter-overview.md).

<!--
### Example scenarios
A typical scenario for using a FlowField could be the Account Balance field in the General Ledger Account table that shows the balance of the account and calculates as the sum of the NetAmount fields for all General Journal entries in the account . A typical scenario for using a FlowFilter could be a date filter. 
-->

## Classifying the field type

In order to create FlowFields and FlowFilters, you must first classify the field type by using the FieldClass Property. For more information, see [FieldClass Property](properties/devenv-fieldclass-property.md). By classifying the field as a FlowField or a FlowFilter type, you enable the fields to act as a virtual field whose value can be dynamically derived based on the calculation formula. 

## Calculation formula

A FlowField type is always associated with a calculation formula that determines how the FlowField is calculated. Likewise, the FlowFilter type is associated with the calculation formula. To perform the calculations by using the FlowField and FlowFilter type, you must derive those fields in the calculation formula, which you classify in the table. You can choose from several methods of calculations including sum (total), average, maximum value, minimum value, record count, lookup, and more, by using the CalcFormula Property. For more information about the syntax and formulas, see [CalcFormula property](properties\devenv-calcformula-property.md). 
 
### Example

In the following example, `MyTable` sets the `Global Dimension 1 Filter` and `Global Dimension 2 Filter` fields whose values are based only on the dimension values included in the filter. Also, some of the following fields formulate the currency filter to one single currency because you don't store the filter value on the entries, hence you define the `Currency Filter` as a FlowFilter type.
`Total Amount`, `Amount upper bound`, `Amount lower bound`, `First Entry`, and `Customer Balance` are classified as a FlowField type and here you specify the calculations. These fields display the results immediately based on the filters that you apply in the user interface. 

```AL
table 50123 MyTable
{
    fields
    {
        field(1;MyField; Decimal)
        {
            Description = 'New field';
        }

        field(2;"No."; Code[20])
        {
            Description = 'Serial number of the service';
        }

        field(3;"Global Dimension 1 Filter"; Code[20])
        {
            FieldClass = FlowFilter;
        }

        field(4;"Global Dimension 2 Filter"; Code[20])
        {
            FieldClass = FlowFilter;
        }

        field(5;"Currency Filter"; Code[10])
        {
            FieldClass = FlowFilter;
        }

        field(6; "Total Amount"; Decimal)
        {
            FieldClass = FlowField;
            CalcFormula = Sum("Detailed Cust. Ledg. Entry"."Amount (LCY)"
            where ("Customer No."=Field("No."),
            "Initial Entry Global Dim. 1"=Field("Global Dimension 1 Filter"),
            "Initial Entry Global Dim. 2"=Field("Global Dimension 2 Filter"),
            "Currency Code"=Field("Currency Filter")
            ) );
        }

        field(7; "Amount upper bound"; Decimal)
        {
            FieldClass = FlowField;
            CalcFormula = max ("Detailed Cust. Ledg. Entry"."Amount (LCY)"
            where ("Customer No." = Field ("No."),
            "Initial Entry Global Dim. 1" = Field ("Global Dimension 1 Filter"),
            "Initial Entry Global Dim. 2" = Field ("Global Dimension 2 Filter"),
            "Currency Code" = Field ("Currency Filter")
            ));
        }

        field(8; "Amount lower bound"; Decimal)
        {
            FieldClass = FlowField;
            CalcFormula = min ("Detailed Cust. Ledg. Entry"."Amount (LCY)"
            where ("Customer No." = Field ("No."),
            "Initial Entry Global Dim. 1" = Field ("Global Dimension 1 Filter"),
            "Initial Entry Global Dim. 2" = Field ("Global Dimension 2 Filter"),
            "Currency Code" = Field ("Currency Filter")
            ));
        }

        field(9; "First entry"; Boolean)
        {
            CalcFormula = exist (Customer where (Payments = const (0),
                                                 "No." = field ("No.")));
            FieldClass = FlowField;
            Caption = 'Specifies whether it is the customer''s first entry';
        }

        field(10; "Customer Balance"; Decimal)
        {
            FieldClass = FlowField;
            CalcFormula = lookup (Customer.Balance where ("No." = field ("No.")));
        }
    }
}
```

## Related information

[FlowFields overview](devenv-flowfields.md)  
[FlowFilter overview](devenv-flowfilter-overview.md)  
[CalcFormula property](properties\devenv-calcformula-property.md)
