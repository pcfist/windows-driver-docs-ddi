---
UID: NC:d3d10umddi.PFND3D11_1DDI_CALCPRIVATESHADERSIZE
title: PFND3D11_1DDI_CALCPRIVATESHADERSIZE
author: windows-driver-content
description: Determines the size of the user-mode display driver's private region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for a shader.
old-location: display\calcprivateshadersize_d3d11_1_.htm
old-project: display
ms.assetid: e23c267f-41df-47a6-ae43-3bbcb48fd300
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CalcPrivateShaderSize(D3D11_1), CalcPrivateShaderSize(D3D11_1) callback function [Display Devices], PFND3D11_1DDI_CALCPRIVATESHADERSIZE, d3d10umddi/CalcPrivateShaderSize(D3D11_1), display.calcprivateshadersize_d3d11_1_, display.pfncalcprivateshadersize
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
-	CalcPrivateShaderSize(D3D11_1)
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11_1DDI_CALCPRIVATESHADERSIZE callback


## -description


Determines the size of the user-mode display driver's private region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for a shader.


## -prototype


````
PFND3D11_1DDI_CALCPRIVATESHADERSIZE CalcPrivateShaderSize(D3D11_1);

SIZE_T APIENTRY* CalcPrivateShaderSize(D3D11_1)(
             D3D10DDI_HDEVICE                  hDevice,
  _In_ const UINT                              *pShaderCode,
  _In_ const D3D11_1DDIARG_STAGE_IO_SIGNATURES *pSignatures
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *pShaderCode [in]

A pointer to an array of CONST UINT tokens that make up the shader code.


### -param *








#### - hDevice

A handle to the display device (graphics context).


#### - pSignatures [in]

A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddiarg_stage_io_signatures.md">D3D11_1DDIARG_STAGE_IO_SIGNATURES</a> structure that makes up the shader's signature.


## -returns



The size of the memory region that the driver requires for creating a shader.




## -see-also

<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddiarg_stage_io_signatures.md">D3D11_1DDIARG_STAGE_IO_SIGNATURES</a>



 

 


