---
UID: NS:msviddrv.tag_video_geterrortext_parms
title: tag_video_geterrortext_parms
author: windows-driver-content
description: "."
old-location: stream\video_geterrortext_parms.htm
old-project: stream
ms.assetid: 6CF06E9A-D6A1-42A7-9C34-44BC52713621
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*LPVIDEO_GETERRORTEXT_PARMS, LPVIDEO_GETERRORTEXT_PARMS, LPVIDEO_GETERRORTEXT_PARMS structure pointer [Streaming Media Devices], VIDEO_GETERRORTEXT_PARMS, VIDEO_GETERRORTEXT_PARMS structure [Streaming Media Devices], msviddrv/LPVIDEO_GETERRORTEXT_PARMS, msviddrv/VIDEO_GETERRORTEXT_PARMS, stream.video_geterrortext_parms, tag_video_geterrortext_parms"
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
-	VIDEO_GETERRORTEXT_PARMS
product: Windows
targetos: Windows
req.typenames: VIDEO_GETERRORTEXT_PARMS, *LPVIDEO_GETERRORTEXT_PARMS
---

# tag_video_geterrortext_parms structure


## -description





## -syntax


````
typedef struct tag_video_geterrortext_parms {
  DWORD  dwError;
#ifdef _WIN32
  LPWSTR lpText;
#else 
  LPSTR  lpText;
#endif 
  DWORD  dwLength;
} VIDEO_GETERRORTEXT_PARMS, *LPVIDEO_GETERRORTEXT_PARMS;
````


## -struct-fields




### -field dwError

Specifies the error number to identify.


### -field lpText

Specifies the text buffer to fill.

Specifies the text buffer to fill.


### -field dwLength

Specifies the size of the text buffer in characters.

