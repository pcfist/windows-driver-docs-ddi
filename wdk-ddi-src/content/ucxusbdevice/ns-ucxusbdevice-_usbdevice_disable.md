---
UID: NS:ucxusbdevice._USBDEVICE_DISABLE
title: "_USBDEVICE_DISABLE"
author: windows-driver-content
description: Contains parameters for a request to disable the specified device. This structure is passed by UCX in request parameters (Parameters.Others.Arg1) of a framework request object of the EVT_UCX_USBDEVICE_DISABLE callback function.
old-location: buses\_usbdevice_disable.htm
old-project: usbref
ms.assetid: C9F2331F-0C16-47F3-9FDE-2719E179513F
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PUSBDEVICE_DISABLE, P_USBDEVICE_DISABLE, P_USBDEVICE_DISABLE structure pointer [Buses], USBDEVICE_DISABLE, USBDEVICE_DISABLE structure [Buses], _USBDEVICE_DISABLE, buses._usbdevice_disable, ucxusbdevice/P_USBDEVICE_DISABLE, ucxusbdevice/_USBDEVICE_DISABLE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ucxusbdevice.h
req.include-header: Ucxclass.h
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ucxusbdevice.h
api_name:
-	USBDEVICE_DISABLE
product: Windows
targetos: Windows
req.typenames: USBDEVICE_DISABLE, *PUSBDEVICE_DISABLE
req.product: Windows 10 or later.
---

# _USBDEVICE_DISABLE structure


## -description


Contains parameters for a request to disable the specified device. This structure is passed by UCX in request parameters (<b>Parameters.Others.Arg1</b>) of a framework request object of the <a href="..\ucxusbdevice\nc-ucxusbdevice-evt_ucx_usbdevice_disable.md">EVT_UCX_USBDEVICE_DISABLE</a> callback function.


## -syntax


````
typedef struct _USBDEVICE_DISABLE {
#if __cplusplus
  USBDEVICE_MGMT_HEADER Header;
#else 
  USBDEVICE_MGMT_HEADER ;
#endif 
  UCXENDPOINT           DefaultEndpoint;
} USBDEVICE_DISABLE, *P_USBDEVICE_DISABLE;
````


## -struct-fields




### -field Header

A <a href="..\ucxusbdevice\ns-ucxusbdevice-_usbdevice_mgmt_header.md">USBDEVICE_MGMT_HEADER</a> structure that contains  the handle for the USB hub or device.


### -field DefaultEndpoint

A handle to the default endpoint of the USB device or hub to disable.


## -see-also

<a href="..\ucxusbdevice\nc-ucxusbdevice-evt_ucx_usbdevice_disable.md">EVT_UCX_USBDEVICE_DISABLE</a>



<a href="..\wdfrequest\nf-wdfrequest-wdfrequestgetparameters.md">WdfRequestGetParameters</a>



<a href="..\ucxusbdevice\ns-ucxusbdevice-_usbdevice_enable.md">USBDEVICE_ENABLE</a>



 

 


