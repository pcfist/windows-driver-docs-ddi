---
UID: NC:d3d10umddi.PFND3D11DDI_CREATEDOMAINSHADER
title: PFND3D11DDI_CREATEDOMAINSHADER
author: windows-driver-content
description: The CreateDomainShader function creates a domain shader.
old-location: display\createdomainshader.htm
old-project: display
ms.assetid: 534c292a-b3ef-41aa-868a-f5e57b90d789
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CreateDomainShader, CreateDomainShader callback function [Display Devices], PFND3D11DDI_CREATEDOMAINSHADER, UserModeDisplayDriverDx11_Functions_e9e86a57-1f64-42a8-a871-d3f42f1c6819.xml, d3d10umddi/CreateDomainShader, display.createdomainshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: CreateDomainShader is supported beginning with the Windows 7 operating system.
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
-	d3d10umddi.h
api_name:
-	CreateDomainShader
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11DDI_CREATEDOMAINSHADER callback


## -description


The <b>CreateDomainShader</b> function creates a domain shader.


## -prototype


````
PFND3D11DDI_CREATEDOMAINSHADER CreateDomainShader;

VOID APIENTRY CreateDomainShader(
  _In_       D3D10DDI_HDEVICE                       hDevice,
  _In_ const UINT                                   *pCode,
  _In_       D3D10DDI_HSHADER                       hShader,
  _In_       D3D10DDI_HRTSHADER                     hRTShader,
  _In_ const D3D11DDIARG_TESSELLATION_IO_SIGNATURES *pSignatures
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *pShaderCode


### -param D3D10DDI_HSHADER


### -param D3D10DDI_HRTSHADER


### -param *








#### - hDevice [in]

 A handle to the display device (graphics context).


#### - hRTShader [in]

 A handle to the domain shader that the driver should use when it calls back into the Direct3D runtime. 


#### - hShader [in]

 A handle to the driver's private data for the domain shader. The driver returns the size, in bytes, of the memory region that the Microsoft Direct3D runtime must allocate for the private data from a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11ddi_calcprivatetessellationshadersize.md">CalcPrivateTessellationShaderSize</a>  function. The handle is  just a pointer to a region of memory, the size of which the driver requested. The driver uses this region of memory to store internal data structures that are related to its tessellation-shader object. 


#### - pCode [in]

 An array of CONST UINT tokens that form the shader code. The first token in the shader code stream is always the version token. The next token in the stream is the length token that determines the end of the shader code stream. For more information about the format of Direct3D version 11 shader code, see the comments inside the <i>D3d11tokenizedprogramformat.hpp</i> header file that is included with the WDK. 


#### - pSignatures [in]

 A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddiarg_tessellation_io_signatures.md">D3D11DDIARG_TESSELLATION_IO_SIGNATURES</a> structure that forms the tessellation-shader's signature.


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the following Remarks section.




## -remarks



The driver can pass E_OUTOFMEMORY (if the driver runs out of memory) or D3DDDIERR_DEVICEREMOVED (if the device is removed) in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function. The Direct3D runtime determines that any other errors are critical. If the driver passes any errors, which includes D3DDDIERR_DEVICEREMOVED, the Direct3D runtime determines that the handle is invalid; therefore, the runtime does not call the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroyshader.md">DestroyShader</a> function to destroy the handle that the <i>hShader</i> parameter specifies.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroyshader.md">DestroyShader</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_devicefuncs.md">D3D11DDI_DEVICEFUNCS</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11ddi_calcprivatetessellationshadersize.md">CalcPrivateTessellationShaderSize</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddiarg_tessellation_io_signatures.md">D3D11DDIARG_TESSELLATION_IO_SIGNATURES</a>



 

 


