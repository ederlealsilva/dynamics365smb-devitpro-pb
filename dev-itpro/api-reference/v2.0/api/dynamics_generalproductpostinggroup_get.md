---
title: Get generalProductPostingGroups
description: Gets a general product posting group object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: reference
ms.devlang: al
ms.date: 05/31/2024
ms.author: solsen
ms.reviewer: solsen
---

# Get generalProductPostingGroups

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Retrieves the properties and relationships of a general product posting group object for [!INCLUDE[prod_short](../../../includes/prod_short.md)].

## HTTP request

Replace the URL prefix for [!INCLUDE[prod_short](../../../includes/prod_short.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).

```
GET businesscentralPrefix/companies({id})/generalProductPostingGroups({id})
```

## Request headers

|Header|Value|
|------|-----|
|Authorization  |Bearer {token}. Required. |

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a ```200 OK``` response code and a **generalProductPostingGroup** object in the response body.

## Example

**Request**

Here's an example of the request.

```json
GET https://{businesscentralPrefix}/api/v2.0/companies({id})/generalProductPostingGroups({id})
```

**Response**

Here's an example of the response.

```json
{
"@odata.etag": "W/\"JzQ0O1RkZjFGSzJKcXR3VU5QTmNyMUNuUjltT2Z5b1FtWjV5eGdndHNKcXN5bFE9MTswMDsn\"",
"id": "50bd9bdb-51ff-eb11-bb76-000d3a220646",
"code": "MISC",
"description": "Miscellaneous with VAT",
"defaultVATProductPostingGroup": "VAT25",
"autoInsertDefault": true
}
```

## Related information

[Tips for working with the APIs](/dynamics365/business-central/dev-itpro/developer/devenv-connect-apps-tips)  
[generalProductPostingGroup](../resources/dynamics_generalProductPostingGroup.md)  
