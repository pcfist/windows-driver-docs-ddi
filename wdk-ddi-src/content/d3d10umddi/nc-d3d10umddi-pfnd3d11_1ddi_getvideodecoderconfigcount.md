---
UID: NC:d3d10umddi.PFND3D11_1DDI_GETVIDEODECODERCONFIGCOUNT
title: PFND3D11_1DDI_GETVIDEODECODERCONFIGCOUNT
author: windows-driver-content
description: Queries the number of video decoder configurations that are supported by the display miniport driver for the specified decoder operation.
old-location: display\getvideodecoderconfigcount.htm
old-project: display
ms.assetid: 5b4cc185-8579-4c13-932f-23065697c4ee
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D11_1DDI_GETVIDEODECODERCONFIGCOUNT, d3d10umddi/pfnGetVideoDecoderConfigCount, display.getvideodecoderconfigcount, pfnGetVideoDecoderConfigCount, pfnGetVideoDecoderConfigCount callback function [Display Devices]
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
-	pfnGetVideoDecoderConfigCount
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11_1DDI_GETVIDEODECODERCONFIGCOUNT callback


## -description


Queries the number of video decoder configurations that are supported by the display miniport driver for the specified decoder operation.


## -prototype


````
PFND3D11_1DDI_GETVIDEODECODERCONFIGCOUNT pfnGetVideoDecoderConfigCount;

VOID APIENTRY* pfnGetVideoDecoderConfigCount(
  _In_        D3D10DDI_HDEVICE              hDevice,
  _In_  const D3D11_1DDI_VIDEO_DECODER_DESC *pDecodeDesc,
  _Out_       UINT                          *pConfigCount
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *








#### - hDevice [in]

A handle to the display device (graphics context).




#### - pConfigCount [out]

A pointer to a UINT value that specifies the maximum number of decoder configurations that are supported.


#### - pDecodeDesc [in]

A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_decoder_desc.md">D3D11_1DDI_VIDEO_DECODER_DESC</a> structure that specifies the video decoder operation.


## -returns



This callback function does not return a value.




## -remarks



The Microsoft Direct3D runtime verifies that the <i>pDecodeDesc</i>  parameter data is valid before it calls the <b>GetVideoDecoderConfigCount</b> function.




## -see-also

<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_decoder_desc.md">D3D11_1DDI_VIDEO_DECODER_DESC</a>



 

 


