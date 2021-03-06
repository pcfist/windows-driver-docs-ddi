---
UID: NS:ntddrilapitypes.RILCALLERIDSETTINGS
title: RILCALLERIDSETTINGS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcalleridsettings.htm
old-project: netvista
ms.assetid: 3ba2cd72-4678-4ada-9777-12cbb6032628
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*LPRILCALLERIDSETTINGS, RILCALLERIDSETTINGS, RILCALLERIDSETTINGS structure [Network Drivers Starting with Windows Vista], netvista.rilcalleridsettings, ntddrilapitypes/RILCALLERIDSETTINGS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
-	RILCALLERIDSETTINGS
product: Windows
targetos: Windows
req.typenames: RILCALLERIDSETTINGS, *LPRILCALLERIDSETTINGS
---

# RILCALLERIDSETTINGS structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILCALLERIDSETTINGS {
  DWORD                         cbSize;
  DWORD                         dwParams;
  DWORD                         dwExecutor;
  RILSERVICESETTINGSSTATUS      dwStatus;
  RILSERVICEPROVISIONINGSTATUS  dwProvisioning;
} RILCALLERIDSETTINGS, RILCALLERIDSETTINGS;
````


## -struct-fields




### -field cbSize


### -field dwParams


### -field dwExecutor


### -field dwStatus


### -field dwProvisioning

