---
UID: NS:wwan._WWAN_USSD_REQUEST
title: "_WWAN_USSD_REQUEST"
author: windows-driver-content
description: The WWAN_USSD_REQUEST structure describes an Unstructured Supplementary Service Data (USSD) request.
old-location: netvista\wwan_ussd_request.htm
old-project: netvista
ms.assetid: 429F5EC9-F8AA-4D5D-9CA7-D9D9AEC46842
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PWWAN_USSD_REQUEST, PWWAN_USSD_REQUEST, PWWAN_USSD_REQUEST structure pointer [Network Drivers Starting with Windows Vista], WWAN_USSD_REQUEST, WWAN_USSD_REQUEST structure [Network Drivers Starting with Windows Vista], _WWAN_USSD_REQUEST, netvista.wwan_ussd_request, wwan/PWWAN_USSD_REQUEST, wwan/WWAN_USSD_REQUEST"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wwan.h
req.include-header: Wwan.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with  Windows 8.
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
-	wwan.h
api_name:
-	WWAN_USSD_REQUEST
product: Windows
targetos: Windows
req.typenames: WWAN_USSD_REQUEST, *PWWAN_USSD_REQUEST
req.product: Windows 10 or later.
---

# _WWAN_USSD_REQUEST structure


## -description


The WWAN_USSD_REQUEST structure describes an Unstructured Supplementary Service Data (USSD) request.


## -syntax


````
typedef struct _WWAN_USSD_REQUEST {
  WWAN_USSD_REQUEST_TYPE RequestType;
  WWAN_USSD_STRING       UssdString;
} WWAN_USSD_REQUEST, *PWWAN_USSD_REQUEST;
````


## -struct-fields




### -field RequestType

The type of USSD request.


### -field UssdString

The USSD string that accompanies the request.


## -see-also

<a href="..\wwan\ns-wwan-_wwan_ussd_string.md">WWAN_USSD_STRING</a>



<a href="..\wwan\ne-wwan-_wwan_ussd_request_type.md">WWAN_USSD_REQUEST_TYPE</a>



 

 


