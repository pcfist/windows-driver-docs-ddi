---
UID: NC:srb.PHW_DMA_STARTED
title: PHW_DMA_STARTED
author: windows-driver-content
description: The PHW_DMA_STARTED routine prototype declares a SCSI miniport driver routine that starts DMA for subordinate DMA device.
old-location: storage\phw_dma_started.htm
old-project: storage
ms.assetid: 2f989c46-e90e-45e1-a520-98b05ff78e73
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "(*PHW_DMA_STARTED), (*PHW_DMA_STARTED) callback function [Storage Devices], ide_minikr_2e265b69-67af-449a-bfef-67fbd6694cba.xml, srb/(*PHW_DMA_STARTED), storage.phw_dma_started"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: srb.h
req.include-header: Storport.h, Srb.h, Storport.h
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
topictype:
-	APIRef
-	kbSyntax
apitype:
-	UserDefined
apilocation:
-	srb.h
apiname:
-	(*PHW_DMA_STARTED)
product: Windows
targetos: Windows
req.typenames: SPB_CONTROLLER_CONFIG, *PSPB_CONTROLLER_CONFIG
req.product: Windows 10 or later.
---

# PHW_DMA_STARTED callback


## -description


The PHW_DMA_STARTED routine prototype declares a SCSI miniport driver routine that starts DMA for subordinate DMA device. 


## -prototype


````
typedef VOID (*PHW_DMA_STARTED)(
  _In_ PVOID DeviceExtension 
);
````


## -parameters




### -param DeviceExtension [in]

Pointer to the miniport driver's per-HBA storage area. 


## -returns



None




## -remarks



If the HBA is a subordinate DMA device, the SCSI miniport driver's <a href="..\srb\nc-srb-phw_dma_started.md">HwScsiDmaStarted</a> routine is called after the OS-specific port driver has set up the system DMA controller for a DMA transfer.

Miniport drivers that work with the StorPort driver do not support adapters that require subordinate DMA. 




## -see-also

<a href="..\srb\nc-srb-phw_dma_started.md">HwScsiDmaStarted</a>



 

 


