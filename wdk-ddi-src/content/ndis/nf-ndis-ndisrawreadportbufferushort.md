---
UID: NF:ndis.NdisRawReadPortBufferUshort
title: NdisRawReadPortBufferUshort macro
author: windows-driver-content
description: NdisRawReadPortBufferUshort reads a specified number of USHORTs into a caller-supplied buffer.
old-location: netvista\ndisrawreadportbufferushort.htm
old-project: netvista
ms.assetid: c100aad1-2fb9-49e0-b68e-20b165a69701
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: NdisRawReadPortBufferUshort, NdisRawReadPortBufferUshort macro [Network Drivers Starting with Windows Vista], miniport_port_raw_ref_fc8d7120-4fbc-46e3-9946-c269f2992f56.xml, ndis/NdisRawReadPortBufferUshort, netvista.ndisrawreadportbufferushort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Universal
req.target-min-winverclnt: Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisRawReadPortBufferUshort   (NDIS 5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see    NdisRawReadPortBufferUshort   (NDIS 5.1)) in Windows XP.
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
req.irql: Any level
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ndis.h
api_name:
-	NdisRawReadPortBufferUshort
product: Windows
targetos: Windows
req.typenames: NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---

# NdisRawReadPortBufferUshort macro


## -description


<b>NdisRawReadPortBufferUshort</b> reads a specified number of USHORTs into a caller-supplied buffer.


## -syntax


````
VOID NdisRawReadPortBufferUshort(
  [in]  ULONG_PTR Port,
  [out] PUSHORT   Buffer,
  [in]  ULONG     Length
);
````


## -parameters




### -param Port [in]

Specifies the I/O port. This address falls in a range that was mapped during initialization with 
     <a href="..\ndis\nf-ndis-ndismregisterioportrange.md">
     NdisMRegisterIoPortRange</a>.


### -param Buffer [out]

Pointer to a caller-allocated buffer, in resident memory, into which the USHORTs will be
     transferred from the NIC. The caller must allocate a buffer at least (<b>sizeof</b>(USHORT)
     *
     <i>Length</i> ).


### -param Length [in]

Specifies how many USHORTs to transfer from the NIC.


## -remarks



<b>NdisRawReadPortBufferUshort</b> reads each USHORT value, one at a time, from the given I/O port into
    the given buffer.




## -see-also

<a href="..\ndis\nf-ndis-ndisrawwriteportbufferushort.md">NdisRawWritePortBufferUshort</a>



<a href="..\ndis\nf-ndis-ndismregisterioportrange.md">NdisMRegisterIoPortRange</a>



<a href="..\ndis\nc-ndis-miniport_initialize.md">MiniportInitializeEx</a>



<a href="..\ndis\nf-ndis-ndisrawreadportbufferuchar.md">NdisRawReadPortBufferUchar</a>



<a href="..\ndis\nf-ndis-ndisrawreadportushort.md">NdisRawReadPortUshort</a>



<a href="..\ndis\nf-ndis-ndisrawreadportbufferulong.md">NdisRawReadPortBufferUlong</a>



 

 


