---
UID: NC:d3d10umddi.PFND3D10DDI_CALCPRIVATEOPENEDRESOURCESIZE
title: PFND3D10DDI_CALCPRIVATEOPENEDRESOURCESIZE
author: windows-driver-content
description: The CalcPrivateOpenedResourceSize function determines the size of the user-mode display driver's private shared region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for an opened resource.
old-location: display\calcprivateopenedresourcesize.htm
old-project: display
ms.assetid: 000688fb-6475-4dab-bb65-91c899a592a7
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CalcPrivateOpenedResourceSize, CalcPrivateOpenedResourceSize callback function [Display Devices], PFND3D10DDI_CALCPRIVATEOPENEDRESOURCESIZE, UserModeDisplayDriverDx10_Functions_1be7ba80-5ffc-4871-b687-f12b4a81fad0.xml, d3d10umddi/CalcPrivateOpenedResourceSize, display.calcprivateopenedresourcesize
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
-	CalcPrivateOpenedResourceSize
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_CALCPRIVATEOPENEDRESOURCESIZE callback


## -description


The <b>CalcPrivateOpenedResourceSize</b> function determines the size of the user-mode display driver's private shared region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for an opened resource.


## -prototype


````
PFND3D10DDI_CALCPRIVATEOPENEDRESOURCESIZE CalcPrivateOpenedResourceSize;

SIZE_T APIENTRY CalcPrivateOpenedResourceSize(
  _In_       D3D10DDI_HDEVICE         hDevice,
  _In_ const D3D10DDIARG_OPENRESOURCE *pOpenResource
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *








#### - hDevice [in]

 A handle to the display device (graphics context).


#### - pOpenResource [in]

 A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddiarg_openresource.md">D3D10DDIARG_OPENRESOURCE</a> structure that describes the parameters that the user-mode display driver uses to calculate the size of the shared memory region. 


## -returns



<b>CalcPrivateOpenedResourceSize</b> returns the size of the shared memory region that the driver requires for opening resources.




## -see-also

<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddiarg_openresource.md">D3D10DDIARG_OPENRESOURCE</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_devicefuncs.md">D3D10DDI_DEVICEFUNCS</a>



 

 


