---
UID: NF:ksproxy.IKsControl.KsEvent
title: IKsControl::KsEvent method
author: windows-driver-content
description: The KsEvent method enables or disables an event, along with any other defined support operations available on an event set.
old-location: stream\ikscontrol_ksevent.htm
old-project: stream
ms.assetid: b1ff6569-9568-40d8-b2a9-e63ce44720a2
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: IKsControl, IKsControl interface [Streaming Media Devices], KsEvent method, IKsControl::KsEvent, KsEvent method [Streaming Media Devices], KsEvent method [Streaming Media Devices], IKsControl interface, KsEvent,IKsControl.KsEvent, ksproxy/IKsControl::KsEvent, ksproxy_d7ef7fda-b615-4aa9-8528-aa66de81da5b.xml, stream.ikscontrol_ksevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ksproxy.h
req.include-header: Ksproxy.h
req.target-type: DesktopMobile
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
-	COM
api_location:
-	ksproxy.h
api_name:
-	IKsControl.KsEvent
product: Windows
targetos: Windows
req.typenames: PIPE_STATE
---

# IKsControl::KsEvent method


## -description


The <b>KsEvent</b> method enables or disables an event, along with any other defined support operations available on an event set. 


## -syntax


````
HRESULT KsEvent(
  [in, optional] PKSEVENT Event,
  [in]           ULONG    EventLength,
  [in, out]      LPVOID   EventData,
  [in]           ULONG    DataLength,
  [in, out]      ULONG    *BytesReturned
);
````


## -parameters




### -param Event [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff561744">KSEVENT</a> structure that describes an event to enable the event and <b>NULL</b> to disable the event.


### -param EventLength [in]

Size, in bytes, of the buffer at <i>Event</i> when the event is enabled and zero when the event is disabled. 


### -param EventData [in, out]

Pointer to a <a href="..\ks\ns-ks-kseventdata.md">KSEVENTDATA</a> structure that contains data for the event and buffer space that receives data for the event. 


### -param DataLength [in]

Size, in bytes, of the buffer at <i>EventData</i>. 


### -param BytesReturned [in, out]

Pointer to a variable that receives the size, in bytes, of the data that <b>KsEvent</b> stores in the buffer at <i>EventData</i>. 


## -returns



Returns NOERROR if successful; otherwise, returns an error code. If the call succeeds, the event is on the driver's list of events.




## -remarks



To disable an event, set <i>Event</i> to <b>NULL</b>, <i>EventLength</i> to zero, and <i>EventData</i> to the pointer to the <a href="..\ks\ns-ks-kseventdata.md">KSEVENTDATA</a> structure that was previously used to enable the event.

The <i>EventData</i> parameter of <b>IKsControl::KsEvent</b> contains a handle in <b>EventHandle.Event</b>. You can wait for the handle to become available and get notifications when the minidriver calls <b>Ks</b><i>Xxx</i><b>GenerateEvents</b> or <a href="..\strmini\nf-strmini-streamclassstreamnotification.md">StreamClassStreamNotification</a>.




## -see-also

<a href="..\ks\ns-ks-kseventdata.md">KSEVENTDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561744">KSEVENT</a>



<a href="..\ks\nf-ks-ksfiltergenerateevents.md">KsFilterGenerateEvents</a>



<a href="..\ks\nf-ks-kspingenerateevents.md">KsPinGenerateEvents</a>



 

 


