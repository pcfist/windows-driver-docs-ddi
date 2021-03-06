---
UID: NC:d3dumddi.PFND3DDDI_SETDEPTHSTENCIL
title: PFND3DDDI_SETDEPTHSTENCIL
author: windows-driver-content
description: The SetDepthStencil function sets the depth buffer in the driver's context.
old-location: display\setdepthstencil.htm
old-project: display
ms.assetid: 7c4b01c8-2376-4956-9b18-649647c19b2b
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3DDDI_SETDEPTHSTENCIL, SetDepthStencil, SetDepthStencil callback function [Display Devices], UserModeDisplayDriver_Functions_0279a98e-e1a5-4e33-8ced-9ac07e5e2921.xml, d3dumddi/SetDepthStencil, display.setdepthstencil
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
-	d3dumddi.h
api_name:
-	SetDepthStencil
product: Windows
targetos: Windows
req.typenames: DXGK_PTE
---

# PFND3DDDI_SETDEPTHSTENCIL callback


## -description


The <i>SetDepthStencil</i> function sets the depth buffer in the driver's context. 


## -prototype


````
PFND3DDDI_SETDEPTHSTENCIL SetDepthStencil;

__checkReturn HRESULT APIENTRY SetDepthStencil(
  _In_       HANDLE                    hDevice,
  _In_ const D3DDDIARG_SETDEPTHSTENCIL *pData
)
{ ... }
````


## -parameters




### -param hDevice [in]

 A handle to the display device (graphics context).


### -param *








#### - pData [in]

 A pointer to a <a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_setdepthstencil.md">D3DDDIARG_SETDEPTHSTENCIL</a> structure that specifies the depth buffer.


## -returns



<i>SetDepthStencil</i> returns S_OK or an appropriate error result if the depth buffer is not successfully set.




## -remarks



The user-mode display driver should store the depth buffer in the driver's context when the Microsoft Direct3D runtime calls <i>SetDepthStencil</i>. 




## -see-also

<a href="..\d3dumddi\ns-d3dumddi-_d3dddi_devicefuncs.md">D3DDDI_DEVICEFUNCS</a>



<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_setdepthstencil.md">D3DDDIARG_SETDEPTHSTENCIL</a>



 

 


