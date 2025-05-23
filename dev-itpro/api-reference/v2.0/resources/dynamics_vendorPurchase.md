---
title: vendorPurchase resource type  
description: A vendor purchase object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 04/09/2024
ms.author: solsen
ms.reviewer: solsen
---

# vendorPurchase resource type

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Represents a vendor purchase in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

> [!NOTE]
> For information about enabling APIs for [!INCLUDE[prod_short](../../../includes/prod_short.md)] see [Enabling the APIs for Dynamics 365 Business Central](../enabling-apis-for-dynamics-nav.md).

## Methods

| Method | Return Type|Description |
|:--------------------|:-----------|:-------------------------|
|[GET vendorPurchase](../api/dynamics_vendorpurchase_get.md)|vendorPurchase|Gets a vendor purchase object.|


## Properties

| Property           | Type   |Description     |
|:-------------------|:-------|:---------------|
|vendorId|GUID|The unique ID of vendor.|
|vendorNumber|string|Specifies vendor's number.|
|name|string|Represents the vendor purchase's name.|
|totalPurchaseAmount|decimal|Represents the vendor purchases.|
|dateFilter_FilterOnly|date|Represents the date filter for the vendor purchase.|

## JSON representation

Here's a JSON representation of the vendorPurchase resource.


```json
{
    "vendorId": "GUID",
    "vendorNumber": "string",
    "name": "string",
    "totalPurchaseAmount": "decimal",
    "dateFilter_FilterOnly": "date"
}
```

## Related information

[GET vendorPurchase](../api/dynamics_vendorPurchase_Get.md)
