---
UID: NF:vmbuskernelmodeclientlibapi.VmbPacketAllocate
title: VmbPacketAllocate function
author: windows-driver-content
description: The VmbPacketAllocate function allocates a packet from the channel's lookaside list.
old-location: netvista\vmbpacketallocate.htm
old-project: netvista
ms.assetid: F121A7BC-5504-4CF5-8C8A-0568D6C4F77F
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: VmbPacketAllocate, VmbPacketAllocate function [Network Drivers Starting with Windows Vista], netvista.vmbpacketallocate, vmbuskernelmodeclientlibapi/VmbPacketAllocate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vmbuskernelmodeclientlibapi.h
req.include-header: VmbusKernelModeClientLibApi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 1.13
req.umdf-ver: 2.0
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vmbkmcl.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	vmbkmcl.lib
-	vmbkmcl.dll
api_name:
-	VmbPacketAllocate
product: Windows
targetos: Windows
req.typenames: VIDEO_PORT_AGP_SERVICES, *PVIDEO_PORT_AGP_SERVICES
req.product: Windows 10 or later.
---

# VmbPacketAllocate function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>VmbPacketAllocate</b> function allocates a packet from the channel's lookaside list.


## -syntax


````
VMBPACKET VmbPacketAllocate(
  _In_ VMBCHANNEL Channel
);
````


## -parameters




### -param Channel [in]

A handle for a channel.  


## -returns



<b>VmbPacketAllocate</b> returns a pointer to an allocated VMBus packet object or null.




## -remarks



The default completion routine of a packet automatically releases the packet.
If the packet is not sent or if the completion routine is changed, the
client should call the <a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketfree.md">VmbPacketFree</a> function to release the packet.




## -see-also

<a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketfree.md">VmbPacketFree</a>



 

 


