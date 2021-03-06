---
UID: NE:d3dkmdt._D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE
title: "_D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE"
author: windows-driver-content
description: The D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE enumeration indicates the pivot type in a call to DxgkDdiEnumVidPnCofuncModality.
old-location: display\d3dkmdt_enumcofuncmodality_pivot_type.htm
old-project: display
ms.assetid: ba99936a-e76a-4a34-b7cd-762a8f15732c
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE, D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE enumeration [Display Devices], D3DKMDT_EPT_NOPIVOT, D3DKMDT_EPT_ROTATION, D3DKMDT_EPT_SCALING, D3DKMDT_EPT_UNINITIALIZED, D3DKMDT_EPT_VIDPNSOURCE, D3DKMDT_EPT_VIDPNTARGET, DmEnums_5abafdb2-5a17-437b-b3e3-9c045c52d582.xml, _D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE, d3dkmdt/D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE, d3dkmdt/D3DKMDT_EPT_NOPIVOT, d3dkmdt/D3DKMDT_EPT_ROTATION, d3dkmdt/D3DKMDT_EPT_SCALING, d3dkmdt/D3DKMDT_EPT_UNINITIALIZED, d3dkmdt/D3DKMDT_EPT_VIDPNSOURCE, d3dkmdt/D3DKMDT_EPT_VIDPNTARGET, display.d3dkmdt_enumcofuncmodality_pivot_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dkmdt.h
req.include-header: D3dkmdt.h
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3dkmdt.h
api_name:
-	D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE
product: Windows
targetos: Windows
req.typenames: D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE
---

# _D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE enumeration


## -description


The D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE enumeration indicates the pivot type in a call to <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_enumvidpncofuncmodality.md">DxgkDdiEnumVidPnCofuncModality</a>.


## -syntax


````
typedef enum _D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE { 
  D3DKMDT_EPT_UNINITIALIZED  = 0,
  D3DKMDT_EPT_VIDPNSOURCE    = 1,
  D3DKMDT_EPT_VIDPNTARGET    = 2,
  D3DKMDT_EPT_SCALING        = 3,
  D3DKMDT_EPT_ROTATION       = 4,
  D3DKMDT_EPT_NOPIVOT        = 5
} D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE;
````


## -enum-fields




### -field D3DKMDT_EPT_UNINITIALIZED

Indicates that a variable of type D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE has not yet been assigned a meaningful value.


### -field D3DKMDT_EPT_VIDPNSOURCE

Indicates that a video present source is the pivot of the enumeration.


### -field D3DKMDT_EPT_VIDPNTARGET

Indicates that a video present target is the pivot of the enumeration.


### -field D3DKMDT_EPT_SCALING

Indicates that the scaling transformation is the pivot of the enumeration.


### -field D3DKMDT_EPT_ROTATION

Indicates that the rotatation transformation is the pivot of the enumeration.


### -field D3DKMDT_EPT_NOPIVOT

Indicates that the enumeration has no pivot.


## -remarks



The <b>EnumPivotType</b> member of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_enumvidpncofuncmodality.md">DXGKARG_ENUMVIDPNCOFUNCMODALITY</a> structure is a D3DKMDT_ENUMCOFUNCMODALITY_PIVOT_TYPE value.




## -see-also

<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_enumvidpncofuncmodality.md">DxgkDdiEnumVidPnCofuncModality</a>



 

 


