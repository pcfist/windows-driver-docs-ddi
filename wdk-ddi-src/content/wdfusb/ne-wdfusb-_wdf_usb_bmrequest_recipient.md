---
UID: NE:wdfusb._WDF_USB_BMREQUEST_RECIPIENT
title: "_WDF_USB_BMREQUEST_RECIPIENT"
author: windows-driver-content
description: The WDF_USB_BMREQUEST_RECIPIENT enumeration identifies the data transfer recipient for a USB control transfer.
old-location: wdf\wdf_usb_bmrequest_recipient.htm
old-project: wdf
ms.assetid: 0749d03d-8174-4f6e-816e-4689594c0c84
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: BmRequestToDevice, BmRequestToEndpoint, BmRequestToInterface, BmRequestToOther, DFUsbRef_646fa8bb-2b05-4247-b3e8-01daad8b204e.xml, WDF_USB_BMREQUEST_RECIPIENT, WDF_USB_BMREQUEST_RECIPIENT enumeration, _WDF_USB_BMREQUEST_RECIPIENT, kmdf.wdf_usb_bmrequest_recipient, wdf.wdf_usb_bmrequest_recipient, wdfusb/BmRequestToDevice, wdfusb/BmRequestToEndpoint, wdfusb/BmRequestToInterface, wdfusb/BmRequestToOther, wdfusb/WDF_USB_BMREQUEST_RECIPIENT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdfusb.h
req.include-header: Wdfusb.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: "<=DISPATCH_LEVEL  (See Remarks section.)"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wdfusb.h
api_name:
-	WDF_USB_BMREQUEST_RECIPIENT
product: Windows
targetos: Windows
req.typenames: WDF_USB_BMREQUEST_RECIPIENT
req.product: Windows 10 or later.
---

# _WDF_USB_BMREQUEST_RECIPIENT enumeration


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_USB_BMREQUEST_RECIPIENT</b> enumeration identifies the data transfer recipient for a USB control transfer. 


## -syntax


````
typedef enum _WDF_USB_BMREQUEST_RECIPIENT { 
  BmRequestToDevice     = BMREQUEST_TO_DEVICE,
  BmRequestToInterface  = BMREQUEST_TO_INTERFACE,
  BmRequestToEndpoint   = BMREQUEST_TO_ENDPOINT,
  BmRequestToOther      = BMREQUEST_TO_OTHER
} WDF_USB_BMREQUEST_RECIPIENT;
````


## -enum-fields




### -field BmRequestToDevice

The data transfer recipient is a device.


### -field BmRequestToInterface

The data transfer recipient is a device interface.


### -field BmRequestToEndpoint

The data transfer recipient is a pipe endpoint.


### -field BmRequestToOther

The data transfer recipient is not a device, interface, or endpoint.


## -remarks



The<b>WDF_USB_BMREQUEST_RECIPIENT</b> enumeration is used in the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

For more information about the data transfer recipient for a USB control transfer, see the USB specification.




## -see-also

<a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a>



 

 


