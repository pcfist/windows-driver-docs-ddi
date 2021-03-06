---
UID: NF:printerextension.IPrinterExtensionContext.get_PrinterQueue
title: IPrinterExtensionContext::get_PrinterQueue method
author: windows-driver-content
description: Gets the queue for the printer.
old-location: print\iprinterextensioncontext_printerqueue.htm
old-project: print
ms.assetid: 304C8AF5-EA4E-4401-A8EC-6E1B279038E8
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: IPrinterExtensionContext, IPrinterExtensionContext interface [Print Devices], PrinterQueue property, IPrinterExtensionContext.PrinterQueue, IPrinterExtensionContext::get_PrinterQueue, PrinterQueue property [Print Devices], PrinterQueue property [Print Devices], IPrinterExtensionContext interface, get_PrinterQueue, get_PrinterQueue,IPrinterExtensionContext.get_PrinterQueue, print.iprinterextensioncontext_printerqueue, printerextension/IPrinterExtensionContext::PrinterQueue, printerextension/IPrinterExtensionContext::get_PrinterQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
-	COM
api_location:
-	Printerextension.h
api_name:
-	IPrinterExtensionContext.PrinterQueue
-	IPrinterExtensionContext.get_PrinterQueue
product: Windows
targetos: Windows
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrinterExtensionContext::get_PrinterQueue method


## -description


Gets the queue for the printer.

This property is read-only.


## -syntax


````
HRESULT get_PrinterQueue(
  [out, retval] IPrinterQueue **ppQueue
);
````


## -parameters


## -see-also

<a href="..\printerextension\nn-printerextension-iprinterextensioncontext.md">IPrinterExtensionContext</a>



<a href="..\printerextension\nn-printerextension-iprinterqueue.md">IPrinterQueue</a>



 

 


