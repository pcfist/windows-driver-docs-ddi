---
UID: NF:dbgeng.IDebugSymbols.SetSymbolPath
title: IDebugSymbols::SetSymbolPath method
author: windows-driver-content
description: The SetSymbolPath method sets the symbol path.
old-location: debugger\setsymbolpath.htm
old-project: debugger
ms.assetid: c003fb1d-b24b-4e79-b8f4-6ff425f77554
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IDebugSymbols, IDebugSymbols interface [Windows Debugging], SetSymbolPath method, IDebugSymbols2 interface [Windows Debugging], SetSymbolPath method, IDebugSymbols2::SetSymbolPath, IDebugSymbols3 interface [Windows Debugging], SetSymbolPath method, IDebugSymbols3::SetSymbolPath, IDebugSymbols::SetSymbolPath, IDebugSymbols_b699ac62-be52-4f79-9762-8ed1274dfb41.xml, SetSymbolPath method [Windows Debugging], SetSymbolPath method [Windows Debugging], IDebugSymbols interface, SetSymbolPath method [Windows Debugging], IDebugSymbols2 interface, SetSymbolPath method [Windows Debugging], IDebugSymbols3 interface, SetSymbolPath,IDebugSymbols.SetSymbolPath, dbgeng/IDebugSymbols2::SetSymbolPath, dbgeng/IDebugSymbols3::SetSymbolPath, dbgeng/IDebugSymbols::SetSymbolPath, debugger.setsymbolpath
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
-	IDebugSymbols.SetSymbolPath
-	IDebugSymbols2.SetSymbolPath
-	IDebugSymbols3.SetSymbolPath
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugSymbols::SetSymbolPath method


## -description


The <b>SetSymbolPath</b>  method sets the symbol path.


## -syntax


````
HRESULT SetSymbolPath(
  [in] PCSTR Path
);
````


## -parameters




### -param Path [in]

Specifies the new symbol path.  This is a string that contains symbol path elements separated by semicolons (;).  Each symbol path element can specify either a directory or a symbol server.


## -returns



This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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
</table>
 




## -remarks



For more information about manipulating the symbol path, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560150">Using Symbols</a>.  For an overview of the symbol path and its syntax, see <a href="https://msdn.microsoft.com/705df98f-717f-40ad-a424-101826970691">Symbol Path</a>.




## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols.md">IDebugSymbols</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538110">AppendSymbolPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549155">GetSymbolPath</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>



 

 


