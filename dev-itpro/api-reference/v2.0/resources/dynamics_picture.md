---
title: picture resource type  
description: A picture object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 04/28/2025
ms.author: solsen
ms.reviewer: solsen
---

# picture resource type

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Represents a picture in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

> [!NOTE]
> For information about enabling APIs for [!INCLUDE[prod_short](../../../includes/prod_short.md)] see [Enabling the APIs for Dynamics 365 Business Central](../enabling-apis-for-dynamics-nav.md).

## Methods

| Method | Return Type|Description |
|:--------------------|:-----------|:-------------------------|
|[GET picture](../api/dynamics_picture_get.md)|picture|Gets a picture object.|
|[DELETE picture](../api/dynamics_picture_delete.md)|none|Deletes a picture object.|
|[PATCH picture](../api/dynamics_picture_update.md)|picture|Updates a picture object.|

## Navigation

| Navigation |Return Type| Description |
|:----------|:----------|:-----------------|
|[item](dynamics_item.md)|item |Gets the item of the picture.|
|[customer](dynamics_customer.md)|customer |Gets the customer of the picture.|
|[contact](dynamics_contact.md)|contact |Gets the contact of the picture.|
|[vendor](dynamics_vendor.md)|vendor |Gets the vendor of the picture.|
|[employee](dynamics_employee.md)|employee |Gets the employee of the picture.|

## Properties

| Property           | Type   |Description     |
|:-------------------|:-------|:---------------|
|id|GUID|The unique ID of the picture. Non-editable.|
|parentType|NAV.pictureEntityParentType|The type of the parent document of the picture. It can be "Customer","Item", "Vendor", "Employee". |
|width|integer|The width of the picture.|
|height|integer|The height of the picture.|
|contentType|string|The media type of the picture.|
|pictureContent|stream|The picture's content.|

## JSON representation

Here's a JSON representation of the picture resource.


```json
{
    "id": "GUID",
    "parentType": "NAV.pictureEntityParentType",
    "width": "integer",
    "height": "integer",
    "contentType": "string",
    "pictureContent": "stream"
}
```

## Related information

[GET picture](../api/dynamics_picture_Get.md)  
[DELETE picture](../api/dynamics_picture_Delete.md)  
[PATCH picture](../api/dynamics_picture_Update.md)
