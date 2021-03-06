---
UID: NC:d3d12umddi.PFND3D12DDI_RESOURCEBARRIER_0022
title: PFND3D12DDI_RESOURCEBARRIER_0022
author: windows-driver-content
description: The pfnResourceBarrier callback function supports resource barriers.
old-location: display\pfnd3d12ddi_resourcebarrier_0022.htm
old-project: display
ms.assetid: AD42B7FC-9928-4386-B3EB-C9F0302415DA
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D12DDI_RESOURCEBARRIER_0022, d3d12umddi/pfnResourceBarrier, display.pfnd3d12ddi_resourcebarrier_0022, pfnResourceBarrier, pfnResourceBarrier callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d12umddi.h
req.include-header: D3d12umddi.h
req.target-type: Windows
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
-	D3d12umddi.h
api_name:
-	pfnResourceBarrier
product: Windows
targetos: Windows
req.typenames: D3D11_1DDI_GETCAPTUREHANDLEDATA
---

# PFND3D12DDI_RESOURCEBARRIER_0022 callback


## -description


The <i>pfnResourceBarrier</i> callback function supports resource barriers. 


## -prototype


````
PFND3D12DDI_RESOURCEBARRIER_0022 pfnResourceBarrier;

VOID APIENTRY* pfnResourceBarrier(
             D3D12DDI_HCOMMANDLIST                            hDrvCommandList,
             UINT                                             Count,
  _In_ const _reads_(Count) D3D12DDIARG_RESOURCE_BARRIER_0022 *ResourceBarrier
)
{ ... }
````


## -parameters




### -param D3D12DDI_HCOMMANDLIST


### -param Count

Specifies a count.


### -param *








#### - ResourceBarrier [in]

A pointer to a resource barrier as a <a href="..\d3d12umddi\ns-d3d12umddi-d3d12ddiarg_resource_barrier_0022.md">D3D12DDIARG_RESOURCE_BARRIER_0022</a> structure. 


#### - hDrvCommandList

The handle of a command list.


## -returns



This callback function does not return a value.




## -remarks



Access this callback function by using a command list functions structure, such as the <b>D3D12DDI_COMMAND_LIST_FUNCS_VIDEO_0020</b> structure. 




## -see-also

<a href="..\d3d12umddi\ns-d3d12umddi-d3d12ddiarg_resource_barrier_0022.md">D3D12DDIARG_RESOURCE_BARRIER_0022</a>



 

 


