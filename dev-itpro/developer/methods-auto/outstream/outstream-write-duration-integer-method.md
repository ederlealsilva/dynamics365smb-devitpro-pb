---
title: "OutStream.Write(Duration [, Integer]) Method"
description: "Writes a specified number of bytes to the stream."
ms.author: solsen
ms.date: 08/26/2024
ms.topic: reference
author: SusanneWindfeldPedersen
ms.reviewer: solsen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# OutStream.Write(Duration [, Integer]) Method
> **Version**: _Available or changed with runtime version 1.0._

Writes a specified number of bytes to the stream. Data is written in binary format.


## Syntax
```AL
[Written := ]  OutStream.Write(Value: Duration [, Length: Integer])
```
## Parameters
*OutStream*  
&emsp;Type: [OutStream](outstream-data-type.md)  
An instance of the [OutStream](outstream-data-type.md) data type.  

*Value*  
&emsp;Type: [Duration](../duration/duration-data-type.md)  
Contains the data to be written.  

*[Optional] Length*  
&emsp;Type: [Integer](../integer/integer-data-type.md)  
The number of bytes to be written. In the case of data types other than string, code, and binary, if you specify a length that differs from the size of the variable, an error message is displayed.  


## Return Value
*[Optional] Written*  
&emsp;Type: [Integer](../integer/integer-data-type.md)  
The number of bytes that were written. If you omit this optional return value and the operation does not execute successfully, a runtime error will occur.  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks
Write adds a zero byte at the end of the stream. This is differs from WriteText, which does not. For more information about how zero bytes and line endings are written and read, see [Write, WriteText, Read, and ReadText Method Behavior Regarding Line Endings and Zero Terminators](../../devenv-write-read-methods-line-break-behavior.md).

 If the optional return value, *Written*, is not specified and it was not possible to write all the data, an error message is displayed.  
  
 If the return value is present, you must verify that all the data was streamed.  
  
## Example  
  
  
```al
 var
    recBinaries: Record "Company Information";
    OStream: OutStream;
    Dur: Duration;
begin
    recBinaries.Find('-');  
    recBinaries.Picture.CreateOutstream(OStream);   
    OStream.Write(Dur);  
    recBinaries.Modify();  
end;
```   
  

## Related information
[OutStream Data Type](outstream-data-type.md)  
[Get Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)