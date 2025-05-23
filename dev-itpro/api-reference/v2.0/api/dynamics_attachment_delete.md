---
title: Delete attachment  
description: Deletes attachments in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 05/31/2024
ms.author: solsen
ms.reviewer: solsen
---

# Delete attachments

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Deletes attachments in [!INCLUDE[prod_short](../../../includes/prod_short.md)]. An attachment in the [!INCLUDE[prod_short](../../../includes/prod_short.md)] API is defined as an Incoming Document (table 130).

## HTTP request
Replace the URL prefix for [!INCLUDE[prod_short](../../../includes/prod_short.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).
```
DELETE businesscentralPrefix/companies({companyId})/attachments({attachmentId})
```

## Request headers

|Header|Value|
|------|-----|
|Authorization  |Bearer {token}. Required. |
|If-Match       |Required. When this request header is included and the eTag provided doesn't match the current tag on the **attachment**, the **attachment** won't be updated. |


## Request body
Don't supply a request body for this method.

## Response
If successful, this method returns a ```204 No Content``` response code and it deletes the attachment.

## Example

**Request**

Here's an example of the request.

```json
DELETE https://{businesscentralPrefix}/api/v2.0/companies({companyId})/attachments({parentId},{attachmentId})
```

**Response** 

Here's an example of the response.

```json
HTTP/1.1 204 No Content
```

## Related information

[Tips for working with the APIs](../../../developer/devenv-connect-apps-tips.md)  
[attachment](../resources/dynamics_attachment.md)  
[Get attachment](dynamics_attachment_get.md)  
[Create attachment](dynamics_attachment_create.md)  
[Update attachment](dynamics_attachment_update.md)
