---
title: Delete journalLines  
description: Deletes a journal line in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 05/31/2024
ms.author: solsen
ms.reviewer: solsen
---

# Delete journalLines

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Delete a journal line object from [!INCLUDE[prod_short](../../../includes/prod_short.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[prod_short](../../../includes/prod_short.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).
```
DELETE businesscentralPrefix/companies({id})/journals({id})/journalLines({id})
```

## Request headers

|Header          |Value                     |
|----------------|--------------------------|
|Authorization   |Bearer {token}. Required. |
|If-Match        |Required. When this request header is included and the eTag provided doesn't match the current tag on the **journalLines**, the **journalLines** won't be updated. |

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns ```204 No Content``` response code. It doesn't return anything in the response body.

## Example

**Request**

Here's an example of the request.

```json
DELETE https://{businesscentralPrefix}/api/v2.0/companies({id})/journals({id})/journalLines({id})
```

**Response** 

Here's an example of the response. 

```json
HTTP/1.1 204 No Content
```

## Related information
[Tips for working with the APIs](../../../developer/devenv-connect-apps-tips.md)    
[journalline](../resources/dynamics_journalline.md)    
[Get journalline](dynamics_journalline_Get.md)    
[Create journalline](dynamics_journalline_Create.md)    
[Update journalline](dynamics_journalline_Update.md)    
