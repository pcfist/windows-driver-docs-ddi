---
UID: NF:midatlax.RxDestroyMidAtlas
title: RxDestroyMidAtlas function
author: windows-driver-content
description: RxDestroyMidAtlas destroys an existing instance of a MID_ATLAS data structure and frees the allocated memory.
old-location: ifsk\rxdestroymidatlas.htm
old-project: ifsk
ms.assetid: 9d5c08c8-8306-46e3-b10b-eeefe473d340
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: RxDestroyMidAtlas, RxDestroyMidAtlas function [Installable File System Drivers], ifsk.rxdestroymidatlas, midatlax/RxDestroyMidAtlas, rxref_3a954108-5744-4b47-87b7-7553d64ec038.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: midatlax.h
req.include-header: Midatlax.h
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
req.irql: "<= APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	midatlax.h
api_name:
-	RxDestroyMidAtlas
product: Windows
targetos: Windows
req.typenames: MCD_INIT_DATA, *PMCD_INIT_DATA
---

# RxDestroyMidAtlas function


## -description


<b>RxDestroyMidAtlas</b> destroys an existing instance of a MID_ATLAS data structure and frees the allocated memory. 


## -syntax


````
VOID RxDestroyMidAtlas(
   PRX_MID_ATLAS       pMidAtlas,
   PCONTEXT_DESTRUCTOR pContextDestructor
);
````


## -parameters




### -param MidAtlas

TBD


### -param ContextDestructor

TBD




#### - pContextDestructor

An associated context destructor.


#### - pMidAtlas

The MID_ATLAS structure to be freed.


## -returns



None 




## -remarks



RDBSS defines a Multiplex ID (MID), a 16-bit value, that can be used by both the network client (mini-redirector) and the server to distinguish between the concurrently active requests on any connection. A MID is part of a MID_ATLAS data structure allocated by calling <b>RxCreateMidAtlas</b>.

<b>RxDestroyMidAtlas</b> destroys a MID_ATLAS data structure previously created by a call to <b>RxCreateMidAtlas</b>. As a side effect, <b>RxDestroyMidAtlas</b> invokes the passed in context destructor on every valid context in the MID_ATLAS. 




## -see-also

<a href="..\midatlax\nf-midatlax-rxmapmidtocontext.md">RxMapMidToContext</a>



<a href="..\midatlax\nf-midatlax-rxreassociatemid.md">RxReassociateMid</a>



<a href="..\midatlax\nf-midatlax-rxmapanddissociatemidfromcontext.md">RxMapAndDissociateMidFromContext</a>



<a href="..\midatlax\nf-midatlax-rxcreatemidatlas.md">RxCreateMidAtlas</a>



<a href="..\midatlax\nf-midatlax-rxassociatecontextwithmid.md">RxAssociateContextWithMid</a>



 

 


