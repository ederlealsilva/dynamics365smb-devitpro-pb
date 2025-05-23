---
title: "OnRename (Table) trigger"
description: "Runs when a user tries to rename a record."
ms.author: solsen
ms.date: 08/26/2024
ms.topic: reference
author: SusanneWindfeldPedersen
ms.reviewer: solsen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)

# OnRename (Table) trigger
> **Version**: _Available or changed with runtime version 1.0._

Runs when a user tries to rename a record.


## Syntax
```AL
trigger OnRename()
begin
    ...
end;
```



[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks  
When you rename a record in one location, it is updated in all other locations. It runs automatically when the user changes a record's primary key field in a page from the Web Client.  The OnRename trigger runs after field validation and before the default renaming behavior, which checks that the new name does not correspond to an already existing record before the rename occurs. The record is not renamed if an error occurs in the trigger code.  

## Related information  
[Get Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)  
[OnRename (Table Extension) Trigger](../tableextension/devenv-onrename-tableextension-trigger.md)
