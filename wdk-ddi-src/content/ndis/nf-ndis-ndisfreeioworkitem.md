---
UID: NF:ndis.NdisFreeIoWorkItem
title: NdisFreeIoWorkItem function
author: windows-driver-content
description: NDIS drivers call the NdisFreeIoWorkItem function to free a specified work item.
old-location: netvista\ndisfreeioworkitem.htm
old-project: netvista
ms.assetid: ddc2f96b-fa2c-43c1-960f-7f8e06a5b22d
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: NdisFreeIoWorkItem, NdisFreeIoWorkItem function [Network Drivers Starting with Windows Vista], ndis/NdisFreeIoWorkItem, ndis_work_items_ref_50b3859f-f34b-4cae-b7ef-935f1aae82cb.xml, netvista.ndisfreeioworkitem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Universal
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: Init_NdisAllocateIoWorkItem, Irql_Miscellaneous_Function
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ndis.lib
req.dll: 
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	ndis.lib
-	ndis.dll
api_name:
-	NdisFreeIoWorkItem
product: Windows
targetos: Windows
req.typenames: NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---

# NdisFreeIoWorkItem function


## -description


NDIS drivers call the
  <b>NdisFreeIoWorkItem</b> function to free a specified work item.


## -syntax


````
VOID NdisFreeIoWorkItem(
  _In_ NDIS_HANDLE NdisIoWorkItemHandle
);
````


## -parameters




### -param NdisIoWorkItemHandle [in]

A handle to a private <b>NDIS_IO_WORKITEM</b> structure that was returned by a previous call to the 
     <a href="..\ndis\nf-ndis-ndisallocateioworkitem.md">
     NdisAllocateIoWorkItem</a> function.


## -returns



None




## -remarks



<b>NdisFreeIoWorkItem</b> calls 
    <a href="..\wdm\nf-wdm-iofreeworkitem.md">IoFreeWorkItem</a> to free the structure that is
    specified by the
    <i>NdisIoWorkItemHandle</i> parameter.




## -see-also

<a href="..\ndis\nf-ndis-ndisqueueioworkitem.md">NdisQueueIoWorkItem</a>



<a href="..\ndis\nf-ndis-ndisallocateioworkitem.md">NdisAllocateIoWorkItem</a>



<a href="https://msdn.microsoft.com/4f966ff3-2092-495f-863f-50f079085fa6">NDIS I/O Work Items</a>



<a href="..\wdm\nf-wdm-iofreeworkitem.md">IoFreeWorkItem</a>



 

 


