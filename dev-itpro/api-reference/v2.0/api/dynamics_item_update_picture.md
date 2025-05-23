---
title: Update item picture  
description: Updates the item picture in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 05/31/2024
ms.author: solsen
ms.reviewer: solsen
---

# Update item picture

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Update the picture of the item in [!INCLUDE[prod_short](../../../includes/prod_short.md)].


## HTTP request
Replace the URL prefix for [!INCLUDE[prod_short](../../../includes/prod_short.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).
```
PATCH businesscentralPrefix/companies({companyId})/items({itemId})/picture
```

## Request headers

|Header        |Value                    |
|--------------|-------------------------|
|Authorization |Bearer {token}. Required.|
|Content-Type  |application/json         |

## Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that aren't included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

> [!NOTE]  
> You can't modify parentId, dimensionId or dimensionCode fields, because these are key fields, and rename is not allowed in Default Dimension record.

## Response
If successful, this method returns a `200 OK` response code and an updated default dimensions for the **item** in the response body. 

## Example

**Request**

Here's an example of the request.

```json
PATCH https://{businesscentralPrefix}/api/v2.0/companies({companyId})/items({itemId})/picture
```

**Request body**


**Response**

Here's an example of the response. 

> [!NOTE]  
> The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.

```json

```

## Related information

[Tips for working with the APIs](../../../developer/devenv-connect-apps-tips.md)  
[Items](../resources/dynamics_item.md)  
[Create item picture](dynamics_item_create_picture.md)  
[Get item picture](dynamics_item_get_picture.md)  
[Delete item picture](dynamics_item_delete_picture.md)  

