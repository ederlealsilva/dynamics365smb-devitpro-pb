---
title: location resource type
description: A location object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 04/28/2025
ms.author: solsen
ms.reviewer: solsen
---

# location resource type

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Represents a location in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

> [!NOTE]
> For information about enabling APIs for [!INCLUDE[prod_short](../../../includes/prod_short.md)] see [Enabling the APIs for Dynamics 365 Business Central](../enabling-apis-for-dynamics-nav.md).

## Methods

| Method | Return Type|Description |
|:--------------------|:-----------|:-------------------------|
|[GET location](../api/dynamics_location_get.md)|location|Gets a location object.|
|[DELETE location](../api/dynamics_location_delete.md)|none|Deletes a location object.|
|[POST location](../api/dynamics_location_create.md)|location|Creates a location object.|
|[PATCH location](../api/dynamics_location_update.md)|location|Updates a location object.|

## Properties

| Property           | Type   |Description     |
|:-------------------|:-------|:---------------|
|id|GUID|The unique ID of the location. Non-editable.|
|code|string|The code of the location.|
|displayName|string|Specifies the location's name. This name will appear on all sales documents for the location.|
|contact|string||
|addressLine1|string|Specifies the location's address. This address will appear on all sales documents for the location.|
|addressLine2|string|Specifies the location's address. This address will appear on all sales documents for the location.|
|city|string|Specifies the location's city.|
|state|string|Specifies the location's state.|
|country|string|Specifies the location's country.|
|postalCode|string|Specifies the location's postal code.|
|phoneNumber|string|Specifies the location's telephone number.|
|email|string|Specifies the location's email address.|
|website|string|Specifies the location's home page address.|
|lastModifiedDateTime|datetime|The last datetime the location was modified. Read-Only.|

## JSON representation

Here's a JSON representation of the location resource.


```json
{
    "id": "GUID",
    "code": "string",
    "displayName": "string",
    "contact": "string",
    "addressLine1": "string",
    "addressLine2": "string",
    "city": "string",
    "state": "string",
    "country": "string",
    "postalCode": "string",
    "phoneNumber": "string",
    "email": "string",
    "website": "string",
    "lastModifiedDateTime": "datetime"
}
```

## Related information

[GET location](../api/dynamics_location_get.md)   
[DELETE location](../api/dynamics_location_delete.md)  
[POST location](../api/dynamics_location_create.md)  
[PATCH location](../api/dynamics_location_update.md)
