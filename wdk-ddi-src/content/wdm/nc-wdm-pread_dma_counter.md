---
UID: NC:wdm.PREAD_DMA_COUNTER
title: PREAD_DMA_COUNTER
author: windows-driver-content
description: The ReadDmaCounter routine returns the number of bytes remaining to be transferred during the current subordinate DMA operation.
old-location: kernel\readdmacounter.htm
old-project: kernel
ms.assetid: c5a49bbd-ddb7-4faa-934a-d5846273d648
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: PREAD_DMA_COUNTER, ReadDmaCounter, ReadDmaCounter callback function [Kernel-Mode Driver Architecture], kdma_81865501-ca01-4f66-b2a9-da0493d72589.xml, kernel.readdmacounter, wdm/ReadDmaCounter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Desktop
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: IrqlDispatch
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	wdm.h
api_name:
-	ReadDmaCounter
product: Windows
targetos: Windows
req.typenames: WDI_TYPE_PMK_NAME, *PWDI_TYPE_PMK_NAME
req.product: Windows 10 or later.
---

# PREAD_DMA_COUNTER callback


## -description


The <b>ReadDmaCounter</b> routine returns the number of bytes remaining to be transferred during the current subordinate DMA operation.


## -prototype


````
PREAD_DMA_COUNTER ReadDmaCounter;

ULONG ReadDmaCounter(
  _In_ PDMA_ADAPTER DmaAdapter
)
{ ... }
````


## -parameters




### -param DmaAdapter [in]

Pointer to the adapter object previously returned by <a href="..\wdm\nf-wdm-iogetdmaadapter.md">IoGetDmaAdapter</a> representing the system DMA controller channel currently in use. 


## -returns



<b>ReadDmaCounter</b> returns the number of bytes remaining to be transferred in the current DMA operation.




## -remarks



<b>ReadDmaCounter</b>
           is not a system routine that can be called directly by name. This routine is callable only by pointer from the address returned in a 
          <a href="..\wdm\ns-wdm-_dma_operations.md">DMA_OPERATIONS</a>
           structure. Drivers obtain the address of this routine by calling <a href="..\wdm\nf-wdm-iogetdmaadapter.md">IoGetDmaAdapter</a>.

<b>ReadDmaCounter</b> can be called only by drivers of subordinate DMA devices. Usually, the caller is the driver of a subordinate device that uses a system DMA controller's autoinitialize mode. 




## -see-also

<a href="..\wdm\nc-wdm-pflush_adapter_buffers.md">FlushAdapterBuffers</a>



<a href="..\wdm\ns-wdm-_dma_adapter.md">DMA_ADAPTER</a>



<a href="..\wdm\nc-wdm-pmap_transfer.md">MapTransfer</a>



<a href="..\wdm\nf-wdm-iogetdmaadapter.md">IoGetDmaAdapter</a>



<a href="..\wdm\nc-wdm-pallocate_common_buffer.md">AllocateCommonBuffer</a>



 

 


