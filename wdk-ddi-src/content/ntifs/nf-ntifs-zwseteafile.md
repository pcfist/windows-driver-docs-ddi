---
UID: NF:ntifs.ZwSetEaFile
title: ZwSetEaFile function
author: windows-driver-content
description: The ZwSetEaFile routine sets extended-attribute (EA) values for a file.
old-location: kernel\zwseteafile.htm
old-project: kernel
ms.assetid: e791900a-06a8-4c8b-8ca8-c4e73d94f609
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: ZwSetEaFile, ZwSetEaFile routine [Kernel-Mode Driver Architecture], kernel.zwseteafile, ntifs/ZwSetEaFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: FltKernel.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000   and later versions of the Windows operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	ZwSetEaFile
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# ZwSetEaFile function


## -description


The <b>ZwSetEaFile</b> routine sets extended-attribute (EA) values for a file.


## -syntax


````
NTSTATUS ZwSetEaFile(
  _In_  HANDLE           FileHandle,
  _Out_ PIO_STATUS_BLOCK IoStatusBlock,
  _In_  PVOID            Buffer,
  _In_  ULONG            Length
);
````


## -parameters




### -param FileHandle [in]

The handle for the file on which the operation is to be performed.


### -param IoStatusBlock [out]

A pointer to an <a href="..\wudfwdm\ns-wudfwdm-_io_status_block.md">IO_STATUS_BLOCK</a> structure that receives the final completion status and other information about the requested operation.


### -param Buffer [in]

A pointer to a caller-supplied, <a href="..\wdm\ns-wdm-_file_full_ea_information.md">FILE_FULL_EA_INFORMATION</a>-structured input buffer that contains the extended attribute values to be set. 


### -param Length [in]

Length, in bytes, of the buffer that the <i>Buffer</i> parameter points to.


## -returns



<b>ZwSetEaFile</b> returns STATUS_SUCCESS or an appropriate NTSTATUS value such as the following:

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>STATUS_EA_LIST_INCONSISTENT</dt>
</dl>
</td>
<td width="60%">
The EaList parameter is not formatted correctly. This is an error code.

</td>
</tr>
</table>
 




## -see-also

<a href="..\ntifs\nf-ntifs-zwqueryeafile.md">ZwQueryEaFile</a>



<a href="..\wdm\ns-wdm-_file_full_ea_information.md">FILE_FULL_EA_INFORMATION</a>



 

 


