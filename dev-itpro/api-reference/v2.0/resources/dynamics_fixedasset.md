---
title: fixedAsset resource type
description: A fixed asset object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 04/28/2025
ms.author: solsen
ms.reviewer: solsen
---

# fixedAsset resource type

Represents a fixed asset in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

> [!NOTE]
> For information about enabling APIs for [!INCLUDE[prod_short](../../../includes/prod_short.md)] see [Enabling the APIs for Dynamics 365 Business Central](../enabling-apis-for-dynamics-nav.md).

## Methods

| Method | Return Type|Description |
|:--------------------|:-----------|:-------------------------|
|[GET fixedAsset](../api/dynamics_fixedasset_get.md)|fixedAsset|Gets a fixed asset object.|
|[DELETE fixedAsset](../api/dynamics_fixedasset_delete.md)|none|Deletes a fixed asset object.|
|[POST fixedAsset](../api/dynamics_fixedasset_create.md)|fixedAsset|Creates a fixed asset object.|
|[PATCH fixedAsset](../api/dynamics_fixedasset_update.md)|fixedAsset|Updates a fixed asset object.|


## Navigation

| Navigation |Return Type| Description |
|:----------|:----------|:-----------------|
|[fixedAssetLocation](dynamics_fixedassetlocation.md)|fixedAssetLocation |Gets the fixedassetlocation of the fixedAsset.|
|[employee](dynamics_employee.md)|employee |Gets the employee of the fixedAsset.|

## Properties

| Property           | Type   |Description     |
|:-------------------|:-------|:---------------|
|id|GUID|The unique ID of the fixed asset. Non-editable.|
|number|string|Specifies the number of the fixed asset.|
|displayName|string|Specifies the fixed asset's name. This name will appear on all sales documents for the fixed asset.|
|fixedAssetLocationCode|string||
|fixedAssetLocationId|GUID||
|classCode|string||
|subclassCode|string||
|blocked|boolean|Specifies that entries can't be posted to the fixed asset. **True** indicates account is blocked and posting is not allowed.|
|serialNumber|string||
|employeeNumber|string|The employee's number.|
|employeeId|GUID|The unique ID of employee.|
|underMaintenance|boolean||
|lastModifiedDateTime|datetime|The last datetime the fixed asset was modified. Read-Only.|

## JSON representation

Here's a JSON representation of the fixedAsset resource.


```json
{
    "id": "GUID",
    "number": "string",
    "displayName": "string",
    "fixedAssetLocationCode": "string",
    "fixedAssetLocationId": "GUID",
    "classCode": "string",
    "subclassCode": "string",
    "blocked": "boolean",
    "serialNumber": "string",
    "employeeNumber": "string",
    "employeeId": "GUID",
    "underMaintenance": "boolean",
    "lastModifiedDateTime": "datetime"
}
```

## Related information

[GET fixedAsset](../api/dynamics_fixedasset_get.md)  
[DELETE fixedAsset](../api/dynamics_fixedasset_delete.md)  
[POST fixedAsset](../api/dynamics_fixedasset_create.md)  
[PATCH fixedAsset](../api/dynamics_fixedasset_update.md)
