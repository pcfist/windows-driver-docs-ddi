---
UID: NE:ntddrilapitypes.RILREGSTATUSINFOPARAMMASK
title: RILREGSTATUSINFOPARAMMASK
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilregstatusinfoparammask.htm
old-project: netvista
ms.assetid: 7857f845-d695-4b0f-9e52-8871c0140a74
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: RILREGSTATUSINFOPARAMMASK, RILREGSTATUSINFOPARAMMASK enumeration [Network Drivers Starting with Windows Vista], RIL_PARAM_REGSI_ACCESSTECHNOLOGY, RIL_PARAM_REGSI_ALL, RIL_PARAM_REGSI_CURRENTOPERATOR, RIL_PARAM_REGSI_HUICCAPP, RIL_PARAM_REGSI_NETWORKCODE, RIL_PARAM_REGSI_REGREJECTREASON, RIL_PARAM_REGSI_REGSTATUS, RIL_PARAM_REGSI_SYSTEMCAPS, RIL_PARAM_REGSI_VOICEDOMAIN, netvista.rilregstatusinfoparammask, ntddrilapitypes/RILREGSTATUSINFOPARAMMASK, ntddrilapitypes/RIL_PARAM_REGSI_ACCESSTECHNOLOGY, ntddrilapitypes/RIL_PARAM_REGSI_ALL, ntddrilapitypes/RIL_PARAM_REGSI_CURRENTOPERATOR, ntddrilapitypes/RIL_PARAM_REGSI_HUICCAPP, ntddrilapitypes/RIL_PARAM_REGSI_NETWORKCODE, ntddrilapitypes/RIL_PARAM_REGSI_REGREJECTREASON, ntddrilapitypes/RIL_PARAM_REGSI_REGSTATUS, ntddrilapitypes/RIL_PARAM_REGSI_SYSTEMCAPS, ntddrilapitypes/RIL_PARAM_REGSI_VOICEDOMAIN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddrilapitypes.h
req.include-header: Rilapitypes.h
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
-	ntddrilapitypes.h
api_name:
-	RILREGSTATUSINFOPARAMMASK
product: Windows
targetos: Windows
req.typenames: RILREGSTATUSINFOPARAMMASK
---

# RILREGSTATUSINFOPARAMMASK enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef enum _RILREGSTATUSINFOPARAMMASK { 
  RIL_PARAM_REGSI_HUICCAPP,
  RIL_PARAM_REGSI_REGSTATUS,
  RIL_PARAM_REGSI_ACCESSTECHNOLOGY,
  RIL_PARAM_REGSI_SYSTEMCAPS,
  RIL_PARAM_REGSI_REGREJECTREASON,
  RIL_PARAM_REGSI_CURRENTOPERATOR,
  RIL_PARAM_REGSI_VOICEDOMAIN,
  RIL_PARAM_REGSI_NETWORKCODE,
  RIL_PARAM_REGSI_ALL
} RILREGSTATUSINFOPARAMMASK;
````


## -enum-fields




### -field RIL_PARAM_REGSI_EXECUTOR


### -field RIL_PARAM_REGSI_HUICCAPP


### -field RIL_PARAM_REGSI_REGSTATUS


### -field RIL_PARAM_REGSI_ACCESSTECHNOLOGY


### -field RIL_PARAM_REGSI_SYSTEMCAPS


### -field RIL_PARAM_REGSI_REGREJECTREASON


### -field RIL_PARAM_REGSI_CURRENTOPERATOR


### -field RIL_PARAM_REGSI_VOICEDOMAIN


### -field RIL_PARAM_REGSI_NETWORKCODE


### -field RIL_PARAM_REGSI_ALL

