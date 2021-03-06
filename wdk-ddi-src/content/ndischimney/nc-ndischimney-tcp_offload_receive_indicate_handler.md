---
UID: NC:ndischimney.TCP_OFFLOAD_RECEIVE_INDICATE_HANDLER
title: TCP_OFFLOAD_RECEIVE_INDICATE_HANDLER
author: windows-driver-content
description: NDIS calls a protocol driver's or intermediate driver's ProtocolTcpOffloadReceiveIndicate function to deliver received data that is being indicated by an underlying driver or offload target.
old-location: netvista\protocoltcpoffloadreceiveindicate.htm
old-project: netvista
ms.assetid: 8a400515-3619-4fe9-8e08-638859442ea3
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: ProtocolTcpOffloadReceiveIndicate, ProtocolTcpOffloadReceiveIndicate callback function [Network Drivers Starting with Windows Vista], TCP_OFFLOAD_RECEIVE_INDICATE_HANDLER, ndischimney/ProtocolTcpOffloadReceiveIndicate, netvista.protocoltcpoffloadreceiveindicate, tcp_chim_protocol_func_c65e1895-a874-4c93-b25f-f2951a0a19db.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ndischimney.h
req.include-header: Ndischimney.h
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
-	UserDefined
api_location:
-	Ndischimney.h
api_name:
-	ProtocolTcpOffloadReceiveIndicate
product: Windows
targetos: Windows
req.typenames: PD_BUFFER_VIRTUAL_SUBNET_INFO
---

# TCP_OFFLOAD_RECEIVE_INDICATE_HANDLER callback


## -description


<p class="CCE_Message">[The TCP chimney offload feature is deprecated and should not be used.]

NDIS calls a protocol driver's or intermediate driver's 
  <i>
  ProtocolTcpOffloadReceiveIndicate</i> function to deliver received data that is being indicated by an
  underlying driver or offload target.


## -prototype


````
TCP_OFFLOAD_RECEIVE_INDICATE_HANDLER ProtocolTcpOffloadReceiveIndicate;

NDIS_STATUS ProtocolTcpOffloadReceiveIndicate(
  _In_  PVOID            OffloadContext,
  _In_  PNET_BUFFER_LIST NetBufferList,
  _In_  NDIS_STATUS      Status,
  _Out_ PULONG           BytesConsumed
)
{ ... }
````


## -parameters




### -param OffloadContext [in]

A pointer to the protocol or intermediate driver's 
     <a href="..\ndischimney\ns-ndischimney-_ndis_offload_handle.md">NDIS_OFFLOAD_HANDLE</a> structure for the
     TCP connection on which the indication is being made. The protocol or intermediate driver supplied this
     pointer as an input parameter to the 
     <a href="..\ndischimney\nf-ndischimney-ndisinitiateoffload.md">NdisInitiateOffload</a> function when
     offloading the connection.


### -param NetBufferList [in]

A pointer to a 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff568388">NET_BUFFER_LIST</a> structure. Each 
      <b>NET_BUFFER_LIST</b> structure
      describes a list of 
      <a href="..\ndis\ns-ndis-_net_buffer.md">NET_BUFFER</a> structures. Each 
      <b>NET_BUFFER</b> structure in the list maps to a
      chain of 
      <a href="..\wdm\ns-wdm-_mdl.md">memory descriptor lists (MDLs)</a>. The MDLs contain the
      received data. The MDLs are locked so that they remain resident, but they are not mapped into system
      memory.

The 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff568388">NET_BUFFER_LIST</a> structure
      specified by 
      <i>NetBufferList</i> must be a stand-alone structure and cannot be the first
      structure in a linked list of 
      <b>NET_BUFFER_LIST</b> structures.
      Offload targets can work around this limitation by chaining as many MDLs as necessary to the same 
      <a href="..\ndis\ns-ndis-_net_buffer.md">NET_BUFFER</a> in an offload receive
      indication.


### -param Status [in]

An intermediate driver should propagate this status when calling 
     <a href="..\ndischimney\nc-ndischimney-ndis_tcp_offload_receive_indicate.md">
     NdisTcpOffloadReceiveHandler</a>.


### -param BytesConsumed [out]

A pointer to a ULONG-typed variable that receives the number of bytes that were consumed by the
     client application.


## -returns



The 
     <i>
     ProtocolTcpOffloadReceiveIndicate</i> function can return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The client application consumed all the indicated receive data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_OFFLOAD_DATA_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
The client application rejected all the indicated receive data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_OFFLOAD_DATA_PARTIALLY_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
The client application consumed a subset of the indicated receive data. The amount of data, in
       bytes, that was consumed by the client application is returned in the variable specified by the 
       <i>BytesConsumed</i> parameter.

</td>
</tr>
</table>
 




## -remarks



To propagate the indication to the overlying driver or host stack, the intermediate driver calls the 
    <a href="..\ndischimney\nc-ndischimney-ndis_tcp_offload_receive_indicate.md">
    NdisTcpOffloadReceiveHandler</a> function. The intermediate driver passes the following parameters to
    the 
    <b>NdisTcpOffloadReceiveHandler</b> function:

<ul>
<li>
The 
      <b>NdisOffloadHandle</b> that the offload target stored in its context for the offloaded TCP connection.
      For more information, see 
      <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/referencing-offloaded-state-through-an-intermediate-driver">
      Referencing Offloaded State Through an Intermediate Driver</a>.

</li>
<li>
The 
      <i>NetBufferList</i> pointer that NDIS passed to the intermediate driver's 
      <i>ProtocolTcpOffloadReceiveIndicate</i> function.

</li>
<li>
The 
      <i>Status</i> that NDIS passed to the intermediate driver's 
      <i>ProtocolTcpOffloadReceiveIndicate</i> function.

</li>
</ul>



## -see-also

<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>



<a href="..\ndischimney\nc-ndischimney-ndis_tcp_offload_receive_indicate.md">NdisTcpOffloadReceiveHandler</a>



<a href="..\ndis\nf-ndis-ndismsetminiportattributes.md">NET_BUFFER_LIST</a>



<a href="..\ndischimney\nf-ndischimney-ndisoffloadtcpreceivereturn.md">NdisOffloadTcpReceiveReturn</a>



<a href="..\ndischimney\nf-ndischimney-ndisinitiateoffload.md">NdisInitiateOffload</a>



<a href="..\ndis\ns-ndis-_net_buffer.md">NET_BUFFER</a>



<a href="..\ndischimney\ns-ndischimney-_ndis_offload_handle.md">NDIS_OFFLOAD_HANDLE</a>



 

 


