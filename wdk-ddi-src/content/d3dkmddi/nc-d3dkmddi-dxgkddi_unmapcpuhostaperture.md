---
UID: NC:d3dkmddi.DXGKDDI_UNMAPCPUHOSTAPERTURE
title: DXGKDDI_UNMAPCPUHOSTAPERTURE
author: windows-driver-content
description: DxgkDdiUnmapCpuHostAperture is used to unmap a previously mapped range of the CPU host aperture.
old-location: display\dxgkddiunmapcpuhostaperture.htm
old-project: display
ms.assetid: AFE6B92F-49DB-47F9-90BC-F75B5F37178D
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGKDDI_UNMAPCPUHOSTAPERTURE, DxgkDdiUnmapCpuHostAperture, DxgkDdiUnmapCpuHostAperture callback function [Display Devices], d3dkmddi/DxgkDdiUnmapCpuHostAperture, display.dxgkddiunmapcpuhostaperture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
-	d3dkmddi.h
api_name:
-	DxgkDdiUnmapCpuHostAperture
product: Windows
targetos: Windows
req.typenames: DD_MULTISAMPLEQUALITYLEVELSDATA
---

# DXGKDDI_UNMAPCPUHOSTAPERTURE callback


## -description


<b>DxgkDdiUnmapCpuHostAperture</b> is used to unmap a previously mapped range of the CPU host aperture.


## -prototype


````
DXGKDDI_UNMAPCPUHOSTAPERTURE DxgkDdiUnmapCpuHostAperture;

NTSTATUS APIENTRY DxgkDdiUnmapCpuHostAperture(
   HANDLE                       hAdapter,
   DXGKARG_UNMAPCPUHOSTAPERTURE pArgs
)
{ ... }
````


## -parameters




### -param hAdapter

A handle to the display adapter.


### -param pArgs

A <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_unmapcpuhostaperture.md">DXGKARG_UNMAPCPUHOSTAPERTURE</a> structure that describes the operation.


## -returns




      Returns <b>STATUS_SUCCESS</b> if it succeeds. Otherwise, it returns one of the error codes defined in <b>Ntstatus.h</b>.




## -see-also

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_unmapcpuhostaperture.md">DXGKARG_UNMAPCPUHOSTAPERTURE</a>



 

 


