---
UID: NF:ntifs.FsRtlIncrementCcFastReadNotPossible
title: FsRtlIncrementCcFastReadNotPossible function
author: windows-driver-content
description: The FsRtlIncrementCcFastReadNotPossible routine increments the CcFastReadNotPossible performance counter in a per processor control block of cache manager system counters.
old-location: ifsk\fsrtlincrementccfastreadnotpossible.htm
old-project: ifsk
ms.assetid: 2e0ae5d1-5189-4f78-9729-9c1b9bbf046d
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: FsRtlIncrementCcFastReadNotPossible, FsRtlIncrementCcFastReadNotPossible routine [Installable File System Drivers], fsrtlref_7789e1c4-9ac3-48c7-9191-f5eba5f4e5e0.xml, ifsk.fsrtlincrementccfastreadnotpossible, ntifs/FsRtlIncrementCcFastReadNotPossible
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: This routine is available on Microsoft Windows XP and later.
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
req.irql: Any level
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	FsRtlIncrementCcFastReadNotPossible
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# FsRtlIncrementCcFastReadNotPossible function


## -description


The <b>FsRtlIncrementCcFastReadNotPossible</b> routine increments the CcFastReadNotPossible performance counter in a per processor control block of cache manager system counters.


## -syntax


````
VOID FsRtlIncrementCcFastReadNotPossible(
   VOID 
);
````


## -parameters








## -returns



This routine does not return a value.




## -remarks



<b>FsRtlIncrementCcFastReadNotPossible </b>increments the CcFastReadNotPossible performance counter in the per processor control block of cache manager system counters. This counter indicates that a fast I/O read operation (<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlcopyread~r7.md">FsRtlCopyRead</a>) was called, but fast I/O was not possible. This counter does not get incremented if fast I/O was not possible because the file resource could not be acquired for shared access. When the resource could not be acquired, the CcFastReadResourceMiss performance counter should be incremented. 

File system drivers should call this function to update the performance counter if the driver chooses to override the default fast I/O read handler.




## -see-also

<a href="..\ntifs\nf-ntifs-fsrtlincrementccfastreadwait.md">FsRtlIncrementCcFastReadWait</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlcopyread~r7.md">FsRtlCopyRead</a>



<a href="..\ntifs\nf-ntifs-fsrtlincrementccfastreadnowait.md">FsRtlIncrementCcFastReadNoWait</a>



<a href="..\ntifs\nf-ntifs-fsrtlincrementccfastreadresourcemiss.md">FsRtlIncrementCcFastReadResourceMiss</a>



 

 


