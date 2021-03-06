---
UID: NS:hbaapi.HBA_FCPTargetMappingV2
title: HBA_FCPTargetMappingV2
author: windows-driver-content
description: The HBA_FCPTargetMappingV2 structure contains a variable length array of target mappings.
old-location: storage\hba_fcptargetmappingv2.htm
old-project: storage
ms.assetid: 2c241a38-c6b6-4c77-a8ba-be7ba2a8a701
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PHBA_FCPTARGETMAPPINGV2, HBA_FCPTARGETMAPPINGV2, HBA_FCPTARGETMAPPINGV2 structure [Storage Devices], HBA_FCPTargetMappingV2, HBA_FCPTargetMappingV2 structure [Storage Devices], PHBA_FCPTARGETMAPPINGV2, PHBA_FCPTARGETMAPPINGV2 structure pointer [Storage Devices], hbaapi/HBA_FCPTargetMappingV2, hbaapi/PHBA_FCPTARGETMAPPINGV2, storage.hba_fcptargetmappingv2, structs-Fibre_316084b2-47c7-46e2-aa1e-1d99a97de1cb.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hbaapi.h
req.include-header: Hbaapi.h
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
-	hbaapi.h
api_name:
-	HBA_FCPTARGETMAPPINGV2
product: Windows
targetos: Windows
req.typenames: HBA_FCPTARGETMAPPINGV2, *PHBA_FCPTARGETMAPPINGV2
---

# HBA_FCPTargetMappingV2 structure


## -description


The HBA_FCPTargetMappingV2 structure contains a variable length array of target mappings. 


## -syntax


````
typedef struct HBA_FCPTargetMappingV2 {
  HBA_UINT32         NumberOfEntries;
  HBA_FCPSCSIENTRYV2 entry[1];
} HBA_FCPTARGETMAPPINGV2, *PHBA_FCPTARGETMAPPINGV2;
````


## -struct-fields




### -field NumberOfEntries

Indicates the number of bindings.


### -field entry

Contains a variable length array of structures of type <a href="..\hbaapi\ns-hbaapi-hba_fcpscsientryv2.md">HBA_FcpScsiEntryV2</a> each of which defines a mapping between an operating system identifier, a logical unit ID descriptor (LUID) and the corresponding fibre channel protocol (FCP) identifier for a logical unit. 


## -see-also

<a href="..\hbaapi\nf-hbaapi-hba_getfcptargetmappingv2.md">HBA_GetFcpTargetMappingV2</a>



 

 


