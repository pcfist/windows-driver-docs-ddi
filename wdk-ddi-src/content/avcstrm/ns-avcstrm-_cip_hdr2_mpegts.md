---
UID: NS:avcstrm._CIP_HDR2_MPEGTS
title: "_CIP_HDR2_MPEGTS"
author: windows-driver-content
description: The CIP_HDR2_MPEGTS structure describes the second quadlet of a CIP header pair for an MPEGTS format stream.
old-location: stream\cip_hdr2_mpegts.htm
old-project: stream
ms.assetid: e1f46926-8c2b-46ff-9adb-5332fba17e3b
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PCIP_HDR2_MPEGTS, CIP_HDR2_MPEGTS, CIP_HDR2_MPEGTS structure [Streaming Media Devices], PCIP_HDR2_MPEGTS, PCIP_HDR2_MPEGTS structure pointer [Streaming Media Devices], _CIP_HDR2_MPEGTS, avcsref_80577192-cbb5-401a-a840-5970841111ab.xml, avcstrm/CIP_HDR2_MPEGTS, avcstrm/PCIP_HDR2_MPEGTS, stream.cip_hdr2_mpegts"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: avcstrm.h
req.include-header: Avcstrm.h
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
-	HeaderDef
api_location:
-	avcstrm.h
api_name:
-	CIP_HDR2_MPEGTS
product: Windows
targetos: Windows
req.typenames: CIP_HDR2_MPEGTS, *PCIP_HDR2_MPEGTS
---

# _CIP_HDR2_MPEGTS structure


## -description


The CIP_HDR2_MPEGTS structure describes the second quadlet of a CIP header pair for an MPEGTS format stream.


## -syntax


````
typedef struct _CIP_HDR2_MPEGTS {
  ULONG TSF  :1;
  ULONG RSV23bit  :23;
  ULONG FMT  :6;
  ULONG Bit10  :2;
} CIP_HDR2_MPEGTS, *PCIP_HDR2_MPEGTS;
````


## -struct-fields




### -field TSF

Time-shift flag. This is not used for opening a stream.


### -field RSV23bit

Reserved bits. This must be 0. Do not use this.


### -field FMT

CIP format. For example, 000000 = DV and 100000 = MPEGTS.


### -field Bit10

Must be set to 1:0


## -see-also

<a href="..\avcstrm\ns-avcstrm-_cip_hdr1.md">CIP_HDR1</a>



 

 


