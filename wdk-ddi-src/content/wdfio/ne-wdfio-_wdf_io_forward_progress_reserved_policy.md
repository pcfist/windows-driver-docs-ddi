---
UID: NE:wdfio._WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY
title: "_WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY"
author: windows-driver-content
description: The WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY enumeration identifies actions that the framework can take when it receives an I/O request for your driver, if a low-memory situation exists.
old-location: wdf\wdf_io_forward_progress_reserved_policy.htm
old-project: wdf
ms.assetid: 6d530cf2-de06-4aa3-9f4d-08619906c9ed
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DFQueueObjectRef_e035ecd7-f728-4d88-80a8-763ab3eb90ab.xml, WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY, WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY enumeration, WdfIoForwardProgressInvalidPolicy, WdfIoForwardProgressReservedPolicyAlwaysUseReservedRequest, WdfIoForwardProgressReservedPolicyPagingIO, WdfIoForwardProgressReservedPolicyUseExamine, _WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY, kmdf.wdf_io_forward_progress_reserved_policy, wdf.wdf_io_forward_progress_reserved_policy, wdfio/WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY, wdfio/WdfIoForwardProgressInvalidPolicy, wdfio/WdfIoForwardProgressReservedPolicyAlwaysUseReservedRequest, wdfio/WdfIoForwardProgressReservedPolicyPagingIO, wdfio/WdfIoForwardProgressReservedPolicyUseExamine
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdfio.h
req.include-header: Wdf.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.9
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
req.irql: "<= DISPATCH_LEVEL (see Remarks section)"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wdfio.h
api_name:
-	WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY
product: Windows
targetos: Windows
req.typenames: WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY
req.product: Windows 10 or later.
---

# _WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY enumeration


## -description


<p class="CCE_Message">[Applies to KMDF only]

The <b>WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY</b> enumeration identifies actions that the framework can take when it receives an I/O request for your driver, if a low-memory situation exists.


## -syntax


````
typedef enum _WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY { 
  WdfIoForwardProgressInvalidPolicy                           = 0x0,
  WdfIoForwardProgressReservedPolicyAlwaysUseReservedRequest  = 0x1,
  WdfIoForwardProgressReservedPolicyUseExamine                = 0x2,
  WdfIoForwardProgressReservedPolicyPagingIO                  = 0x3
} WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY;
````


## -enum-fields




### -field WdfIoForwardProgressInvalidPolicy


### -field WdfIoForwardProgressReservedPolicyAlwaysUseReservedRequest

In a low-memory situation, the framework always uses a reserved request object, if one is available.


### -field WdfIoForwardProgressReservedPolicyUseExamine

In a low-memory situation, the framework calls the driver's <a href="..\wdfio\nc-wdfio-evt_wdf_io_wdm_irp_for_forward_progress.md">EvtIoWdmIrpForForwardProgress</a> callback function.


### -field WdfIoForwardProgressReservedPolicyPagingIO

In a low-memory situation, if the <b>Flags</b> member of the I/O request's <a href="..\wdm\ns-wdm-_irp.md">IRP</a> structure indicates a paging operation, the framework uses a reserved request object, if one is available. If the I/O request is not a paging operation, the framework completes the I/O request with an error status value.


## -remarks



The <b>WDF_IO_FORWARD_PROGRESS_RESERVED_POLICY</b> enumeration is used as a member type in the <a href="..\wdfio\ns-wdfio-_wdf_io_queue_forward_progress_policy.md">WDF_IO_QUEUE_FORWARD_PROGRESS_POLICY</a> structure.



