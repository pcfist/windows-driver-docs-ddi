---
UID: NF:wdm.ExInterlockedPopEntrySList
title: ExInterlockedPopEntrySList macro
author: windows-driver-content
description: The ExInterlockedPopEntrySList routine atomically removes the first entry from a sequenced singly linked list.
old-location: kernel\exinterlockedpopentryslist.htm
old-project: kernel
ms.assetid: dbea07e1-f987-45d8-91cb-bde45df0672b
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: ExInterlockedPopEntrySList, ExInterlockedPopEntrySList routine [Kernel-Mode Driver Architecture], k102_fc9dbcb7-5cb0-405c-9a65-f7d6b60d2fee.xml, kernel.exinterlockedpopentryslist, wdm/ExInterlockedPopEntrySList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.irql: Any level (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	ExInterlockedPopEntrySList
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# ExInterlockedPopEntrySList macro


## -description


The <b>ExInterlockedPopEntrySList</b> routine atomically removes the first entry from a sequenced singly linked list.


## -syntax


````
PSLIST_ENTRY ExInterlockedPopEntrySList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PKSPIN_LOCK   Lock
);
````


## -parameters




### -param Head

TBD


### -param Lock [in, out]

A pointer to a <b>KSPIN_LOCK</b> structure that serves as the spin lock used to synchronize access to the list. The storage for the spin lock must be resident and must have been initialized by calling <a href="..\wdm\nf-wdm-keinitializespinlock.md">KeInitializeSpinLock</a>. You must use this spin lock only with the <b>ExInterlocked<i>Xxx</i>List</b> routines.


#### - ListHead [in, out]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563810">SLIST_HEADER</a> structure that serves as the header for the sequenced singly linked list. <i>ListHead</i> must have been initialized by calling <a href="..\wdm\nf-wdm-initializeslisthead.md">ExInitializeSListHead</a>.


## -remarks



For more information about using this routine to implement a sequenced singly linked list, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563802">Singly and Doubly Linked Lists</a>. 

On Windows 2000, drivers must use the <b>-D_WIN2K_COMPAT_SLIST_USAGE</b> switch to successfully link code that uses <b>ExInterlockedPopEntrySList</b>.

<b>ExInterlockedPopEntrySList</b> can be called at any IRQL. The storage for the <i>ListHead</i> parameter must be resident at all IRQLs.




## -see-also

<a href="..\wdm\nf-wdm-initializeslisthead.md">ExInitializeSListHead</a>



<a href="..\wdm\nf-wdm-keinitializespinlock.md">KeInitializeSpinLock</a>



<a href="..\wdm\nf-wdm-exinterlockedpushentryslist.md">ExInterlockedPushEntrySList</a>



<a href="..\wdm\nf-wdm-exquerydepthslist.md">ExQueryDepthSList</a>



<a href="..\wdm\nf-wdm-exinterlockedremoveheadlist.md">ExInterlockedRemoveHeadList</a>



 

 


