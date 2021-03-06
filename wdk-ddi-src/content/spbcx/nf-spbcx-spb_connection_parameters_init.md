---
UID: NF:spbcx.SPB_CONNECTION_PARAMETERS_INIT
title: SPB_CONNECTION_PARAMETERS_INIT function
author: windows-driver-content
description: The SPB_CONNECTION_PARAMETERS_INIT function initializes an SPB_CONNECTION_PARAMETERS structure.
old-location: spb\spb_connection_parameters_init.htm
old-project: SPB
ms.assetid: 0E23690B-4AE1-42F1-A53F-FE9A4697DBF2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SPB.spb_connection_parameters_init, SPB_CONNECTION_PARAMETERS_INIT, SPB_CONNECTION_PARAMETERS_INIT function [Buses], spbcx/SPB_CONNECTION_PARAMETERS_INIT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: spbcx.h
req.include-header: 
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
req.irql: Any IRQL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Spbcx.h
api_name:
-	SPB_CONNECTION_PARAMETERS_INIT
product: Windows
targetos: Windows
req.typenames: SPB_REQUEST_TYPE, *PSPB_REQUEST_TYPE
req.product: Windows 10 or later.
---

# SPB_CONNECTION_PARAMETERS_INIT function


## -description


The <b>SPB_CONNECTION_PARAMETERS_INIT</b> function initializes an  <a href="https://msdn.microsoft.com/library/windows/hardware/hh406204">SPB_CONNECTION_PARAMETERS</a> structure.


## -syntax


````
VOID SPB_CONNECTION_PARAMETERS_INIT(
  _Out_ SPB_CONNECTION_PARAMETERS *Parameters
);
````


## -parameters




### -param Parameters [out]

A pointer to the <b>SPB_CONNECTION_PARAMETERS</b> structure that is to be initialized.


## -returns



None.




## -remarks



Your SPB controller driver must use this function to initialize an <b>SPB_CONNECTION_PARAMETERS</b> structure before passing this structure as an output parameter to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh450926">SpbTargetGetConnectionParameters</a> method. This method writes the connection parameters for a target device on the bus to this structure.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/hh450926">SpbTargetGetConnectionParameters</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406204">SPB_CONNECTION_PARAMETERS</a>



 

 


