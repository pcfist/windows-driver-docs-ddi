---
UID: NF:miniport.READ_REGISTER_BUFFER_ULONG
title: READ_REGISTER_BUFFER_ULONG function
author: windows-driver-content
description: The READ_REGISTER_BUFFER_ULONG routine reads a number of ULONG values from the specified register address into a buffer.
old-location: kernel\read_register_buffer_ulong.htm
old-project: kernel
ms.assetid: a80d361e-81d3-483c-8ddb-d5e5a69c8ba4
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: READ_REGISTER_BUFFER_ULONG, READ_REGISTER_BUFFER_ULONG routine [Kernel-Mode Driver Architecture], k103_8349c675-ef3b-441a-b11c-730cc43ee09a.xml, kernel.read_register_buffer_ulong, wdm/READ_REGISTER_BUFFER_ULONG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: miniport.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h, Wudfwdm.h
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
-	READ_REGISTER_BUFFER_ULONG
product: Windows
targetos: Windows
req.typenames: MEMORY_CACHING_TYPE
---

# READ_REGISTER_BUFFER_ULONG function


## -description


The <b>READ_REGISTER_BUFFER_ULONG</b> routine reads a number of ULONG values from the specified register address into a buffer. 


## -syntax


````
VOID READ_REGISTER_BUFFER_ULONG(
  _In_  PULONG Register,
  _Out_ PULONG Buffer,
  _In_  ULONG  Count
);
````


## -parameters




### -param Register [in]

Pointer to the register, which must be a mapped range in memory space.


### -param Buffer [out]

Pointer to a buffer into which an array of ULONG values is read.


### -param Count [in]

Specifies the number of ULONG values to be read into the buffer. 


## -returns



None




## -remarks



The size of the buffer must be large enough to contain at least the specified number of ULONG values.

Callers of <b>READ_REGISTER_BUFFER_ULONG</b> can be running at any IRQL, assuming the <i>Buffer</i> is resident and the <i>Register</i> is resident, mapped device memory.



