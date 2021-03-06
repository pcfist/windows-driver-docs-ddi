---
UID: NF:dbgeng.IDebugSymbols3.AddTypeOptions
title: IDebugSymbols3::AddTypeOptions method
author: windows-driver-content
description: The AddTypeOptions method turns on some type formatting options for output generated by the engine.
old-location: debugger\addtypeoptions.htm
old-project: debugger
ms.assetid: fe7fadc4-6ace-421a-986d-6fb2e0950ce8
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: AddTypeOptions method [Windows Debugging], AddTypeOptions method [Windows Debugging], IDebugSymbols2 interface, AddTypeOptions method [Windows Debugging], IDebugSymbols3 interface, AddTypeOptions,IDebugSymbols3.AddTypeOptions, IDebugSymbols2 interface [Windows Debugging], AddTypeOptions method, IDebugSymbols2::AddTypeOptions, IDebugSymbols3, IDebugSymbols3 interface [Windows Debugging], AddTypeOptions method, IDebugSymbols3::AddTypeOptions, IDebugSymbols_e856a688-7f26-4a00-b911-5b23a0bafa11.xml, dbgeng/IDebugSymbols2::AddTypeOptions, dbgeng/IDebugSymbols3::AddTypeOptions, debugger.addtypeoptions
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
-	Dbgeng.h
api_name:
-	IDebugSymbols2.AddTypeOptions
-	IDebugSymbols3.AddTypeOptions
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugSymbols3::AddTypeOptions method


## -description


The <b>AddTypeOptions</b> method turns on some type formatting options for output generated by the <a href="https://msdn.microsoft.com/1e32bd40-8c77-4c6b-913c-6ec26707ed36">engine</a>.


## -syntax


````
HRESULT AddTypeOptions(
  [in] ULONG Options
);
````


## -parameters




### -param Options [in]

Specifies type formatting options to turn on.  <i>Options</i> is a bit-set that will be ORed with the existing type formatting options.  For a description of the bit flags, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff541712">DEBUG_TYPEOPTS_XXX</a>.


## -returns



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
 

This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.




## -remarks



After the type options have been changed, for each <a href="https://msdn.microsoft.com/295b05a3-e27f-4761-a562-7e87e25bfd3b">client</a> the engine sends out notification to that client's <a href="..\dbgeng\nn-dbgeng-idebugeventcallbacks.md">IDebugEventCallbacks</a> by passing the DEBUG_CES_TYPE_OPTIONS flag to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550692">IDebugEventCallbacks::ChangeSymbolState</a> method.

For more information about types, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558931">Types</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff556874">SetTypeOptions</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554551">RemoveTypeOptions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549428">GetTypeOptions</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>



 

 


