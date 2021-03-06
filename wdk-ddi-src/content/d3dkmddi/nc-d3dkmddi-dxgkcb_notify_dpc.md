---
UID: NC:d3dkmddi.DXGKCB_NOTIFY_DPC
title: DXGKCB_NOTIFY_DPC
author: windows-driver-content
description: The DxgkCbNotifyDpc function informs the graphics processing unit (GPU) scheduler about a graphics hardware update at deferred-procedure-call (DPC) time.
old-location: display\dxgkcbnotifydpc.htm
old-project: display
ms.assetid: 3df3f7d4-3721-46f5-b9e3-19bd3d870292
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGKCB_NOTIFY_DPC, DpFunctions_a1e9512a-ae77-4e3b-9876-5ce247b811e5.xml, DxgkCbNotifyDpc, DxgkCbNotifyDpc callback function [Display Devices], d3dkmddi/DxgkCbNotifyDpc, display.dxgkcbnotifydpc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
-	UserDefined
api_location:
-	d3dkmddi.h
api_name:
-	DxgkCbNotifyDpc
product: Windows
targetos: Windows
req.typenames: DD_MULTISAMPLEQUALITYLEVELSDATA
---

# DXGKCB_NOTIFY_DPC callback


## -description


The <b>DxgkCbNotifyDpc</b> function informs the graphics processing unit (GPU) scheduler about a graphics hardware update at deferred-procedure-call (DPC) time.


## -prototype


````
DXGKCB_NOTIFY_DPC DxgkCbNotifyDpc;

VOID APIENTRY DxgkCbNotifyDpc(
  _In_ const HANDLE hAdapter
)
{ ... }
````


## -parameters




### -param hAdapter [in]

[in] A handle to the adapter object for the GPU. The driver receives the handle from the <b>DeviceHandle</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560942">DXGKRNL_INTERFACE</a> structure in a call to its <a href="..\dispmprt\nc-dispmprt-dxgkddi_start_device.md">DxgkDdiStartDevice</a> function.


## -returns



None




## -remarks



The display miniport driver's DPC callback routine calls the <b>DxgkCbNotifyDpc</b> function to inform the GPU scheduler about an update to a fence through a direct memory access (DMA) stream to the graphics hardware. 


#### Examples

The following code example shows how to notify the GPU scheduler about the DMA or V-Sync interrupt.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>NTSTATUS
D3DDDINotifyDPC(
    HW_DEVICE_EXTENSION  *pAdapter)
{
    DXGKRNL_INTERFACE  *pCallback;
    DXGKCB_NOTIFY_DPC  DxgkCbNotifyDpc;

    pCallback = &amp;(pAdapter-&gt;ddiCallback);

    if (! pAdapter-&gt;pVidSchDPCCB) {
        return (STATUS_SUCCESS);
    }

    DxgkCbNotifyDpc = (DXGKCB_NOTIFY_DPC)pAdapter-&gt;pVidSchDPCCB;

    DxgkCbNotifyDpc(pAdapter-&gt;DeviceHandle);

    return (STATUS_SUCCESS);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff560942">DXGKRNL_INTERFACE</a>



<a href="..\dispmprt\nc-dispmprt-dxgkcb_queue_dpc.md">DxgkCbQueueDpc</a>



<a href="..\dispmprt\nc-dispmprt-dxgkddi_start_device.md">DxgkDdiStartDevice</a>



<a href="..\d3dkmddi\nc-d3dkmddi-dxgkcb_notify_interrupt.md">DxgkCbNotifyInterrupt</a>



 

 


