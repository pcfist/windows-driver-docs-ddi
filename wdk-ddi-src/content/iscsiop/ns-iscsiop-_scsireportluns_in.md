---
UID: NS:iscsiop._ScsiReportLuns_IN
title: "_ScsiReportLuns_IN"
author: windows-driver-content
description: The ScsiReportLuns_IN structure holds the input data for the ScsiReportLuns method.
old-location: storage\scsireportluns_in.htm
old-project: storage
ms.assetid: ba1d67f7-cb90-473a-849d-7990889e4a40
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PScsiReportLuns_IN, PScsiReportLuns_IN, PScsiReportLuns_IN structure pointer [Storage Devices], ScsiReportLuns_IN, ScsiReportLuns_IN structure [Storage Devices], _ScsiReportLuns_IN, iscsiop/PScsiReportLuns_IN, iscsiop/ScsiReportLuns_IN, storage.scsireportluns_in, structs-iSCSI_1bc2b9de-bb9a-417a-bbe3-07167f866b7b.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iscsiop.h
req.include-header: Iscsiop.h
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
-	iscsiop.h
api_name:
-	ScsiReportLuns_IN
product: Windows
targetos: Windows
req.typenames: ScsiReportLuns_IN, *PScsiReportLuns_IN
---

# _ScsiReportLuns_IN structure


## -description


The ScsiReportLuns_IN structure holds the input data for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564918">ScsiReportLuns</a> method.


## -syntax


````
typedef struct _ScsiReportLuns_IN {
  ULONGLONG UniqueSessionId;
} ScsiReportLuns_IN, *PScsiReportLuns_IN;
````


## -struct-fields




### -field UniqueSessionId

A 64-bit integer that uniquely identifies the session. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff561599">LoginToTarget</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff550121">AddConnectionToSession</a> methods both return this value in their <i>UniqueSessionId</i> parameter. 


## -remarks



You must implement this method.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff561599">LoginToTarget</a>



<a href="..\iscsiop\ns-iscsiop-_scsireportluns_out.md">ScsiReportLuns_OUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550121">AddConnectionToSession</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564918">ScsiReportLuns</a>



 

 


