---
UID: NF:hidpi.HidP_GetCaps
title: HidP_GetCaps function
author: windows-driver-content
description: The HidP_GetCaps routine returns a top-level collection's HIDP_CAPS structure.
old-location: hid\hidp_getcaps.htm
old-project: hid
ms.assetid: a43baab5-26d9-43f7-bc13-3b0864769e68
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: HidP_GetCaps, HidP_GetCaps callback function [Human Input Devices], PHIDP_GETCAPS, hid.hidp_getcaps, hidfunc_420188e5-e357-43cc-b195-dea7637fd3c9.xml, hidpi/HidP_GetCaps
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: hidpi.h
req.include-header: Hidclass.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of Windows.
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
-	hidpi.h
api_name:
-	HidP_GetCaps
product: Windows
targetos: Windows
req.typenames: HIDP_REPORT_TYPE
---

# HidP_GetCaps function


## -description


The <b>HidP_GetCaps</b> routine returns a <a href="https://msdn.microsoft.com/dcbee8e3-d03a-45c8-92e4-0897b9f55177">top-level collection's</a> <a href="..\hidpi\ns-hidpi-_hidp_caps.md">HIDP_CAPS</a> structure.


## -syntax


````
PHIDP_GETCAPS HidP_GetCaps;

NTSTATUS __stdcall HidP_GetCaps(
  _In_  PHIDP_PREPARSED_DATA PreparsedData,
  _Out_ PHIDP_CAPS           Capabilities
)
{ ... }
````


## -parameters




### -param PreparsedData [in]

Pointer to a top-level collection's <a href="https://msdn.microsoft.com/50ac2877-4c45-4d55-b5cc-013486892fbf">preparsed data</a>.


### -param Capabilities [out]

Pointer to a caller-allocated buffer that the routine uses to return a collection's HIDP_CAPS structure.


## -returns



<b>HidP_GetCaps</b> returns one of the following status values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HIDP_STATUS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The routine successfully returned the collection capability information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HIDP_STATUS_INVALID_PREPARSED_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified preparsed data is invalid.

</td>
</tr>
</table>
 




## -remarks



For more information about a collection's capability, see <a href="https://msdn.microsoft.com/0568993b-ff50-48ac-a875-95ab643d6c28">Obtaining Collection Information</a>.

See also <a href="https://msdn.microsoft.com/2d3efb38-4eba-43db-8cff-9fac30209952">HID Collections</a>. 




## -see-also

<a href="..\hidsdi\nf-hidsdi-hidd_getpreparseddata.md">HidD_GetPreparsedData</a>



<a href="..\hidpi\ns-hidpi-_hidp_caps.md">HIDP_CAPS</a>



<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff539679">_HIDP_PREPARSED_DATA</a>



<a href="..\hidclass\ni-hidclass-ioctl_hid_get_collection_descriptor.md">IOCTL_HID_GET_COLLECTION_DESCRIPTOR</a>



<a href="..\hidclass\ni-hidclass-ioctl_hid_get_collection_information.md">IOCTL_HID_GET_COLLECTION_INFORMATION</a>



 

 


