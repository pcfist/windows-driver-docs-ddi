---
UID: NF:ucxendpoint.UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT
title: UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT function
author: windows-driver-content
description: Initializes a UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS structure with client driver's callback functions. The client driver calls this function before calling UcxEndpointCreate method to create an endpoint and register its callback functions with UCX.
old-location: buses\ucx_default_endpoint_event_callbacks_init.htm
old-project: usbref
ms.assetid: EE7ABC3D-948B-481B-B254-40A05EDEB83D
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT, UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT function [Buses], buses.ucx_default_endpoint_event_callbacks_init, ucxendpoint/UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ucxendpoint.h
req.include-header: Ucxclass.h, Ucxendpoint.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ucxendpoint.h
api_name:
-	UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT
product: Windows
targetos: Windows
req.typenames: UCX_ENDPOINT_CHARACTERISTIC_TYPE
req.product: Windows 10 or later.
---

# UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT function


## -description


Initializes a <a href="..\ucxendpoint\ns-ucxendpoint-_ucx_default_endpoint_event_callbacks.md">UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS</a> structure with client driver's callback functions. The client driver calls this function before calling <a href="..\ucxendpoint\nf-ucxendpoint-ucxendpointcreate.md">UcxEndpointCreate</a> method to create an endpoint and register its callback functions with UCX.


## -syntax


````
FORCEINLINE void UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS_INIT(
  _Out_ PUCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS        Callbacks,
  _In_  PEVT_UCX_ENDPOINT_PURGE                      EvtEndpointPurge,
  _In_  PEVT_UCX_ENDPOINT_START                      EvtEndpointStart,
  _In_  PEVT_UCX_ENDPOINT_ABORT                      EvtEndpointAbort,
  _In_  PEVT_UCX_ENDPOINT_OK_TO_CANCEL_TRANSFERS     EvtEndpointOkToCancelTransfers,
  _In_  PEVT_UCX_DEFAULT_ENDPOINT_UPDATE             EvtDefaultEndpointUpdate
);
````


## -parameters




### -param Callbacks [out]

A pointer to a <a href="..\ucxendpoint\ns-ucxendpoint-_ucx_default_endpoint_event_callbacks.md">UCX_DEFAULT_ENDPOINT_EVENT_CALLBACKS</a> structure that contains pointers to the client driver's event callback functions.


### -param EvtEndpointPurge [in]

A pointer to client driver's implementation of the <a href="..\ucxendpoint\nc-ucxendpoint-evt_ucx_endpoint_purge.md">EVT_UCX_ENDPOINT_PURGE</a>                     event callback function.


### -param EvtEndpointStart [in]

A pointer to client driver's implementation of the <a href="..\ucxendpoint\nc-ucxendpoint-evt_ucx_endpoint_start.md">EVT_UCX_ENDPOINT_START</a>                     event callback function.


### -param EvtEndpointAbort [in]

A pointer to client driver's implementation of the <a href="..\ucxendpoint\nc-ucxendpoint-evt_ucx_endpoint_abort.md">EVT_UCX_ENDPOINT_ABORT</a>                     event callback function.


### -param EvtEndpointOkToCancelTransfers [in]

A pointer to client driver's implementation of the <a href="..\ucxendpoint\nc-ucxendpoint-evt_ucx_endpoint_ok_to_cancel_transfers.md">EVT_UCX_ENDPOINT_OK_TO_CANCEL_TRANSFERS</a>    event callback function.


### -param EvtDefaultEndpointUpdate [in]

A pointer to client driver's implementation of the <a href="..\ucxendpoint\nc-ucxendpoint-evt_ucx_default_endpoint_update.md">EVT_UCX_DEFAULT_ENDPOINT_UPDATE</a>    event callback function.


## -returns



This function does not return a value.




## -see-also

<a href="..\ucxendpoint\nf-ucxendpoint-ucxendpointcreate.md">UcxEndpointCreate</a>



 

 


