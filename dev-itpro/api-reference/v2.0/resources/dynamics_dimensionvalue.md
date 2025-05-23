---
title: dimensionValue resource type  
description: A dimension value object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 04/28/2025
ms.author: solsen
ms.reviewer: solsen
---

# dimensionValue resource type

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Represents a dimension value in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

> [!NOTE]
> For information about enabling APIs for [!INCLUDE[prod_short](../../../includes/prod_short.md)] see [Enabling the APIs for Dynamics 365 Business Central](../enabling-apis-for-dynamics-nav.md).

## Methods

| Method | Return Type|Description |
|:--------------------|:-----------|:-------------------------|
|[GET dimensionValue](../api/dynamics_dimensionvalue_get.md)|dimensionValue|Gets a dimension value object.|

## Navigation

| Navigation |Return Type| Description |
|:----------|:----------|:-----------------|
|[dimension](dynamics_dimension.md)|dimension |Gets the dimension of the dimensionValue.|

## Properties

| Property           | Type   |Description     |
|:-------------------|:-------|:---------------|
|id|GUID|The unique ID of the dimension value. Non-editable.|
|code|string|The code of the dimension value.|
|dimensionId|GUID|The unique ID of dimension.|
|displayName|string|Specifies the dimension value's name. This name will appear on all sales documents for the dimension value.|
|consolidationCode|string||
|lastModifiedDateTime|datetime|The last datetime the dimension value was modified. Read-Only.|

## JSON representation

Here's a JSON representation of the dimensionValue resource.


```json
{
    "id": "GUID",
    "code": "string",
    "dimensionId": "GUID",
    "displayName": "string",
    "consolidationCode": "string",
    "lastModifiedDateTime": "datetime"
}
```

## Related information

[GET dimensionValue](../api/dynamics_dimensionValue_Get.md)
