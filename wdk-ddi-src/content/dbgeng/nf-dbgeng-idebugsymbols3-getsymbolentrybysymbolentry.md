---
UID: NF:dbgeng.IDebugSymbols3.GetSymbolEntryBySymbolEntry
title: IDebugSymbols3::GetSymbolEntryBySymbolEntry method
author: windows-driver-content
description: Allows navigation within the symbol entry hierarchy.
old-location: debugger\idebugsymbols3_getsymbolentrybysymbolentry.htm
old-project: debugger
ms.assetid: 39AD3C10-C6E8-463F-BDDE-5941CB4B2830
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetSymbolEntryBySymbolEntry method [Windows Debugging], GetSymbolEntryBySymbolEntry method [Windows Debugging], IDebugSymbols3 interface, GetSymbolEntryBySymbolEntry,IDebugSymbols3.GetSymbolEntryBySymbolEntry, IDebugSymbols3, IDebugSymbols3 interface [Windows Debugging], GetSymbolEntryBySymbolEntry method, IDebugSymbols3::GetSymbolEntryBySymbolEntry, dbgeng/IDebugSymbols3::GetSymbolEntryBySymbolEntry, debugger.idebugsymbols3_getsymbolentrybysymbolentry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
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
-	COM
api_location:
-	Dbgeng.h
api_name:
-	IDebugSymbols3.GetSymbolEntryBySymbolEntry
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugSymbols3::GetSymbolEntryBySymbolEntry method


## -description


Allows navigation within the
    symbol entry hierarchy.


## -syntax


````
HRESULT GetSymbolEntryBySymbolEntry(
  [in]  PDEBUG_MODULE_AND_ID FromId,
  [in]  ULONG                Flags,
  [out] PDEBUG_MODULE_AND_ID ToId
);
````


## -parameters




### -param FromId [in]

A pointer to a <a href="..\dbgeng\ns-dbgeng-_debug_module_and_id.md">DEBUG_MODULE_AND_ID</a> structure as the input ID.


### -param Flags [in]

A bit-set that contains options that affect the behavior of this method. 


### -param ToId [out]

A pointer to a <a href="..\dbgeng\ns-dbgeng-_debug_module_and_id.md">DEBUG_MODULE_AND_ID</a> structure as the output ID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>



<a href="..\dbgeng\ns-dbgeng-_debug_module_and_id.md">DEBUG_MODULE_AND_ID</a>



 

 


