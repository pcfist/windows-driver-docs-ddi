---
UID: NS:ucxendpoint._UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS
title: "_UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS"
author: windows-driver-content
description: Stores the isochronous transfer path delay values.
old-location: buses\ucx_endpoint_isoch_transfer_path_delays.htm
old-project: usbref
ms.assetid: 5001C27B-EA5F-43C4-AD59-84B42041262E
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PUCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, PUCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, PUCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS structure pointer [Buses], UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS structure [Buses], _UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, buses.ucx_endpoint_isoch_transfer_path_delays, ucxendpoint/PUCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, ucxendpoint/UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ucxendpoint.h
req.include-header: Ucxclass.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
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
-	Ucxendpoint.h
api_name:
-	UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS
product: Windows
targetos: Windows
req.typenames: UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, *PUCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS
req.product: Windows 10 or later.
---

# _UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS structure


## -description


Stores the isochronous transfer path delay values. 


## -syntax


````
typedef struct _UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS {
  ULONG MaximumSendPathDelayInMilliSeconds;
  ULONG MaximumCompletionPathDelayInMilliSeconds;
} UCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS, *PUCX_ENDPOINT_ISOCH_TRANSFER_PATH_DELAYS;
````


## -struct-fields




### -field MaximumSendPathDelayInMilliSeconds

The maximum delay in milliseconds from the time the  client driver's isochronous transfer is received by the USB driver stack to the time the transfer is programmed in the host controller. The host controller could either be a local host (as in case of wired USB) or it could be a remote controller as in case of Media-Agnostic USB (MA-USB). In case of MA-USB, it includes the maximum delay associated with the network medium.  
  


### -field MaximumCompletionPathDelayInMilliSeconds

The maximum delay in milliseconds from the time an isochronous transfer is completed by the (local or remote) host controller to the time the corresponding client driver's request is completed by the USB driver stack. For MA-USB, it includes the maximum delay associated with the network medium.


## -see-also

<a href="..\ucxendpoint\nc-ucxendpoint-evt_ucx_endpoint_get_isoch_transfer_path_delays.md">EVT_UCX_ENDPOINT_GET_ISOCH_TRANSFER_PATH_DELAYS</a>



 

 


