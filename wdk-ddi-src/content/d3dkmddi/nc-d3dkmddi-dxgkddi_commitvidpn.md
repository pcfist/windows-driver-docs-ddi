---
UID: NC:d3dkmddi.DXGKDDI_COMMITVIDPN
title: DXGKDDI_COMMITVIDPN
author: windows-driver-content
description: The DxgkDdiCommitVidPn function makes a specified video present network (VidPN) active on a display adapter.
old-location: display\dxgkddicommitvidpn.htm
old-project: display
ms.assetid: 979b86e9-f3ff-4022-8c00-b6afc2b1f747
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGKDDI_COMMITVIDPN, DmFunctions_467cba1e-3eeb-4735-9fb3-46c8c737b48d.xml, DxgkDdiCommitVidPn, DxgkDdiCommitVidPn callback function [Display Devices], d3dkmddi/DxgkDdiCommitVidPn, display.dxgkddicommitvidpn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3dkmddi.h
api_name:
-	DxgkDdiCommitVidPn
product: Windows
targetos: Windows
req.typenames: DD_MULTISAMPLEQUALITYLEVELSDATA
---

# DXGKDDI_COMMITVIDPN callback


## -description


The <i>DxgkDdiCommitVidPn</i> function makes a specified video present network (VidPN) active on a display adapter.


## -prototype


````
DXGKDDI_COMMITVIDPN DxgkDdiCommitVidPn;

NTSTATUS APIENTRY DxgkDdiCommitVidPn(
  _In_ const HANDLE                    hAdapter,
  _In_ const DXGKARG_COMMITVIDPN CONST *pCommitVidPnArg
)
{ ... }
````


## -parameters




### -param hAdapter [in]

A handle to a context block associated with a display adapter. The display miniport driver previously provided this handle to the DirectX graphics kernel subsystem in the <i>MiniportDeviceContext</i> output parameter of the <a href="..\dispmprt\nc-dispmprt-dxgkddi_add_device.md">DxgkDdiAddDevice</a> function.


### -param pCommitVidPn








#### - pCommitVidPnArg [in]

A pointer to a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_commitvidpn.md">DXGKARG_COMMITVIDPN</a> structure that contains function arguments.


## -returns



<i>DxgkDdiCommitVidPn</i> returns one of the values in the following list. The VidPN referred to in the list is the VidPN represented by <i>pCommitVidPnArg</i>-&gt;<b>hFunctionalVidPn</b>.




## -remarks



For more information about how the display miniport driver should handle calls to <i>DxgkDdiCommitVidPn</i>, see <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_commitvidpn.md">DXGKARG_COMMITVIDPN</a>.

Beginning with Windows 8, if the display miniport driver sets the <b>SupportSmoothRotation</b> member of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a> structure, it must support updating the path rotation on the adapter using the <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_updateactivevidpnpresentpath.md">DxgkDdiUpdateActiveVidPnPresentPath</a> function. The driver must always be able to set the path rotation during a call to the <i>DxgkDdiCommitVidPn</i> function.




## -see-also

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a>



<a href="..\dispmprt\nc-dispmprt-dxgkddi_add_device.md">DxgkDdiAddDevice</a>



<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_commitvidpn.md">DXGKARG_COMMITVIDPN</a>



<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_updateactivevidpnpresentpath.md">DxgkDdiUpdateActiveVidPnPresentPath</a>



 

 


