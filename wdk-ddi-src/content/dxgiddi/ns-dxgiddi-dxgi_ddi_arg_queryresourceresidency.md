---
UID: NS:dxgiddi.DXGI_DDI_ARG_QUERYRESOURCERESIDENCY
title: DXGI_DDI_ARG_QUERYRESOURCERESIDENCY
author: windows-driver-content
description: The DXGI_DDI_ARG_QUERYRESOURCERESIDENCY structure describes the residency status of a list of resources.
old-location: display\dxgi_ddi_arg_queryresourceresidency.htm
old-project: display
ms.assetid: 140a92a8-4b82-47d0-855c-6bc1f9a3d167
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGI_DDI_ARG_QUERYRESOURCERESIDENCY, DXGI_DDI_ARG_QUERYRESOURCERESIDENCY structure [Display Devices], UMDisplayDriver_Dx10param_Structs_c6e97d75-9ef8-4ae5-9b1f-c4a25234b906.xml, display.dxgi_ddi_arg_queryresourceresidency, dxgiddi/DXGI_DDI_ARG_QUERYRESOURCERESIDENCY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxgiddi.h
req.include-header: D3d10umddi.h
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
-	dxgiddi.h
api_name:
-	DXGI_DDI_ARG_QUERYRESOURCERESIDENCY
product: Windows
targetos: Windows
req.typenames: DXGI_DDI_ARG_QUERYRESOURCERESIDENCY
---

# DXGI_DDI_ARG_QUERYRESOURCERESIDENCY structure


## -description


The DXGI_DDI_ARG_QUERYRESOURCERESIDENCY structure describes the residency status of a list of resources. 


## -syntax


````
typedef struct DXGI_DDI_ARG_QUERYRESOURCERESIDENCY {
  DXGI_DDI_HDEVICE         hDevice;
  const DXGI_DDI_HRESOURCE *pResources;
  DXGI_DDI_RESIDENCY       *pStatus;
  SIZE_T                   Resources;
} DXGI_DDI_ARG_QUERYRESOURCERESIDENCY;
````


## -struct-fields




### -field hDevice

[in] A handle to the display device (graphics context) on which the driver determines resource residency status. The Direct3D runtime passes this handle to the driver in the <b>hDrvDevice</b> member of the <a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddiarg_createdevice.md">D3D10DDIARG_CREATEDEVICE</a> structure when the runtime calls the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a> function to create the display device. 


### -field pResources

[in] An array of handles to the resources to query for residency on. 


### -field pStatus

[out] A pointer to an array of DXGI_DDI_RESIDENCY values. The number of elements in the array is specified by the <b>Resources</b> member, and each element receives one of the following values to indicate the residency status of the corresponding resource in the array that <b>pResources</b> specifies. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DXGI_DDI_RESIDENCY_FULLY_RESIDENT (1)

</td>
<td>
The resources reside in GPU memory, which is the highest residency status.

</td>
</tr>
<tr>
<td>
DXGI_DDI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY (2)

</td>
<td>
The resources reside in shared memory.

</td>
</tr>
<tr>
<td>
DXGI_DDI_RESIDENCY_EVICTED_TO_DISK (3)

</td>
<td>
The resources are nonresident, which is the lowest residency status.

</td>
</tr>
</table>
 


### -field Resources

[in] The number of elements in the <i>pResources</i> and <i>pStatus</i> arrays. 


## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff569224">QueryResourceResidencyDXGI</a>



 

 


