---
UID: NS:d3dumddi._D3DDDIARG_CREATEPIXELSHADER
title: "_D3DDDIARG_CREATEPIXELSHADER"
author: windows-driver-content
description: The D3DDDIARG_CREATEPIXELSHADER structure specifies a shader handle to associate with pixel shader code.
old-location: display\d3dddiarg_createpixelshader.htm
old-project: display
ms.assetid: dc7baff1-7e74-4666-805b-33b524c89c1d
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3DDDIARG_CREATEPIXELSHADER, D3DDDIARG_CREATEPIXELSHADER structure [Display Devices], UMDisplayDriver_param_Structs_c1c78eaf-3eb9-4518-9b3c-f3fd5d6ce1f7.xml, _D3DDDIARG_CREATEPIXELSHADER, d3dumddi/D3DDDIARG_CREATEPIXELSHADER, display.d3dddiarg_createpixelshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Windows
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
-	HeaderDef
api_location:
-	d3dumddi.h
api_name:
-	D3DDDIARG_CREATEPIXELSHADER
product: Windows
targetos: Windows
req.typenames: D3DDDIARG_CREATEPIXELSHADER
---

# _D3DDDIARG_CREATEPIXELSHADER structure


## -description


The D3DDDIARG_CREATEPIXELSHADER structure specifies a shader handle to associate with pixel shader code.


## -syntax


````
typedef struct _D3DDDIARG_CREATEPIXELSHADER {
  UINT   CodeSize;
  HANDLE ShaderHandle;
} D3DDDIARG_CREATEPIXELSHADER;
````


## -struct-fields




### -field CodeSize

[in] The size, in bytes, of the pixel shader code that is passed in the <i>pCode</i> parameter in a call to the user-mode display driver's <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_createpixelshader.md">CreatePixelShader</a> function.


### -field ShaderHandle

[out] A handle to the pixel shader code.


## -remarks



For more information about programming shader assemblers, see <a href="https://msdn.microsoft.com/c858766c-b414-4971-b4d9-23ec94aca8ea">Processing Shader Codes</a>.




## -see-also

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_createpixelshader.md">CreatePixelShader</a>



 

 


