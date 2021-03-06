---
UID: NC:d3d10umddi.PFND3D11_1DDI_GETVIDEOPROCESSORCUSTOMRATE
title: PFND3D11_1DDI_GETVIDEOPROCESSORCUSTOMRATE
author: windows-driver-content
description: Queries a custom frame rate that is associated with a rate conversion capability group.
old-location: display\getvideoprocessorcustomrate.htm
old-project: display
ms.assetid: 49aec00a-8d63-4ec9-966a-0826354fbbe0
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D11_1DDI_GETVIDEOPROCESSORCUSTOMRATE, d3d10umddi/pfnGetVideoProcessorCustomRate, display.getvideoprocessorcustomrate, pfnGetVideoProcessorCustomRate, pfnGetVideoProcessorCustomRate callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
-	D3d10umddi.h
api_name:
-	pfnGetVideoProcessorCustomRate
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11_1DDI_GETVIDEOPROCESSORCUSTOMRATE callback


## -description


Queries a custom frame rate that is associated with a rate conversion capability group. 


## -prototype


````
PFND3D11_1DDI_GETVIDEOPROCESSORCUSTOMRATE pfnGetVideoProcessorCustomRate;

VOID APIENTRY* pfnGetVideoProcessorCustomRate(
  _In_  D3D10DDI_HDEVICE                       hDevice,
  _In_  D3D11_1DDI_HVIDEOPROCESSORENUM         hProcessorEnum,
  _In_  UINT                                   RateConversionIndex,
  _In_  UINT                                   CustomRateIndex,
  _Out_ D3D11_1DDI_VIDEO_PROCESSOR_CUSTOM_RATE *pRate
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param D3D11_1DDI_HVIDEOPROCESSORENUM


### -param UINT


### -param *








#### - CustomRateIndex [in]

The zero-based index of the custom rate to query. For more information, see the Remarks section.


#### - RateConversionIndex [in]

The zero-based index of the frame-rate conversion capability group. For more information, see the Remarks section.


#### - hDevice [in]

A handle to the display device (graphics context).




#### - hProcessorEnum [in]

A handle to a video processor enumeration object that was created through a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessorenum.md">CreateVideoProcessorEnum</a> function.




#### - pRate [out]

A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_processor_custom_rate.md">D3D11_1DDI_VIDEO_PROCESSOR_CUSTOM_RATE</a> structure that contains the attributes of the specified custom rate.




## -returns



This callback function does not return a value.




## -remarks



The display miniport driver returns the maximum number of frame-rate conversion capabilities that it supports through the <b>RateConversionCapsCount</b> member of the <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_processor_caps.md">D3D11_1DDI_VIDEO_PROCESSOR_CAPS</a> structure. The driver returns a pointer to this structure through its <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_getvideoprocessorcaps.md">GetVideoProcessorCaps</a> function. In addition, the attributes of a frame-rate conversion capability group can be queried by calling the <b>GetVideoProcessorCaps</b> function.

The display miniport driver returns the maximum number of custom rates that it supports through the <b>CustomRateCount</b> member of the <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_processor_rate_conversion_caps.md">D3D11_1DDI_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure. The driver returns a pointer to this structure through its <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_getvideoprocessorcaps.md">GetVideoProcessorCaps</a> function. In addition, the attributes of a frame-rate conversion capability group can be queried by calling the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_getvideoprocessorrateconversioncaps.md">GetVideoProcessorRateConversionCaps</a> function.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_getvideoprocessorrateconversioncaps.md">GetVideoProcessorRateConversionCaps</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_getvideoprocessorcaps.md">GetVideoProcessorCaps</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessorenum.md">CreateVideoProcessorEnum</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_processor_caps.md">D3D11_1DDI_VIDEO_PROCESSOR_CAPS</a>



 

 


