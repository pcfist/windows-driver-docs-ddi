---
UID: NS:netdispumdddi.MIRACAST_CHUNK_DATA
title: MIRACAST_CHUNK_DATA
author: windows-driver-content
description: Contains encode chunk data that is used when a user-mode driver calls the wireless display (Miracast) GetNextChunkData function.
old-location: display\miracast_chunk_data.htm
old-project: display
ms.assetid: 1ff4af0b-df1c-4529-9f80-c9e44d889a63
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: MIRACAST_CHUNK_DATA, MIRACAST_CHUNK_DATA structure [Display Devices], display.miracast_chunk_data, netdispumdddi/MIRACAST_CHUNK_DATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: netdispumdddi.h
req.include-header: Netdispumdddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
-	Netdispumdddi.h
api_name:
-	MIRACAST_CHUNK_DATA
product: Windows
targetos: Windows
req.typenames: MIRACAST_CHUNK_DATA
---

# MIRACAST_CHUNK_DATA structure


## -description


Contains encode chunk data that is used when a user-mode driver calls the wireless display (Miracast) <a href="..\netdispumdddi\nc-netdispumdddi-pfn_get_next_chunk_data.md">GetNextChunkData</a> function.


## -syntax


````
typedef struct {
  MIRACAST_CHUNK_INFO ChunkInfo;
  UINT                PrivateDriverDataSize;
  UCHAR               PrivateDriverData[1];
} MIRACAST_CHUNK_DATA;
````


## -struct-fields




### -field ChunkInfo

A <a href="..\netdispumdddi\ns-netdispumdddi-miracast_chunk_info.md">MIRACAST_CHUNK_INFO</a> encode chunk information structure that the user-mode display driver wants to report.


### -field PrivateDriverDataSize

The size, in bytes, of the buffer that <b>pPrivateDriverData</b> points to.


### -field PrivateDriverData

Private data, of type <b>UCHAR</b>, that the user-mode display driver sends when it calls the <a href="..\netdispumdddi\nc-netdispumdddi-pfn_get_next_chunk_data.md">GetNextChunkData</a> function.


## -see-also

<a href="..\netdispumdddi\nc-netdispumdddi-pfn_get_next_chunk_data.md">GetNextChunkData</a>



<a href="..\netdispumdddi\ns-netdispumdddi-miracast_chunk_info.md">MIRACAST_CHUNK_INFO</a>



 

 


