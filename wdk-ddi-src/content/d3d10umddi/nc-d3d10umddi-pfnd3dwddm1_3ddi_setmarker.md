---
UID: NC:d3d10umddi.PFND3DWDDM1_3DDI_SETMARKER
title: PFND3DWDDM1_3DDI_SETMARKER
author: windows-driver-content
description: Notifies the user-mode display driver that it must generate a new time stamp if any GPU work has completed since the last call to SetMarker.
old-location: display\setmarker.htm
old-project: display
ms.assetid: BE618B0C-18E7-4B2B-87EB-172DAD9BCE15
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3DWDDM1_3DDI_SETMARKER, SetMarker, SetMarker callback function [Display Devices], d3d10umddi/SetMarker, display.setmarker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8.1,WDDM 1.3 and later
req.target-min-winversvr: Windows Server 2012 R2
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
-	SetMarker
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3DWDDM1_3DDI_SETMARKER callback


## -description


Notifies the user-mode display driver that it must generate a new time stamp if any GPU work has completed since the last call to <i>SetMarker</i>.


## -prototype


````
PFND3DWDDM1_3DDI_SETMARKER SetMarker;

_Check_return_ HRESULT APIENTRY* SetMarker(
  _In_ D3D10DDI_HDEVICE hDevice
)
{ ... }
````


## -parameters




### -param hDevice [in]

A handle to the display device (graphics context).


## -returns




      Returns <b>S_OK</b> or an appropriate error result if the function does not complete successfully.




## -remarks



If the marker event type from the  <i>Type</i> parameter of the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3dwddm1_3ddi_setmarkermode.md">SetMarkerMode</a> function is not <b>D3DWDDM1_3DDI_MARKER_TYPE_NONE</b>, the user-mode display driver must perform this procedure with each call to <i>SetMarker</i>:

<ol>
<li>Increment the value of the <b>APISequenceNumber</b> member of the <a href="..\d3dumddi\ns-d3dumddi-d3dddicb_logumdmarker.md">D3DDDICB_LOGUMDMARKER</a> structure.</li>
<li>Determine which contexts associated with single-threaded device driver interface (DDI) render calls submitted work with the last call to <i>SetMarker</i>. For each such context:<ol>
<li>If the command buffer for the context is empty, do nothing.</li>
<li>Otherwise:<ul>
<li>Ensure that more memory is available in the context's history buffer. Flush the buffer if necessary.</li>
<li>Add another entry to the context's API sequence number buffer that contains the low 32 bits of the current <b>APISequenceNumber</b> value.</li>
<li>Sample and write out time stamps that are appropriate for the current marker event type.</li>
</ul>
</li>
<li>Update tracking data that will be used the next time that <i>SetMarker</i> is called.</li>
</ol>
</li>
</ol>



## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3dwddm1_3ddi_setmarkermode.md">SetMarkerMode</a>



 

 


