---
UID: NC:d3d10umddi.PFND3D10DDI_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT
title: PFND3D10DDI_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT
author: windows-driver-content
description: The CreateGeometryShaderWithStreamOutput function creates a geometry shader with stream output.
old-location: display\creategeometryshaderwithstreamoutput.htm
old-project: display
ms.assetid: 6ad1573d-4377-4795-8511-5d6cae96ee4f
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CreateGeometryShaderWithStreamOutput, CreateGeometryShaderWithStreamOutput callback function [Display Devices], PFND3D10DDI_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT, UserModeDisplayDriverDx10_Functions_e7442d66-9ff1-4ac0-b72d-cf23a1f34017.xml, d3d10umddi/CreateGeometryShaderWithStreamOutput, display.creategeometryshaderwithstreamoutput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
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
-	d3d10umddi.h
api_name:
-	CreateGeometryShaderWithStreamOutput
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT callback


## -description


The <b>CreateGeometryShaderWithStreamOutput</b> function creates a geometry shader with stream output.


## -prototype


````
PFND3D10DDI_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT CreateGeometryShaderWithStreamOutput;

VOID APIENTRY CreateGeometryShaderWithStreamOutput(
  _In_       D3D10DDI_HDEVICE                                 hDevice,
  _In_ const D3D10DDIARG_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT *pCreateGeometryWithShaderOutput,
  _In_       D3D10DDI_HSHADER                                 hShader,
  _In_       D3D10DDI_HRTSHADER                               hRTShader,
  _In_ const D3D10DDIARG_STAGE_IO_SIGNATURES                  *pSignatures
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *








### -param D3D10DDI_HSHADER


### -param D3D10DDI_HRTSHADER


#### - hDevice [in]

 A handle to the display device (graphics context).


#### - hRTShader [in]

 A handle to the geometry shader with stream output that the driver should use anytime it calls back into the Direct3D runtime. 


#### - hShader [in]

 A handle to the driver's private data for the geometry shader with stream output. The driver returns the size, in bytes, of the memory region that the Microsoft Direct3D runtime must allocate for the private data from a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_calcprivategeometryshaderwithstreamoutput.md">CalcPrivateGeometryShaderWithStreamOutput</a> function. The handle is really just a pointer to a region of memory, the size of which the driver requested. The driver uses this region of memory to store internal data structures that are related to its shader object. 


#### - pCreateGeometryWithShaderOutput [in]

 A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddiarg_creategeometryshaderwithstreamoutput.md">D3D10DDIARG_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT</a> structure that describes the parameters that the user-mode display driver uses to create a geometry shader with stream output. 


#### - pSignatures [in]

 A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddiarg_stage_io_signatures.md">D3D10DDIARG_STAGE_IO_SIGNATURES</a> structure that makes up the shader's signature.


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the following Remarks section.




## -remarks



The driver can pass E_OUTOFMEMORY (if the driver runs out of memory) or D3DDDIERR_DEVICEREMOVED (if the device has been removed) in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function. The Direct3D runtime will determine that any other errors are critical. If the driver passes any errors, including D3DDDIERR_DEVICEREMOVED, the Direct3D runtime will determine that the handle is invalid; therefore, the runtime will not call the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroyshader.md">DestroyShader</a> function to destroy the handle that the <i>hShader</i> parameter specifies.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroyshader.md">DestroyShader</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddiarg_stage_io_signatures.md">D3D10DDIARG_STAGE_IO_SIGNATURES</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_calcprivategeometryshaderwithstreamoutput.md">CalcPrivateGeometryShaderWithStreamOutput</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddiarg_creategeometryshaderwithstreamoutput.md">D3D10DDIARG_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_devicefuncs.md">D3D10DDI_DEVICEFUNCS</a>



 

 


