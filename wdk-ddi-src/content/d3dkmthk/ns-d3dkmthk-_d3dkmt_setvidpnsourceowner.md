---
UID: NS:d3dkmthk._D3DKMT_SETVIDPNSOURCEOWNER
title: "_D3DKMT_SETVIDPNSOURCEOWNER"
author: windows-driver-content
description: The D3DKMT_SETVIDPNSOURCEOWNER structure describes the parameters for setting or releasing the video present source in the path of a video present network (VidPN) topology that owns the VidPN.
old-location: display\d3dkmt_setvidpnsourceowner.htm
old-project: display
ms.assetid: 9154848b-ecbe-4f21-9d27-9013f97c5dde
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3DKMT_SETVIDPNSOURCEOWNER, D3DKMT_SETVIDPNSOURCEOWNER structure [Display Devices], OpenGL_Structs_942045f1-1a3a-4c4a-b533-ec70fcad6d8f.xml, _D3DKMT_SETVIDPNSOURCEOWNER, d3dkmthk/D3DKMT_SETVIDPNSOURCEOWNER, display.d3dkmt_setvidpnsourceowner
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
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
-	d3dkmthk.h
api_name:
-	D3DKMT_SETVIDPNSOURCEOWNER
product: Windows
targetos: Windows
req.typenames: D3DKMT_SETVIDPNSOURCEOWNER
---

# _D3DKMT_SETVIDPNSOURCEOWNER structure


## -description


The D3DKMT_SETVIDPNSOURCEOWNER structure describes the parameters for setting or releasing the video present source in the path of a video present network (VidPN) topology that owns the VidPN.


## -syntax


````
typedef struct _D3DKMT_SETVIDPNSOURCEOWNER {
  D3DKMT_HANDLE                        hDevice;
  const D3DKMT_VIDPNSOURCEOWNER_TYPE   *pType;
  const D3DDDI_VIDEO_PRESENT_SOURCE_ID *pVidPnSourceId;
  UINT                                 VidPnSourceCount;
} D3DKMT_SETVIDPNSOURCEOWNER;
````


## -struct-fields




### -field hDevice

[in] A D3DKMT_HANDLE data type that represents a kernel-mode handle to the device that acquires or releases the VidPN source owner.


### -field pType

[in] An array of owner types. Elements of the array can contain the following values from the D3DKMT_VIDPNSOURCEOWNER_TYPE enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
D3DKMT_VIDPNSOURCEOWNER_UNOWNED (0)

</td>
<td>
No owner, or GDI is the owner.

</td>
</tr>
<tr>
<td>
D3DKMT_VIDPNSOURCEOWNER_SHARED (1)

</td>
<td>
A shared owner. That is, the owner can yield to any exclusive owner. This type is not available to legacy devices.

</td>
</tr>
<tr>
<td>
D3DKMT_VIDPNSOURCEOWNER_EXCLUSIVE (2)

</td>
<td>
An exclusive owner without shared GDI primary.

</td>
</tr>
<tr>
<td>
D3DKMT_VIDPNSOURCEOWNER_EXCLUSIVEGDI (3)

</td>
<td>
An exclusive owner with shared GDI primary. This owner must exclusively own all of the VidPn sources. This type is available only to legacy devices.

</td>
</tr>
</table>
 


### -field pVidPnSourceId

[in] An array of zero-based identification numbers of the video present sources in paths of a video present network (VidPN) topology.


### -field VidPnSourceCount

The number of valid entries in the array that <b>pVidPnSourceId</b> specifies.


## -see-also

<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtsetvidpnsourceowner.md">D3DKMTSetVidPnSourceOwner</a>



 

 


