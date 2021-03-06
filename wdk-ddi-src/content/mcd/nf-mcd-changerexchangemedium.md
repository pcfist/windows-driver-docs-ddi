---
UID: NF:mcd.ChangerExchangeMedium
title: ChangerExchangeMedium function
author: windows-driver-content
description: ChangerExchangeMedium handles the device-specific aspects of a device-control IRP with the IOCTL code IOCTL_CHANGER_EXCHANGE_MEDIUM.
old-location: storage\changerexchangemedium.htm
old-project: storage
ms.assetid: 4cb6e9af-ddd0-48d9-9f07-43c828e4187b
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: ChangerExchangeMedium, ChangerExchangeMedium function [Storage Devices], chgrmini_1a4e68fa-4ef3-4f1e-ab2c-ca26b138fc14.xml, mcd/ChangerExchangeMedium, storage.changerexchangemedium
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mcd.h
req.include-header: Mcd.h, Ntddchgr.h
req.target-type: Desktop
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mcd.h
api_name:
-	ChangerExchangeMedium
product: Windows
targetos: Windows
req.typenames: LAMP_INTENSITY_WHITE
---

# ChangerExchangeMedium function


## -description


<b>ChangerExchangeMedium</b> handles the device-specific aspects of a device-control IRP with the IOCTL code <a href="..\ntddchgr\ni-ntddchgr-ioctl_changer_exchange_medium.md">IOCTL_CHANGER_EXCHANGE_MEDIUM</a>. 


## -syntax


````
NTSTATUS ChangerExchangeMedium(
  _In_ PDEVICE_OBJECT DeviceObject,
  _In_ PIRP           Irp
);
````


## -parameters




### -param DeviceObject [in]

Pointer to the device object that represents the changer. 


### -param Irp [in]

Pointer to the IRP. 


## -returns



If the changer supports exchanging media, <b>ChangerExchangeMedium</b> returns the status returned by the system port driver, or one of the following values:
      

STATUS_SUCCESS

STATUS_DESTINATION_ELEMENT_FULL

STATUS_INVALID_ELEMENT_ADDRESS

STATUS_SOURCE_ELEMENT_EMPTY

If the changer does not support exchanging media, ChangerExchangeMedium returns STATUS_INVALID_DEVICE_REQUEST.




## -remarks



This routine is required.

<b>ChangerExchangeMedium</b> moves a piece of media from a source element to one destination and from that destination to another destination. The source and second destination are often the same, resulting in a simple exchange of media.

The CHANGER_EXCHANGE_MEDIA flag in <b>Features0</b> of the <a href="..\ntddchgr\ns-ntddchgr-_get_changer_parameters.md">GET_CHANGER_PARAMETERS</a> structure indicates whether the changer supports this functionality. A changer that supports exchanging media typically has two picker mechanisms on a single transport element, or at least two transport elements. A changer that has a single picker mechanism might support exchanging medium through emulation of the command. 

The changer class driver checks the input buffer length in the I/O stack location before calling a miniclass driver's <b>ChangerExchangeMedium</b> routine. <i>Irp</i><b>-&gt;SystemBuffer</b> points to a <a href="..\ntddchgr\ns-ntddchgr-_changer_exchange_medium.md">CHANGER_EXCHANGE_MEDIUM</a> structure as an input parameter that indicates the transport element and the destination to set. 

<b>ChangerExchangeMedium</b> first verifies that the transport, source, and destination element addresses are valid, then converts zero-based element addresses to device-specific element addresses. It then builds an SRB with a CDB to exchange the media and sends it to the system port driver. 




## -see-also

<a href="..\ntddchgr\ns-ntddchgr-_changer_element.md">CHANGER_ELEMENT</a>



<a href="..\ntddchgr\ns-ntddchgr-_get_changer_parameters.md">GET_CHANGER_PARAMETERS</a>



<a href="..\ntddchgr\ns-ntddchgr-_changer_exchange_medium.md">CHANGER_EXCHANGE_MEDIUM</a>



<a href="..\mcd\nf-mcd-changermovemedium.md">ChangerMoveMedium</a>



 

 


