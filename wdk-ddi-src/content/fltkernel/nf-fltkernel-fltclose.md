---
UID: NF:fltkernel.FltClose
title: FltClose function
author: windows-driver-content
description: FltClose closes a file handle that was opened by FltCreateFile or FltCreateFileEx.
old-location: ifsk\fltclose.htm
old-project: ifsk
ms.assetid: fd5967cc-fb30-4882-9567-4617b9f9e723
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: FltApiRef_a_to_d_f50e2397-1161-4e6e-9688-2baa417f6845.xml, FltClose, FltClose function [Installable File System Drivers], fltkernel/FltClose, ifsk.fltclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltkernel.h
req.include-header: Fltkernel.h
req.target-type: Universal
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
req.lib: FltMgr.lib
req.dll: Fltmgr.sys
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	fltmgr.sys
api_name:
-	FltClose
product: Windows
targetos: Windows
req.typenames: EXpsFontRestriction
---

# FltClose function


## -description


<b>FltClose</b> closes a file handle that was opened by <a href="..\fltkernel\nf-fltkernel-fltcreatefile.md">FltCreateFile</a> or <a href="..\fltkernel\nf-fltkernel-fltcreatefileex.md">FltCreateFileEx</a>. 


## -syntax


````
NTSTATUS FltClose(
  _In_ HANDLE FileHandle
);
````


## -parameters




### -param FileHandle [in]

Handle created by a successful call to <a href="..\fltkernel\nf-fltkernel-fltcreatefile.md">FltCreateFile</a> or <a href="..\fltkernel\nf-fltkernel-fltcreatefileex.md">FltCreateFileEx</a>. 


## -returns



<b>FltClose</b> returns STATUS_SUCCESS or an appropriate NTSTATUS value such as the following: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>FileHandle</i> was not a valid file handle. This is an error code. 

</td>
</tr>
</table>
 




## -remarks



<b>FltClose</b> is only for closing file handles opened by <a href="..\fltkernel\nf-fltkernel-fltcreatefile.md">FltCreateFile</a> or <a href="..\fltkernel\nf-fltkernel-fltcreatefileex.md">FltCreateFileEx</a>. It should not be used to close arbitrary handles. 




## -see-also

<a href="..\fltkernel\nf-fltkernel-fltcreatefileex.md">FltCreateFileEx</a>



<a href="..\fltkernel\nf-fltkernel-fltcreatefile.md">FltCreateFile</a>



<a href="..\wdm\nf-wdm-zwclose.md">ZwClose</a>



 

 


