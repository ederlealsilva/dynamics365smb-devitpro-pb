---
title: DELETE vendorPaymentJournals  
description: Deletes vendorPaymentJournal  in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 05/31/2024
ms.author: solsen
ms.reviewer: solsen
---

# Delete vendorPaymentJournals

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Deletes vendorPaymentJournals in [!INCLUDE[prod_short](../../../includes/prod_short.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[prod_short](../../../includes/prod_short.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).
```
DELETE businesscentralPrefix/companies({id})/vendorPaymentJournals({id})
```

## Request headers

|Header         |Value                     |
|---------------|--------------------------|
|Authorization  |Bearer {token}. Required. |
|If-Match       |Required. When this request header is included and the eTag provided doesn't match the current tag on the **vendorPaymentJournal**, the **vendorPaymentJournals** won't be updated. |

## Request body
Don't supply a request body for this method.

## Response
If successful, this method returns a ```204 No Content``` response code and it deletes the vendorPaymentJournal .

## Example

**Request**

Here's an example of the request.

```json
DELETE https://{businesscentralPrefix}/api/v2.0/companies({id})/vendorPaymentJournals({id})
```

**Response** 

Here's an example of the response. 

```json
HTTP/1.1 204 No Content
```

## Related information
[Tips for working with the APIs](../../../developer/devenv-connect-apps-tips.md)  
[vendorPaymentJournal](../resources/dynamics_vendorPaymentJournal.md)  
[Get vendorPaymentJournal](dynamics_vendorPaymentJournal_Get.md)   
[Create vendorPaymentJournal](dynamics_vendorPaymentJournal_Create.md)   
[Update vendorPaymentJournal](dynamics_vendorPaymentJournal_Update.md)   

