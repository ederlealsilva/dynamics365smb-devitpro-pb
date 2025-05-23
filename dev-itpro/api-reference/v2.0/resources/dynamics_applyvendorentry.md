---
title: applyVendorEntry resource type  
description: An apply vendor entry object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 04/09/2024
ms.author: solsen
ms.reviewer: solsen
---

# applyVendorEntry resource type

Represents an apply vendor entry in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

> [!NOTE]
> For information about enabling APIs for [!INCLUDE[prod_short](../../../includes/prod_short.md)] see [Enabling the APIs for Dynamics 365 Business Central](../enabling-apis-for-dynamics-nav.md).

## Methods

| Method | Return Type|Description |
|:--------------------|:-----------|:-------------------------|
|[GET applyVendorEntry](../api/dynamics_applyvendorentry_get.md)|applyVendorEntry|Gets a apply vendor entry object.|
|[PATCH applyVendorEntry](../api/dynamics_applyvendorentry_update.md)|applyVendorEntry|Updates a apply vendor entry object.|

## Properties

| Property           | Type   |Description     |
|:-------------------|:-------|:---------------|
|id|GUID|The unique ID of the apply vendor entry. Non-editable.|
|applied|boolean|Specifies whether the apply vendor entry has been applied.|
|appliesToId|string|The ID of the vendor it applies to.|
|postingDate|date|The date that the apply vendor entry   is posted.|
|documentType|NAV.genJournalDocumentType|Specifies the document type of the apply vendor entry. It can be " ", "Payment", "Invoice", "Credit Memo", "Finance Charge Memo", "Reminder" or "Refund".|
|documentNumber|string|Specifies a document number for the apply vendor entry.|
|externalDocumentNumber|string|Specifies an external document number for the apply vendor entry.|
|vendorNumber|string|Specifies vendor's number.|
|vendorName|string|Specifies vendor's name.|
|description|string|Specifies the description of the apply vendor entry.|
|remainingAmount|decimal|The amount including VAT.|
|lastModifiedDateTime|datetime|The last datetime the apply vendor entry was modified. Read-Only.|

## JSON representation

Here's a JSON representation of the applyVendorEntry resource.


```json
{
    "id": "GUID",
    "applied": "boolean",
    "appliesToId": "string",
    "postingDate": "date",
    "documentType": "NAV.genJournalDocumentType",
    "documentNumber": "string",
    "externalDocumentNumber": "string",
    "vendorNumber": "string",
    "vendorName": "string",
    "description": "string",
    "remainingAmount": "decimal",
    "lastModifiedDateTime": "datetime"
}
```

## Remarks

This resource type requires [!INCLUDE[prod_short](../../../includes/prod_short.md)] version 18.0.

## Related information

[GET applyVendorEntry](../api/dynamics_applyvendorentry_get.md)  
[PATCH applyVendorEntry](../api/dynamics_applyvendorentry_update.md)  
