---
UID: NS:msviddrv.tag_video_stream_init_parms
title: tag_video_stream_init_parms
author: windows-driver-content
description: "."
old-location: stream\video_stream_init_parms.htm
old-project: stream
ms.assetid: 0FEC5054-8045-4CE5-AA59-AE3D23568308
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*LPVIDEO_STREAM_INIT_PARMS, LPVIDEO_STREAM_INIT_PARMS, LPVIDEO_STREAM_INIT_PARMS structure pointer [Streaming Media Devices], VIDEO_STREAM_INIT_PARMS, VIDEO_STREAM_INIT_PARMS structure [Streaming Media Devices], msviddrv/LPVIDEO_STREAM_INIT_PARMS, msviddrv/VIDEO_STREAM_INIT_PARMS, stream.video_stream_init_parms, tag_video_stream_init_parms"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: msviddrv.h
req.include-header: 
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
req.irql: "<= APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msviddrv.h
api_name:
-	VIDEO_STREAM_INIT_PARMS
product: Windows
targetos: Windows
req.typenames: VIDEO_STREAM_INIT_PARMS, *LPVIDEO_STREAM_INIT_PARMS
---

# tag_video_stream_init_parms structure


## -description





## -syntax


````
typedef struct tag_video_stream_init_parms {
  DWORD  dwMicroSecPerFrame;
  DWORD  dwCallback;
  DWORD  dwCallbackInst;
  DWORD  dwFlags;
  HANDLE hVideo;
} VIDEO_STREAM_INIT_PARMS, *LPVIDEO_STREAM_INIT_PARMS;
````


## -struct-fields




### -field dwMicroSecPerFrame


### -field dwCallback


### -field dwCallbackInst


### -field dwFlags


### -field hVideo

