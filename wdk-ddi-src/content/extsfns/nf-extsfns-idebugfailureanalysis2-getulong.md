---
UID: NF:extsfns.IDebugFailureAnalysis2.GetUlong
title: IDebugFailureAnalysis2::GetUlong method
author: windows-driver-content
description: The GetUlong method searches a DebugFailureAnalysis object for the first FA entry that has a specified tag. If it finds an FA entry with the specified tag, it gets the ULONG value from the entry's data block.
old-location: debugger\idebugfailureanalysis2_getulong.htm
old-project: debugger
ms.assetid: 3926D55C-0EF6-4E15-B919-CB9E5137DC14
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetUlong method [Windows Debugging], GetUlong method [Windows Debugging], IDebugFailureAnalysis2 interface, GetUlong,IDebugFailureAnalysis2.GetUlong, IDebugFailureAnalysis2, IDebugFailureAnalysis2 interface [Windows Debugging], GetUlong method, IDebugFailureAnalysis2::GetUlong, debugger.idebugfailureanalysis2_getulong, extsfns/IDebugFailureAnalysis2::GetUlong
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: extsfns.h
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	extsfns.h
api_name:
-	IDebugFailureAnalysis2.GetUlong
product: Windows
targetos: Windows
req.typenames: FA_EXTENSION_PLUGIN_PHASE
---

# IDebugFailureAnalysis2::GetUlong method


## -description


The <b>GetUlong</b> method searches a <a href="..\extsfns\nn-extsfns-idebugfailureanalysis2.md">DebugFailureAnalysis</a> object for the first <a href="https://msdn.microsoft.com/759DE159-F2A8-4BB1-AAF5-B2B91C4F91B0">FA entry</a> that has a specified tag. If it finds an FA entry with the specified tag, it gets the <b>ULONG</b> value from the entry's data block.


## -syntax


````
PFA_ENTRY GetUlong(
        FA_TAG Tag,
  [out] PULONG Value
);
````


## -parameters




### -param Tag

A value in the <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/writing-an-analysis-extension-to-extend--analyze">FA_TAG</a> enumeration.


### -param Value [out]

A pointer to a <b>ULONG</b> that receives the value from the entry's data block.


## -returns



If this method finds an <a href="https://msdn.microsoft.com/759DE159-F2A8-4BB1-AAF5-B2B91C4F91B0">FA entry</a> with the specified tag, and if it succeeds in getting the data block, it returns a pointer to the <a href="..\extsfns\ns-extsfns-_fa_entry.md">FA_ENTRY</a> structure. Otherwise, it returns <b>NULL</b>.




## -remarks



If this method finds an <a href="https://msdn.microsoft.com/759DE159-F2A8-4BB1-AAF5-B2B91C4F91B0">FA entry</a> with the specified tag, it checks to see whether the <b>DataSize</b> member of the <a href="..\extsfns\ns-extsfns-_fa_entry.md">FA_ENTRY</a> structure is equal to the size of a <b>ULONG</b>. If <b>DataSize</b> is not equal to the size of a <b>ULONG</b>, this method returns <b>NULL</b> and does not get the data block.

Each tag that has already been used in a <a href="..\extsfns\nn-extsfns-idebugfailureanalysis2.md">DebugFailureAnalysis</a> object is associated with one of the data types in the <a href="..\extsfns\ne-extsfns-_fa_entry_type.md">FA_ENTRY_TYPE</a> enumeration. To determine the data type associated with a tag, call the <a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a> method of the <a href="..\extsfns\nn-extsfns-idebugfaentrytags.md">IDebugFAEntryTags</a> interface. To get a pointer to an IDebugFAEntryTags interface, call the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983414">GetDebugFATagControl</a> method of the <b>IDebugFailureAnalysis2</b> interface.

The appropriate use of this method is get the data block from an <a href="https://msdn.microsoft.com/759DE159-F2A8-4BB1-AAF5-B2B91C4F91B0">FA entry</a> that has a data type of <b>DEBUG_FA_ENTRY_ULONG</b>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/jj983425">SetUlong</a>



<a href="..\extsfns\nn-extsfns-idebugfailureanalysis2.md">IDebugFailureAnalysis2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj983409">AddUlong</a>



<a href="https://msdn.microsoft.com/7648F789-85D5-4247-90DD-2EAA43543483">Writing an Analysis Extension Plug-in to Extend !analyze</a>



<a href="..\extsfns\nc-extsfns-ext_analysis_plugin.md">_EFN_Analyze</a>



 

 


