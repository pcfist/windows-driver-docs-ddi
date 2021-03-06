---
UID: NF:usbdlib.UsbBuildGetStatusRequest
title: UsbBuildGetStatusRequest macro
author: windows-driver-content
description: The UsbBuildGetStatusRequest macro formats an URB to obtain status from a device, interface, endpoint, or other device-defined target on a USB device.
old-location: buses\usbbuildgetstatusrequest.htm
old-project: usbref
ms.assetid: 7a5fcb4f-fc9a-4ebb-93ef-b83461557b22
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: UsbBuildGetStatusRequest, UsbBuildGetStatusRequest routine [Buses], buses.usbbuildgetstatusrequest, usbdlib/UsbBuildGetStatusRequest, usbfunc_a99bf737-8bb6-4000-af2b-ac076a4ffc8e.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: usbdlib.h
req.include-header: Usbdlib.h
req.target-type: Desktop
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbdlib.h
api_name:
-	UsbBuildGetStatusRequest
product: Windows
targetos: Windows
req.typenames: USBCAMD_DEVICE_DATA2, *PUSBCAMD_DEVICE_DATA2
req.product: Windows 10 or later.
---

# UsbBuildGetStatusRequest macro


## -description



   The <b>UsbBuildGetStatusRequest</b> macro formats an <a href="..\usb\ns-usb-_urb.md">URB</a> to obtain status from a device, interface, endpoint, or other device-defined target on a USB device.


## -syntax


````
void UsbBuildGetStatusRequest(
  _Inout_         urb,
  _In_     USHORT op,
  _In_     USHORT index,
  _In_opt_ PVOID  transferBuffer,
  _In_opt_ PMDL   transferBufferMDL,
  _In_     PURB   link
);
````


## -parameters




### -param urb [in, out]

Pointer to an <a href="..\usb\ns-usb-_urb.md">URB</a> to be formatted as an status request.


### -param op [in]

Specifies one of the following values:





#### URB_FUNCTION_GET_STATUS_FROM_DEVICE

Retrieves status from a USB device.



#### URB_FUNCTION_GET_STATUS_FROM_INTERFACE

Retrieves status from an interface on a USB device.



#### URB_FUNCTION_GET_STATUS_FROM_ENDPOINT

Retrieves status from an endpoint for an interface on a USB device.



#### URB_FUNCTION_GET_STATUS_FROM_OTHER

Retrieves status from a device-defined target on a USB device.


### -param index [in]

Specifies the device-defined index, returned by a successful configuration request, if the request is for an endpoint or interface. Otherwise, <i>Index</i> must be zero.


### -param transferBuffer [in, optional]

Pointer to a resident buffer to receive the status data or is <b>NULL</b> if an MDL is supplied in <i>TransferBufferMDL</i>.


### -param transferBufferMDL [in, optional]

Pointer to an MDL that describes a resident buffer to receive the status data or is <b>NULL</b> if a buffer is supplied in <i>TransferBuffer</i>.


### -param link [in]

Reserved. Must be set to <b>NULL</b>. 


## -see-also

<a href="..\usb\ns-usb-_urb.md">URB</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540134">USB device driver programming reference</a>



<a href="..\usb\ns-usb-_urb_control_get_status_request.md">_URB_CONTROL_GET_STATUS_REQUEST</a>



 

 


