---
UID: NF:dbgeng.IDebugClient5.TerminateCurrentProcess
title: IDebugClient5::TerminateCurrentProcess method
author: windows-driver-content
description: The TerminateCurrentProcess method attempts to terminate the current process.
old-location: debugger\terminatecurrentprocess.htm
old-project: debugger
ms.assetid: 8d3798f2-dd43-4703-bd33-8f2c3f738122
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IDebugClient2 interface [Windows Debugging], TerminateCurrentProcess method, IDebugClient2::TerminateCurrentProcess, IDebugClient3 interface [Windows Debugging], TerminateCurrentProcess method, IDebugClient3::TerminateCurrentProcess, IDebugClient4 interface [Windows Debugging], TerminateCurrentProcess method, IDebugClient4::TerminateCurrentProcess, IDebugClient5, IDebugClient5 interface [Windows Debugging], TerminateCurrentProcess method, IDebugClient5::TerminateCurrentProcess, IDebugClient_7129a1e4-f1a5-4dff-a45c-bf759ae410cf.xml, TerminateCurrentProcess method [Windows Debugging], TerminateCurrentProcess method [Windows Debugging], IDebugClient2 interface, TerminateCurrentProcess method [Windows Debugging], IDebugClient3 interface, TerminateCurrentProcess method [Windows Debugging], IDebugClient4 interface, TerminateCurrentProcess method [Windows Debugging], IDebugClient5 interface, TerminateCurrentProcess,IDebugClient5.TerminateCurrentProcess, dbgeng/IDebugClient2::TerminateCurrentProcess, dbgeng/IDebugClient3::TerminateCurrentProcess, dbgeng/IDebugClient4::TerminateCurrentProcess, dbgeng/IDebugClient5::TerminateCurrentProcess, debugger.terminatecurrentprocess
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
-	IDebugClient2.TerminateCurrentProcess
-	IDebugClient3.TerminateCurrentProcess
-	IDebugClient4.TerminateCurrentProcess
-	IDebugClient5.TerminateCurrentProcess
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugClient5::TerminateCurrentProcess method


## -description


The <b>TerminateCurrentProcess</b> method attempts to terminate the current process.


## -syntax


````
HRESULT TerminateCurrentProcess();
````


## -parameters






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



Only live user-modeprocesses are terminated by this method.  For other targets, the target is detached from the <a href="https://msdn.microsoft.com/fa52a1f0-9397-48a5-acbd-ce5347c0baef">debugger engine</a> without terminating.

For more information about creating and attaching to live user-mode targets, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552020">Live User-Mode Targets</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537786">AbandonCurrentProcess</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540055">CreateProcessAndAttach2</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient4.md">IDebugClient4</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563855">.kill (Kill Process)</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff558867">TerminateProcesses</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient3.md">IDebugClient3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538150">AttachProcess</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient2.md">IDebugClient2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541846">DetachCurrentProcess</a>



 

 


