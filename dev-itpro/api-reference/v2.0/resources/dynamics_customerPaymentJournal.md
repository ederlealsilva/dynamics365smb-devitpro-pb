---
title: customerPaymentJournal resource type  
description: A customer payment journal object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 04/28/2025
ms.author: solsen
ms.reviewer: solsen
---

# customerPaymentJournal resource type

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Represents a customer payment journal in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

> [!NOTE]
> For information about enabling APIs for [!INCLUDE[prod_short](../../../includes/prod_short.md)] see [Enabling the APIs for Dynamics 365 Business Central](../enabling-apis-for-dynamics-nav.md).

## Methods

| Method | Return Type|Description |
|:--------------------|:-----------|:-------------------------|
|[GET customerPaymentJournal](../api/dynamics_customerpaymentjournal_get.md)|customerPaymentJournal|Gets a customer payment journal object.|
|[DELETE customerPaymentJournal](../api/dynamics_customerpaymentjournal_delete.md)|none|Deletes a customer payment journal object.|
|[POST customerPaymentJournal](../api/dynamics_customerpaymentjournal_create.md)|customerPaymentJournal|Creates a customer payment journal object.|
|[PATCH customerPaymentJournal](../api/dynamics_customerpaymentjournal_update.md)|customerPaymentJournal|Updates a customer payment journal object.|


## Navigation

| Navigation |Return Type| Description |
|:----------|:----------|:-----------------|
|[customerPayments](dynamics_customerpayment.md)|customerPayments |Gets the customerpayments of the customerPaymentJournal.|

## Properties

| Property           | Type   |Description     |
|:-------------------|:-------|:---------------|
|id|GUID|The unique ID of the customer payment journal. Non-editable.|
|code|string|The code of the customer payment journal.|
|displayName|string|Specifies the customer payment journal's name. This name will appear on all sales documents for the customer payment journal.|
|lastModifiedDateTime|datetime|The last datetime the customer payment journal was modified. Read-Only.|
|balancingAccountId|GUID|The balancing G/L Account ID.|
|balancingAccountNumber|string|The balancing G/L Account number.|

## JSON representation

Here's a JSON representation of the customerPaymentJournal resource.


```json
{
    "id": "GUID",
    "code": "string",
    "displayName": "string",
    "lastModifiedDateTime": "datetime",
    "balancingAccountId": "GUID",
    "balancingAccountNumber": "string"
}
```

## Related information

[GET customerPaymentJournal](../api/dynamics_customerPaymentJournal_Get.md)  
[DELETE customerPaymentJournal](../api/dynamics_customerPaymentJournal_Delete.md)  
[POST customerPaymentJournal](../api/dynamics_customerPaymentJournal_Create.md)  
[PATCH customerPaymentJournal](../api/dynamics_customerPaymentJournal_Update.md)
