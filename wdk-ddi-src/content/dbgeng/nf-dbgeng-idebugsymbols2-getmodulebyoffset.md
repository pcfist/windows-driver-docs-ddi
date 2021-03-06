---
UID: NF:dbgeng.IDebugSymbols2.GetModuleByOffset
title: IDebugSymbols2::GetModuleByOffset method
author: windows-driver-content
description: The GetModuleByOffset method searches through the target's modules for one whose memory allocation includes the specified location.
old-location: debugger\getmodulebyoffset.htm
old-project: debugger
ms.assetid: ff51d0d1-47f1-4df6-b671-d74f791d778b
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetModuleByOffset method [Windows Debugging], GetModuleByOffset method [Windows Debugging], IDebugSymbols interface, GetModuleByOffset method [Windows Debugging], IDebugSymbols2 interface, GetModuleByOffset method [Windows Debugging], IDebugSymbols3 interface, GetModuleByOffset,IDebugSymbols2.GetModuleByOffset, IDebugSymbols interface [Windows Debugging], GetModuleByOffset method, IDebugSymbols2, IDebugSymbols2 interface [Windows Debugging], GetModuleByOffset method, IDebugSymbols2::GetModuleByOffset, IDebugSymbols3 interface [Windows Debugging], GetModuleByOffset method, IDebugSymbols3::GetModuleByOffset, IDebugSymbols::GetModuleByOffset, IDebugSymbols_2f5375ce-a9f1-4e86-ab82-7f35edc716c2.xml, dbgeng/IDebugSymbols2::GetModuleByOffset, dbgeng/IDebugSymbols3::GetModuleByOffset, dbgeng/IDebugSymbols::GetModuleByOffset, debugger.getmodulebyoffset
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
-	IDebugSymbols.GetModuleByOffset
-	IDebugSymbols2.GetModuleByOffset
-	IDebugSymbols3.GetModuleByOffset
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugSymbols2::GetModuleByOffset method


## -description


The <b>GetModuleByOffset</b> method searches through the target's <a href="https://msdn.microsoft.com/library/windows/hardware/ff552231">modules</a> for one whose memory allocation includes the specified location.


## -syntax


````
HRESULT GetModuleByOffset(
  [in]            ULONG64  Offset,
  [in]            ULONG    StartIndex,
  [out, optional] PULONG   Index,
  [out, optional] PULONG64 Base
);
````


## -parameters




### -param Offset [in]

Specifies a location in the target's virtual address space which is inside the desired module's memory allocation -- for example, the address of a symbol belonging to the module.


### -param StartIndex [in]

Specifies the index to start searching from.


### -param Index [out, optional]

Receives the index of the module.  If <i>Index</i> is <b>NULL</b>, this information is not returned.


### -param Base [out, optional]

Receives the location in the target's memory address space of the base of the module.  If <i>Base</i> is <b>NULL</b>, this information is not returned.


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
</table>
 




## -remarks



Starting at the specified index, this method returns the first module it finds whose memory allocation address range includes the specified location.  If the target has more than one module whose memory address range includes this location, then subsequent modules can be found by repeated calls to this method with higher values of <i>StartIndex</i>.

For more information about modules, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552231">Modules</a>.




## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547080">GetModuleByIndex</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols.md">IDebugSymbols</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547138">GetModuleByOffset2</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>



 

 


