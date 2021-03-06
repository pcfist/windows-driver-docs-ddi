---
UID: NC:video.PEXECUTE_DMA
title: PEXECUTE_DMA
author: windows-driver-content
description: HwVidExecuteDma is a miniport driver-implemented callback routine that is responsible for retrieving physical address/length pairs from a scatter/gather list, and for programming the hardware to start the actual DMA transfer.
old-location: display\hwvidexecutedma.htm
old-project: display
ms.assetid: 262c4b9b-fdca-4899-a635-fb273bbf4cc8
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: HwVidExecuteDma, HwVidExecuteDma callback function [Display Devices], PEXECUTE_DMA, VideoMiniport_Functions_5819a796-9dfd-41fe-9158-6ec09ac14760.xml, display.hwvidexecutedma, video/HwVidExecuteDma
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: video.h
req.include-header: Video.h
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
-	UserDefined
api_location:
-	video.h
api_name:
-	HwVidExecuteDma
product: Windows
targetos: Windows
req.typenames: VHF_CONFIG, *PVHF_CONFIG
req.product: Windows 10 or later.
---

# PEXECUTE_DMA callback


## -description


<i>HwVidExecuteDma</i> is a miniport driver-implemented callback routine that is responsible for retrieving physical address/length pairs from a scatter/gather list, and for programming the hardware to start the actual DMA transfer.


## -prototype


````
PEXECUTE_DMA HwVidExecuteDma;

VOID HwVidExecuteDma(
   PVOID                   HwDeviceExtension,
   PVP_DMA_ADAPTER         VpDmaAdapter,
   PVP_SCATTER_GATHER_LIST SGList,
   PVOID                   Context
)
{ ... }
````


## -parameters




### -param HwDeviceExtension

Pointer to the miniport driver's per-adapter storage area. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff543119">Device Extensions</a>.


### -param VpDmaAdapter

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570570">VP_DMA_ADAPTER</a> structure that represents the bus-master adapter. This structure was returned by a call to <a href="..\video\nf-video-videoportgetdmaadapter.md">VideoPortGetDmaAdapter</a>.


### -param SGList

Pointer to a <a href="..\video\ns-video-_vp_scatter_gather_list.md">VP_SCATTER_GATHER_LIST</a> structure. The video port driver fills in the information in this structure, and passes this structure to the miniport driver.


### -param Context

Pointer to the driver-determined context passed in from <b>VideoPortStartDma</b>.


## -returns



None




## -remarks



This function is available in Windows XP and later.

If the miniport driver reports that the device does not support scatter/gather, there will be only a single element in the scatter/gather list passed to this routine. The scatter/gather list is valid until <a href="..\video\nf-video-videoportcompletedma.md">VideoPortCompleteDma</a> is called.

The last task that the video port driver's <b>VideoPortStartDma</b> function performs is to call the miniport driver's <i>HwVidExecuteDma</i> callback routine. It is this callback that actually carries out the DMA transfer operation.

<i>HwVidExecuteDma</i> must be in nonpaged memory and must not access any pageable code or data.




## -see-also

<a href="..\video\nf-video-videoportstartdma.md">VideoPortStartDma</a>



<a href="..\video\nf-video-videoportcompletedma.md">VideoPortCompleteDma</a>



<a href="..\video\ns-video-_vp_scatter_gather_list.md">VP_SCATTER_GATHER_LIST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570570">VP_DMA_ADAPTER</a>



<a href="..\video\nf-video-videoportgetdmaadapter.md">VideoPortGetDmaAdapter</a>



 

 


