---
title: Isolated Storage
description: Isolated Storage is a data storage that provides isolation between extensions, so that you can keep keys/values in one extension from being accessed from other extensions.
ms.date: 06/14/2024
ms.topic: article
author: SusanneWindfeldPedersen
---

# Isolated Storage

Isolated Storage is a data storage that provides isolation between extensions, so that you can keep keys/values in one extension from being accessed from other extensions. Keys/values in the Isolated Storage are accessible through an API. The option type used for classifying data is [DataScope Option Type](methods-auto/datascope/datascope-option.md) and the data type used is the [IsolatedStorage Data Type](methods-auto/isolatedstorage/isolatedstorage-data-type.md).

The methods supported for IsolatedStorage are:

|Method|Description|For more information, see|  
|--------------|-----------------|-------------------------------|  
|Set(String, String, [DataScope])|Sets the value associated with the specified key within the extension.|[Set(String, String, [DataScope]) Method](methods-auto/isolatedstorage/isolatedstorage-set-string-string-datascope-method.md)|  
|Get(String, [DataScope], var Text)|Gets the value associated with the specified key within the extension.|[Get(String, [DataScope], var Text) Method](methods-auto/isolatedstorage/isolatedstorage-get-string-datascope-text-method.md)|  
|Contains(String, [DataScope])|Determines whether the storage contains a value with the specified key within the extension.|[Contains(String, [DataScope]) Method](methods-auto/isolatedstorage/isolatedstorage-contains-string-datascope-boolean-method.md)|  
|Delete(String, [DataScope])|Deletes the value with the specified key from the isolated storage within the extension.|[IsolatedStorage.Delete Method](methods-auto/isolatedstorage/isolatedstorage-delete-method.md)|
|SetEncrypted(String, String, [DataScope])|Encrypts and sets the value associated with the specified key. The input string cannot exceed a length of 215 plain characters; be aware that special characters take up more space.|[SetEncrypted(String, String, [DataScope]) Method](methods-auto/isolatedstorage/isolatedstorage-setencrypted-string-string-datascope-method.md)|

## Related information

[DataScope Option Type](methods-auto/datascope/datascope-option.md)  
[IsolatedStorage Data Type](methods-auto/isolatedstorage/isolatedstorage-data-type.md)  
