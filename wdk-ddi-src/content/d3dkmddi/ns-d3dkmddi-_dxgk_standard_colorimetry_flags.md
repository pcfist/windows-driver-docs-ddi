---
UID: NS:d3dkmddi._DXGK_STANDARD_COLORIMETRY_FLAGS
title: "_DXGK_STANDARD_COLORIMETRY_FLAGS"
author: windows-driver-content
description: Flags describing standard colorimetry and related support.
old-location: display\dxgk_standard_colorimetry_flags.htm
old-project: display
ms.assetid: 473C5D7B-8FDD-49E2-981A-00ECCA67671A
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PDXGK_STANDARD_COLORIMETRY_FLAGS, DXGK_STANDARD_COLORIMETRY_FLAGS, DXGK_STANDARD_COLORIMETRY_FLAGS union [Display Devices], PDXGK_STANDARD_COLORIMETRY_FLAGS, PDXGK_STANDARD_COLORIMETRY_FLAGS union pointer [Display Devices], _DXGK_STANDARD_COLORIMETRY_FLAGS, d3dkmddi/DXGK_STANDARD_COLORIMETRY_FLAGS, d3dkmddi/PDXGK_STANDARD_COLORIMETRY_FLAGS, display.dxgk_standard_colorimetry_flags"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmddi.h
req.include-header: 
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3dkmddi.h
api_name:
-	DXGK_STANDARD_COLORIMETRY_FLAGS
product: Windows
targetos: Windows
req.typenames: DXGK_STANDARD_COLORIMETRY_FLAGS, *PDXGK_STANDARD_COLORIMETRY_FLAGS
---

# _DXGK_STANDARD_COLORIMETRY_FLAGS structure


## -description


Flags describing standard colorimetry and related support.


## -syntax


````
typedef union _DXGK_STANDARD_COLORIMETRY_FLAGS {
  struct {
    UINT BT2020YCC  :1;
    UINT BT2020RGB  :1;
    UINT ST2084  :1;
    UINT Reserved  :29;
  };
  ULONG Value;
} DXGK_STANDARD_COLORIMETRY_FLAGS, *PDXGK_STANDARD_COLORIMETRY_FLAGS;
````


## -struct-fields




### -field Value

The combined value that is operated on.


#### - BT2020RGB

Flag which indicates device support for the color space defined by BT.2020 using an RGB signal format.


#### - BT2020YCC

Flag which indicates device support for the color space defined by BT.2020 using a YCC signal format.


#### - Reserved

This value is reserved for system use.


#### - ST2084

Flag which indicates device support for the ST.2084 EOTF.

