---
UID: NC:vmbuskernelmodeclientlibapi.EVT_VMB_PACKET_COMPLETION_ROUTINE
title: EVT_VMB_PACKET_COMPLETION_ROUTINE
author: windows-driver-content
description: The EvtVmbPacketCompletionRoutine callback function is invoked when the transaction associated with a sent packet is complete.
old-location: netvista\evt_vmb_packet_completion_routine.htm
old-project: netvista
ms.assetid: DEE6FBD6-4807-4216-9010-F59C9E08076B
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: EVT_VMB_PACKET_COMPLETION_ROUTINE, EvtVmbPacketCompletionRoutine, EvtVmbPacketCompletionRoutine callback function [Network Drivers Starting with Windows Vista], PFN_VMB_PACKET_COMPLETION_ROUTINE, PFN_VMB_PACKET_COMPLETION_ROUTINE callback function pointer [Network Drivers Starting with Windows Vista], netvista.evt_vmb_packet_completion_routine, vmbuskernelmodeclientlibapi/EvtVmbPacketCompletionRoutine
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: vmbuskernelmodeclientlibapi.h
req.include-header: VmbusKernelModeClientLibApi.h
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
req.irql: "<=DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	VmbusKernelModeClientLibApi.h
api_name:
-	PFN_VMB_PACKET_COMPLETION_ROUTINE
product: Windows
targetos: Windows
req.typenames: VIDEO_PORT_AGP_SERVICES, *PVIDEO_PORT_AGP_SERVICES
req.product: Windows 10 or later.
---

# EVT_VMB_PACKET_COMPLETION_ROUTINE callback


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <i>EvtVmbPacketCompletionRoutine</i> callback function is invoked when the transaction associated with a sent packet
is complete.  


## -prototype


````
EVT_VMB_PACKET_COMPLETION_ROUTINE EvtVmbPacketCompletionRoutine;

VOID EvtVmbPacketCompletionRoutine(
  _In_ VMBPACKET                            Packet,
  _In_ NTSTATUS                             Status,
  _In_ reads_bytes_opt_(BufferLength) PVOID Buffer,
  _In_ UINT32                               BufferLength
)
{ ... }

typedef EVT_VMB_PACKET_COMPLETION_ROUTINE PFN_VMB_PACKET_COMPLETION_ROUTINE;
````


## -parameters




### -param Packet [in]

The packet that is completed.



### -param Status [in]

A status code.


### -param Buffer [in]

A buffer that contains the completion response from the opposite endpoint, if any.



### -param BufferLength [in]

Length of the <i>Buffer</i> parameter, in bytes.


## -returns



This callback function does not return a value.




## -remarks



After allocating a packet object by using the <a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketallocate.md">VmbPacketAllocate</a> function, the client drive can set a completion callback by using the <a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketsetcompletionroutine.md">VmbPacketSetCompletionRoutine</a> function.  

If the sender used the VMBUS_CHANNEL_FORMAT_FLAG_WAIT_FOR_COMPLETION
flag, invocation of this callback means that the opposite endpoint received the packet and completed it.
If not, the outgoing packet was successfully placed into the ring buffer.




## -see-also

<a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketallocate.md">VmbPacketAllocate</a>



<a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketsetcompletionroutine.md">VmbPacketSetCompletionRoutine</a>



 

 


