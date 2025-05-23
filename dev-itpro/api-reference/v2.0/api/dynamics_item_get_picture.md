---
title: Get item picture  
description: Gets an item picture in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 05/31/2024
ms.author: solsen
ms.reviewer: solsen
---

# Get item picture

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Gets the picture of the item in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[prod_short](../../../includes/prod_short.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md). 
The following example gets the default dimensions of the item entity in the response body.

```
GET businesscentralPrefix/companies({companyId})/items({itemId})/picture
```

## Request header

|Header|Value|
|------|-----|
|Authorization| Bearer {token}. Required.|

## Request body
Don't supply a request body for this method.

## Response 

If successful, this method returns a `200 OK` response code and the **picture** in the response body.

## Example 
**Request**

```json
GET https://{businesscentralPrefix}/api/v2.0/companies({companyId})/items({itemId})/picture
```

**Response**  
Here's an example of the response.

> [!NOTE]  
> The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.

```json
{
  "id": "d0e5d5da-795a-4924-b376-13665f794cdd",
  "width": 500,
  "height": 496,
  "contentType": "image\jpeg",
  "content@odata.mediaEditLink": "https:\\api.businesscentral.dynamics-tie.com\v2.0\api\beta\companies(55c438d0-2f5c-44a0-9965-20b4923d0bef)\items(d0e5d5da-795a-4924-b376-13665f794cdd)\picture(d0e5d5da-795a-4924-b376-13665f794cdd)\content",
  "content@odata.mediaReadLink": "https:\\api.businesscentral.dynamics-tie.com\v2.0\api\beta\companies(55c438d0-2f5c-44a0-9965-20b4923d0bef)\items(d0e5d5da-795a-4924-b376-13665f794cdd)\picture(d0e5d5da-795a-4924-b376-13665f794cdd)\content"
}
```

## Related information

[Tips for working with the APIs](../../../developer/devenv-connect-apps-tips.md)  
[Items](../resources/dynamics_item.md)  
[Create item picture](dynamics_item_create_picture.md)  
[Update item picture](dynamics_item_update_picture.md)  
[Delete item picture](dynamics_item_delete_picture.md)  

