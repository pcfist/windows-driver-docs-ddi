---
UID: NE:d3dumddi._DXVAHDDDI_BLT_STATE
title: "_DXVAHDDDI_BLT_STATE"
author: windows-driver-content
description: The DXVAHDDDI_BLT_STATE enumeration contains values that identify the bit-block transfer (bitblt) state data for a video processor.
old-location: display\dxvahdddi_blt_state.htm
old-project: display
ms.assetid: c17cf4bd-34f0-4bc6-9efc-2f9a649b5438
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXVA2_Structs_2d8a894a-25be-49c1-bebe-82c7403007db.xml, DXVAHDDDI_BLT_STATE, DXVAHDDDI_BLT_STATE enumeration [Display Devices], DXVAHDDDI_BLT_STATE_ALPHA_FILL, DXVAHDDDI_BLT_STATE_BACKGROUND_COLOR, DXVAHDDDI_BLT_STATE_CONSTRICTION, DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE, DXVAHDDDI_BLT_STATE_PRIVATE, DXVAHDDDI_BLT_STATE_TARGET_RECT, _DXVAHDDDI_BLT_STATE, d3dumddi/DXVAHDDDI_BLT_STATE, d3dumddi/DXVAHDDDI_BLT_STATE_ALPHA_FILL, d3dumddi/DXVAHDDDI_BLT_STATE_BACKGROUND_COLOR, d3dumddi/DXVAHDDDI_BLT_STATE_CONSTRICTION, d3dumddi/DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE, d3dumddi/DXVAHDDDI_BLT_STATE_PRIVATE, d3dumddi/DXVAHDDDI_BLT_STATE_TARGET_RECT, display.dxvahdddi_blt_state
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Windows
req.target-min-winverclnt: DXVAHDDDI_BLT_STATE is supported beginning with the Windows 7 operating system.
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
-	DXVAHDDDI_BLT_STATE
product: Windows
targetos: Windows
req.typenames: DXVAHDDDI_BLT_STATE
---

# _DXVAHDDDI_BLT_STATE enumeration


## -description


The DXVAHDDDI_BLT_STATE enumeration contains values that identify the bit-block transfer (bitblt) state data for a video processor. 


## -syntax


````
typedef enum _DXVAHDDDI_BLT_STATE { 
  DXVAHDDDI_BLT_STATE_TARGET_RECT         = 0,
  DXVAHDDDI_BLT_STATE_BACKGROUND_COLOR    = 1,
  DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE  = 2,
  DXVAHDDDI_BLT_STATE_ALPHA_FILL          = 3,
  DXVAHDDDI_BLT_STATE_CONSTRICTION        = 4,
  DXVAHDDDI_BLT_STATE_PRIVATE             = 1000
} DXVAHDDDI_BLT_STATE;
````


## -enum-fields




### -field DXVAHDDDI_BLT_STATE_TARGET_RECT

The bitblt state data specifies the target rectangle of the output in a <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_target_rect_data.md">DXVAHDDDI_BLT_STATE_TARGET_RECT_DATA</a> structure. 


### -field DXVAHDDDI_BLT_STATE_BACKGROUND_COLOR

The bitblt state data specifies the background color to fill in the target rectangle of the output in a <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_background_color_data.md">DXVAHDDDI_BLT_STATE_BACKGROUND_COLOR_DATA</a> structure. 


### -field DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE

The bitblt state data specifies the color space of the output in a <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_output_color_space_data.md">DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA</a> structure. 


### -field DXVAHDDDI_BLT_STATE_ALPHA_FILL

The bitblt state data specifies the alpha-fill mode of the output in a <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_alpha_fill_data.md">DXVAHDDDI_BLT_STATE_ALPHA_FILL_DATA</a> structure. 


### -field DXVAHDDDI_BLT_STATE_CONSTRICTION

The bitblt state data specifies the down sampling of the output in a <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_constriction_data.md">DXVAHDDDI_BLT_STATE_CONSTRICTION_DATA</a> structure. 


### -field DXVAHDDDI_BLT_STATE_PRIVATE

The bitblt state data specifies the private parameters in a <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_private_data.md">DXVAHDDDI_BLT_STATE_PRIVATE_DATA</a> structure. 


## -remarks



A DXVAHDDDI_BLT_STATE-typed value, which is specified in the <b>State</b> member of the <a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_dxvahd_setvideoprocessbltstate.md">D3DDDIARG_DXVAHD_SETVIDEOPROCESSBLTSTATE</a> structure in a call to the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_dxvahd_setvideoprocessbltstate.md">SetVideoProcessBltState</a> function, sets the state of a bitblt for a video processor. Bitblt data that corresponds to the supplied DXVAHDDDI_BLT_STATE-typed value is pointed to by the <b>pData</b> member of D3DDDIARG_DXVAHD_SETVIDEOPROCESSBLTSTATE. 




## -see-also

<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_dxvahd_setvideoprocessbltstate.md">D3DDDIARG_DXVAHD_SETVIDEOPROCESSBLTSTATE</a>



<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_constriction_data.md">DXVAHDDDI_BLT_STATE_CONSTRICTION_DATA</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_dxvahd_setvideoprocessbltstate.md">SetVideoProcessBltState</a>



<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_output_color_space_data.md">DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA</a>



<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_target_rect_data.md">DXVAHDDDI_BLT_STATE_TARGET_RECT_DATA</a>



<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_background_color_data.md">DXVAHDDDI_BLT_STATE_BACKGROUND_COLOR_DATA</a>



<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_private_data.md">DXVAHDDDI_BLT_STATE_PRIVATE_DATA</a>



<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_blt_state_alpha_fill_data.md">DXVAHDDDI_BLT_STATE_ALPHA_FILL_DATA</a>



 

 


