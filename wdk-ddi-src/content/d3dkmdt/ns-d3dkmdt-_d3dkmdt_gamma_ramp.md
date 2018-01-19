---
UID: NS:d3dkmdt._D3DKMDT_GAMMA_RAMP
title: _D3DKMDT_GAMMA_RAMP
author: windows-driver-content
description: The D3DKMDT_GAMMA_RAMP structure contains descriptive information about a gamma lookup table and a pointer to the lookup table.
old-location: display\d3dkmdt_gamma_ramp.htm
old-project: display
ms.assetid: 3a875a1e-ef4f-4851-9329-f1fd2aca261f
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: _D3DKMDT_GAMMA_RAMP, D3DKMDT_GAMMA_RAMP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmdt.h
req.include-header: D3dkmdt.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: D3DKMDT_GAMMA_RAMP
req.alt-loc: d3dkmdt.h
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
req.typenames: D3DKMDT_GAMMA_RAMP
---

# _D3DKMDT_GAMMA_RAMP structure



## -description
The D3DKMDT_GAMMA_RAMP structure contains descriptive information about a gamma lookup table and a pointer to the lookup table.



## -syntax

````
typedef struct _D3DKMDT_GAMMA_RAMP {
  D3DDDI_GAMMARAMP_TYPE Type;
  SIZE_T                DataSize;
  union {
    D3DDDI_GAMMA_RAMP_RGB256x3x16   *pRgb256x3x16;
    D3DDDI_GAMMA_RAMP_DXGI_1        *pDxgi1;
    D3DDDI_3x4_COLORSPACE_TRANSFORM *p3x4;
    VOID                            *pRaw;
  } Data;
} D3DKMDT_GAMMA_RAMP;
````


## -struct-fields

### -field Type

A <a href="..\d3dukmdt\ne-d3dukmdt-_d3dddi_gammaramp_type.md">D3DDDI_GAMMARAMP_TYPE</a> enumerator that specifies the format of the lookup table. 


### -field DataSize

The size, in bytes, of the lookup table pointed to by <i>Data</i>.


### -field Data

[in] A union that contains one of the following ways to access the lookup table data depending on the value in the Type member:


### -field pRgb256x3x16

If <b>Type</b> is equal to D3DDDI_GAMMARAMP_RGB256x3x16, this member is a pointer to a <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_gamma_ramp_rgb256x3x16.md">D3DDDI_GAMMA_RAMP_RGB256x3x16</a> structure that contains the lookup table. 


### -field pDxgi1

If <b>Type</b> is equal to D3DDDI_GAMMARAMP_DXGI_1, this member is a pointer to a <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_gamma_ramp_dxgi_1.md">D3DDDI_GAMMA_RAMP_DXGI_1</a> structure that contains the lookup table. 


### -field p3x4

Pointer to a D3DDDI_3x4_COLORSPACE_TRANSFORM which describes the 3 by 4 matrix colorspace transform to be applied.


### -field pRaw

This member provides an alternative way to access the lookup table data. For example, for copying the lookup table, VOID* might be more convenient than D3DDDI_GAMMA_RAMP_RGB256x3x16.

</dd>
</dl>

## -remarks
The <b>GammaRamp</b> member of the <a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_vidpn_present_path.md">D3DKMDT_VIDPN_PRESENT_PATH</a> structure is a D3DKMDT_GAMMA_RAMP structure.</p>