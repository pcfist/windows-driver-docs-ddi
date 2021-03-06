---
UID: NF:wudfddi.IWDFMemory.CopyToBuffer
title: IWDFMemory::CopyToBuffer method
author: windows-driver-content
description: The CopyToBuffer method safely copies data from a memory object to the specified target buffer.
old-location: wdf\iwdfmemory_copytobuffer.htm
old-project: wdf
ms.assetid: c5b34168-b3b8-4559-8b41-982f0a66f01d
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CopyToBuffer method, CopyToBuffer method, IWDFMemory interface, CopyToBuffer,IWDFMemory.CopyToBuffer, IWDFMemory, IWDFMemory interface, CopyToBuffer method, IWDFMemory::CopyToBuffer, UMDFMemoryObjectRef_40ff2a7e-f93c-4f95-ba14-b7ade765ab2d.xml, umdf.iwdfmemory_copytobuffer, wdf.iwdfmemory_copytobuffer, wudfddi/IWDFMemory::CopyToBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WUDFx.dll
api_name:
-	IWDFMemory.CopyToBuffer
product: Windows
targetos: Windows
req.typenames: POWER_ACTION, *PPOWER_ACTION
req.product: Windows 10 or later.
---

# IWDFMemory::CopyToBuffer method


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>CopyToBuffer</b> method safely copies data from a memory object to the specified target buffer.


## -syntax


````
HRESULT CopyToBuffer(
  [in]  ULONG_PTR SourceOffset,
  [out] void      *pTargetBuffer,
  [in]  SIZE_T    NumOfBytesToCopyTo
);
````


## -parameters




### -param SourceOffset [in]

The offset, in bytes, into the memory object to start to copy data from. 


### -param TargetBuffer




### -param NumOfBytesToCopyTo [in]

The number of bytes to copy to the buffer that <i>pTargetBuffer</i> points to.


#### - pTargetBuffer [out]

A pointer to the target buffer that data is copied to.


## -returns



<b>CopyToBuffer</b> returns S_OK if the operation succeeds. Otherwise, this method returns one of the error codes that are defined in Winerror.h.




## -see-also

<a href="..\wudfddi\nn-wudfddi-iwdfmemory.md">IWDFMemory</a>



 

 


