---
UID: NE:ksproxy.PIPE_ALLOCATOR_PLACE
title: PIPE_ALLOCATOR_PLACE
author: windows-driver-content
description: "."
old-location: stream\pipe_allocator_place.htm
old-project: stream
ms.assetid: 86B1D8BB-7213-403C-8EAB-D681A5DBF49E
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PPIPE_ALLOCATOR_PLACE, PIPE_ALLOCATOR_PLACE, PIPE_ALLOCATOR_PLACE enumeration [Streaming Media Devices], Pipe_Allocator_FirstPin, Pipe_Allocator_LastPin, Pipe_Allocator_MiddlePin, Pipe_Allocator_None, ksproxy/PIPE_ALLOCATOR_PLACE, ksproxy/Pipe_Allocator_FirstPin, ksproxy/Pipe_Allocator_LastPin, ksproxy/Pipe_Allocator_MiddlePin, ksproxy/Pipe_Allocator_None, stream.pipe_allocator_place"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ksproxy.h
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ksproxy.h
api_name:
-	PIPE_ALLOCATOR_PLACE
product: Windows
targetos: Windows
req.typenames: PIPE_ALLOCATOR_PLACE
---

# PIPE_ALLOCATOR_PLACE enumeration


## -description





## -syntax


````
typedef enum  { 
  Pipe_Allocator_None,
  Pipe_Allocator_FirstPin,
  Pipe_Allocator_LastPin,
  Pipe_Allocator_MiddlePin
} PIPE_ALLOCATOR_PLACE;
````


## -enum-fields




### -field Pipe_Allocator_None


### -field Pipe_Allocator_FirstPin


### -field Pipe_Allocator_LastPin


### -field Pipe_Allocator_MiddlePin

