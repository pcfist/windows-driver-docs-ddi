---
UID: NF:ntddk.IoIsFileObjectIgnoringSharing
title: IoIsFileObjectIgnoringSharing function
author: windows-driver-content
description: The IoIsFileObjectIgnoringSharing routine determines if a file object is set with the option to ignore file sharing access checks.
old-location: ifsk\ioisfileobjectignoringsharing.htm
old-project: ifsk
ms.assetid: 1398056B-6AC3-4F92-8981-58C193907D6F
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: IoIsFileObjectIgnoringSharing, IoIsFileObjectIgnoringSharing routine [Installable File System Drivers], ifsk.ioisfileobjectignoringsharing, ntddk/IoIsFileObjectIgnoringSharing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntddk.h
req.include-header: Ntddk.h, Ntifs.h, Fltkernel.h
req.target-type: Universal
req.target-min-winverclnt: This routine is available starting with Windows Vista.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: Any
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	IoIsFileObjectIgnoringSharing
product: Windows
targetos: Windows
req.typenames: WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---

# IoIsFileObjectIgnoringSharing function


## -description


The <b>IoIsFileObjectIgnoringSharing</b> routine determines if a file object is set with the option to ignore file  sharing access checks.


## -syntax


````
BOOLEAN IoIsFileObjectIgnoringSharing(
   PFILE_OBJECT FileObject
);
````


## -parameters




### -param FileObject

Pointer to a file object for the file.


## -returns



<b>TRUE</b> if file sharing access checks are ignored. Otherwise, <b>FALSE</b>.




## -see-also

<a href="..\ntddk\nf-ntddk-iosetfileobjectignoresharing.md">IoSetFileObjectIgnoreSharing</a>



 

 


