---
UID: NF:wpprecorder.imp_WppRecorderLogGetDefault
title: imp_WppRecorderLogGetDefault function
author: windows-driver-content
description: The WppRecorderLogGetDefault method gets a handle to the default recorder log.
old-location: devtest\wpprecorderloggetdefault.htm
old-project: devtest
ms.assetid: 823E9AA6-F838-41B1-A502-A983B7F24661
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: WppRecorderLogGetDefault, devtest.wpprecorderloggetdefault, imp_WppRecorderLogGetDefault, imp_WppRecorderLogGetDefault function [Driver Development Tools], wpprecorder/imp_WppRecorderLogGetDefault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wpprecorder.h
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
-	Wpprecorder.h
api_name:
-	imp_WppRecorderLogGetDefault
product: Windows
targetos: Windows
req.typenames: WNODE_HEADER, *PWNODE_HEADER
req.product: Windows 10 or later.
---

# imp_WppRecorderLogGetDefault function


## -description


The <b>WppRecorderLogGetDefault</b> method gets a handle to the default recorder log.


## -syntax


````
RECORDER_LOG imp_WppRecorderLogGetDefault(void);
````


## -parameters




### -param WppCb

TBD




## -returns



An opaque handle to the default log.




## -see-also

<a href="..\wpprecorder\nf-wpprecorder-imp_wpprecorderisdefaultlogavailable.md">WppRecorderIsDefaultLogAvailable</a>



 

 


