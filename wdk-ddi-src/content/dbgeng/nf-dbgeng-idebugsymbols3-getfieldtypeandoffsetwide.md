---
UID: NF:dbgeng.IDebugSymbols3.GetFieldTypeAndOffsetWide
title: IDebugSymbols3::GetFieldTypeAndOffsetWide method
author: windows-driver-content
description: The GetFieldTypeAndOffsetWide method returns the type of a field and its offset within a container.
old-location: debugger\getfieldtypeandoffsetwide.htm
old-project: debugger
ms.assetid: b4e38b33-2f23-4439-b0bc-ab3524e5180e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetFieldTypeAndOffsetWide method [Windows Debugging], GetFieldTypeAndOffsetWide method [Windows Debugging], IDebugSymbols3 interface, GetFieldTypeAndOffsetWide,IDebugSymbols3.GetFieldTypeAndOffsetWide, IDebugSymbols3, IDebugSymbols3 interface [Windows Debugging], GetFieldTypeAndOffsetWide method, IDebugSymbols3::GetFieldTypeAndOffsetWide, dbgeng/IDebugSymbols3::GetFieldTypeAndOffsetWide, debugger.getfieldtypeandoffsetwide
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dbgeng.h
api_name:
-	IDebugSymbols3.GetFieldTypeAndOffsetWide
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugSymbols3::GetFieldTypeAndOffsetWide method


## -description


The <b>GetFieldTypeAndOffsetWide</b>  method returns the type of a field and its offset within a container.


## -syntax


````
HRESULT GetFieldTypeAndOffsetWide(
  [in]            ULONG64 Module,
  [in]            ULONG   ContainerTypeId,
  [in]            PCWSTR  Field,
  [out, optional] PULONG  FieldTypeId,
  [out, optional] PULONG  Offset
);
````


## -parameters




### -param Module [in]

Specifies the module containing the types of both the container and the field.


### -param ContainerTypeId [in]

Specifies the type ID for the container's type.  Examples of containers include structures, unions, and classes.


### -param Field [in]

Specifies the name of the field whose type and offset are requested.  Subfields may be specified by using a dot-separated path.


### -param FieldTypeId [out, optional]

Receives the type ID of the field.


### -param Offset [out, optional]

Receives the offset of the field <i>Field</i> from the base memory location of an instance of the container.


## -returns



This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The field <i>Field</i> could not be found in the type specified by <i>ContainerTypeId</i>.

</td>
</tr>
</table>
 




## -remarks



An example of a dot-separated path for the <i>Field</i> parameter is as follows.  Suppose the MyStruct structure contains a field <b>MyField</b> of type MySubStruct, and the MySubStruct structure contains the field <b>MySubField</b>.  Then the type of this field and its location relative to the location of MyStruct structure can be found by passing "MyField.MySubField" as the <i>Field</i> parameter to this method.

For more information about types, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558931">Types</a>.  For more information about symbols, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558824">Symbols</a>.




## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546758">GetFieldOffset</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549376">GetTypeId</a>



 

 


