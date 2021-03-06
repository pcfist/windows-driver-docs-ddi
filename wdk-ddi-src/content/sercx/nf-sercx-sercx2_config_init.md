---
UID: NF:sercx.SERCX2_CONFIG_INIT
title: SERCX2_CONFIG_INIT function
author: windows-driver-content
description: The SERCX2_CONFIG_INIT function initializes a SERCX2_CONFIG structure.
old-location: serports\sercx2_config_init.htm
old-project: serports
ms.assetid: 630C7EDA-8C6A-4BD7-9287-EA15FBA34408
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: 2/SERCX2_CONFIG_INIT, SERCX2_CONFIG_INIT, SERCX2_CONFIG_INIT function [Serial Ports], serports.sercx2_config_init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sercx.h
req.include-header: 
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
-	2.0\Sercx.h
api_name:
-	SERCX2_CONFIG_INIT
product: Windows
targetos: Windows
req.typenames: SERCX_STATUS, *PSERCX_STATUS
req.product: Windows 10 or later.
---

# SERCX2_CONFIG_INIT function


## -description


The <b>SERCX2_CONFIG_INIT</b> function initializes a <a href="..\sercx\ns-sercx-_sercx2_config.md">SERCX2_CONFIG</a> structure.


## -syntax


````
VOID SERCX2_CONFIG_INIT(
  _Out_ SERCX2_CONFIG           *Config,
  _In_  PFN_SERCX2_APPLY_CONFIG EvtSerCx2ApplyConfig,
  _In_  PFN_SERCX2_CONTROL      EvtSerCx2Control,
  _In_  PFN_SERCX2_PURGE_FIFOS  EvtSerCx2PurgeFifos
);
````


## -parameters




### -param Config [out]

A pointer to the <a href="..\sercx\ns-sercx-_sercx2_config.md">SERCX2_CONFIG</a> structure that is to be initialized.


### -param EvtSerCx2ApplyConfig [in]

The value to load into the <b>EvtSerCx2ApplyConfig</b> member of the <b>SERCX2_CONFIG</b> structure. For more information, see the description of this member in <a href="..\sercx\ns-sercx-_sercx2_config.md">SERCX2_CONFIG</a>.


### -param EvtSerCx2Control [in]

The value to load into the <b>EvtSerCx2Control</b> member of the <b>SERCX2_CONFIG</b> structure. For more information, see the description of this member in <a href="..\sercx\ns-sercx-_sercx2_config.md">SERCX2_CONFIG</a>.


### -param EvtSerCx2PurgeFifos [in]

The value to load into the <b>EvtSerCx2PurgeFifos</b> member of the <b>SERCX2_CONFIG</b> structure. For more information, see the description of this member in <a href="..\sercx\ns-sercx-_sercx2_config.md">SERCX2_CONFIG</a>.


## -returns



None.




## -remarks



Your serial controller driver must use this function to initialize a <a href="..\sercx\ns-sercx-_sercx2_config.md">SERCX2_CONFIG</a> structure before passing a pointer to this structure as an input parameter to the <a href="..\sercx\nf-sercx-sercx2initializedevice.md">SerCx2InitializeDevice</a> method.

<b>SERCX2_CONFIG_INIT</b> sets the <b>Size</b> member of the structure to <b>sizeof</b>(<b>SERCX2_CONFIG</b>), and sets three additional members of the structure to the values supplied as input parameters to the function. The function sets the other members of the structure to zero. The driver can, if necessary, explicitly set these other members to nonzero values after the <b>SERCX2_CONFIG_INIT</b> call.




## -see-also

<a href="..\sercx\nf-sercx-sercx2initializedevice.md">SerCx2InitializeDevice</a>



<a href="..\sercx\ns-sercx-_sercx2_config.md">SERCX2_CONFIG</a>



 

 


