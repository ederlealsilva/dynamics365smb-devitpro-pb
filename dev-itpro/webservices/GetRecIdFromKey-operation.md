---
title: "GetRecIdFromKey"
ms.date: 04/01/2021
ms.topic: article
---
# GetRecIdFromKey
Converts a key to a record ID. The key is always part of the page result.  
  
## Method Signature  
 `string GetRecIdFromKey(string key)`  
  
## Parameters  
  
|Parameter|[!INCLUDE[bp_tabledescription](../developer/includes/bp_tabledescription_md.md)]|  
|---------------|---------------------------------------|  
|*key*|Type: String<br /><br /> The bookmark of the record that includes both primary key and concurrency information.|  
  
## Results  
  
|Result name|[!INCLUDE[bp_tabledescription](../developer/includes/bp_tabledescription_md.md)]|  
|-----------------|---------------------------------------|  
|*String*|Type: String<br /><br /> The record ID that was obtained from the key.|  
  
## Faults  
  
|SOAP fault message|[!INCLUDE[bp_tabledescription](../developer/includes/bp_tabledescription_md.md)]|  
|------------------------|---------------------------------------|  
|\[*record name*\] \[*field*\] \[*value*\] does not exist.|Indicates that the record has been deleted by another user or process after it has been retrieved for this operation.|  
  
## Usage Example  
  
```c#  
  
Customer_Service service = new Customer_Service();  
Customer cust = new Customer();  
service.UseDefaultCredentials = true;  
string id = service.GetRecIdFromKey(cust.No);  
cust = service.ReadByRecId(id.ToUpper());  
```  
  
## Related information  
 [Basic Page Operations](Basic-Page-Operations.md)
