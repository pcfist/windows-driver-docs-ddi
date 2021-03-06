---
UID: NE:ucxendpoint._ENDPOINT_RESET_FLAGS
title: "_ENDPOINT_RESET_FLAGS"
author: windows-driver-content
description: Defines parameters for a request to reset an endpoint.
old-location: buses\endpoint_reset_flags.htm
old-project: usbref
ms.assetid: 3775836D-DC1E-47B4-8186-2AC329825FCE
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: ENDPOINT_RESET_FLAGS, ENDPOINT_RESET_FLAGS enumeration [Buses], FlagEndpointResetPreserveTransferState, _ENDPOINT_RESET_FLAGS, buses.endpoint_reset_flags, ucxendpoint/ENDPOINT_RESET_FLAGS, ucxendpoint/FlagEndpointResetPreserveTransferState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ucxendpoint.h
req.include-header: Ucxclass.h, Ucxendpoint.h
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
req.irql: DISPATCH_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ucxendpoint.h
api_name:
-	ENDPOINT_RESET_FLAGS
product: Windows
targetos: Windows
req.typenames: ENDPOINT_RESET_FLAGS
req.product: Windows 10 or later.
---

# _ENDPOINT_RESET_FLAGS enumeration


## -description


Defines parameters for a request to reset an endpoint.


## -syntax


````
typedef enum _ENDPOINT_RESET_FLAGS { 
  FlagEndpointResetPreserveTransferState  = 0x1
} ENDPOINT_RESET_FLAGS;
````


## -enum-fields




### -field FlagEndpointResetPreserveTransferState

The transfer state must be preserved after the endpoint reset operation is complete.


## -see-also

<a href="..\ucxendpoint\nc-ucxendpoint-evt_ucx_endpoint_reset.md">EVT_UCX_ENDPOINT_RESET</a>



<a href="..\ucxendpoint\ns-ucxendpoint-_endpoint_reset.md">ENDPOINT_RESET</a>



 

 


