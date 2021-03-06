---
UID: NF:wdm.ExInitializeSetTimerParameters
title: ExInitializeSetTimerParameters function
author: windows-driver-content
description: The ExInitializeSetTimerParameters routine initializes an EXT_SET_PARAMETERS structure.
old-location: kernel\exinitializesettimerparameters.htm
old-project: kernel
ms.assetid: 43A07E6E-C69F-4D6C-9B9C-EB7FFDF7651E
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: ExInitializeSetTimerParameters, ExInitializeSetTimerParameters routine [Kernel-Mode Driver Architecture], kernel.exinitializesettimerparameters, wdm/ExInitializeSetTimerParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Desktop
req.target-min-winverclnt: Available starting with Windows 8.1.
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
req.irql: Any level.
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdm.h
api_name:
-	ExInitializeSetTimerParameters
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# ExInitializeSetTimerParameters function


## -description


The <b>ExInitializeSetTimerParameters</b> routine initializes an <a href="..\wdm\ns-wdm-_ext_set_parameters_v0.md">EXT_SET_PARAMETERS</a> structure.


## -syntax


````
VOID ExInitializeSetTimerParameters(
  _Out_ PEXT_SET_PARAMETERS Parameters
);
````


## -parameters




### -param Parameters [out]

A pointer to the <b>EXT_SET_PARAMETER</b> structure that is to be initialized.


## -returns



None.




## -remarks



Your driver must call <b>ExInitializeSetTimerParameters</b> to initialize an <b>EXT_SET_PARAMETERS</b> structure before the driver passes this structure to the <a href="..\wdm\nf-wdm-exsettimer.md">ExSetTimer</a> routine. For more information about the member values that <b>ExInitializeSetTimerParameters</b> writes to the members of this structure, see <a href="..\wdm\ns-wdm-_ext_set_parameters_v0.md">EXT_SET_PARAMETERS</a>.




## -see-also

<a href="..\wdm\nf-wdm-exsettimer.md">ExSetTimer</a>



<a href="..\wdm\ns-wdm-_ext_set_parameters_v0.md">EXT_SET_PARAMETERS</a>



 

 


