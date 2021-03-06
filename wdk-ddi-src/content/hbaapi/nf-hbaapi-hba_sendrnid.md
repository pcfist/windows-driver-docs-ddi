---
UID: NF:hbaapi.HBA_SendRNID
title: HBA_SendRNID function
author: windows-driver-content
description: The HBA_SendRNID routine sends a request for node identification data (RNID) to the indicated HBA, which in turn routes the request through the indicated port or node to the appropriate fabric configuration server.
old-location: storage\hba_sendrnid.htm
old-project: storage
ms.assetid: c15d74c8-bc04-4d82-a729-6b13f778b8c7
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: HBA_SendRNID, HBA_SendRNID routine [Storage Devices], fibreHBA_rtns_fd816d59-9c64-499e-a3bb-2a2d2427fbf9.xml, hbaapi/HBA_SendRNID, storage.hba_sendrnid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: hbaapi.h
req.include-header: Hbaapi.h
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
req.lib: Hbaapi.lib
req.dll: Hbaapi.dll
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Hbaapi.dll
api_name:
-	HBA_SendRNID
product: Windows
targetos: Windows
req.typenames: HBA_WWNTYPE
---

# HBA_SendRNID function


## -description


The <b>HBA_SendRNID</b> routine sends a request for node identification data (RNID) to the indicated HBA, which in turn routes the request through the indicated port or node to the appropriate fabric configuration server. 


## -syntax


````
HBA_STATUS HBA_API HBA_SendRNID(
  _In_    HBA_HANDLE  HbaHandle,
  _In_    HBA_WWN     Wwn,
  _In_    HBA_WWNTYPE WwnType,
  _Out_   void        *pRspBuffer,
  _Inout_ HBA_UINT32  *RspBufferSize
);
````


## -parameters




### -param Handle

TBD


### -param Wwn [in]

Contains a 64-bit worldwide name (WWN) that uniquely identifies a port or a node from which the RNID command is issued. For a discussion of worldwide names, see the T11 committee's <i>Fibre Channel HBA API</i> specification. 


### -param WnnType

TBD


### -param pRspBuffer [out]

Pointer to a buffer that contains, in big-endian (wire) format, the payload data from the reply to the node identification request. 


### -param RspBufferSize [in, out]

On input, indicates the size, in bytes, of the buffer pointed to by <i>pRspBuffer</i>. On return, this member indicates the size, in bytes, of the response data. 


#### - HbaHandle [in]

Contains a value returned by the routine <a href="..\hbaapi\nf-hbaapi-hba_openadapter.md">HBA_OpenAdapter</a> that identifies the HBA that will route the command. The HBA routes this command to the appropriate fabric configuration server. 


#### - WwnType [in]

Contains an enumerator value of type <a href="..\hbaapi\ne-hbaapi-hba_wwntype.md">HBA_wwntype</a> that indicates whether the WWN specified by <i>Wwn </i>is a port or a node:


## -returns



The <b>HBA_SendRNID</b> routine returns a value of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a> that indicates the status of the HBA.




## -remarks



The node identification data request is a common transport (CT) command that queries a fabric configuration server for node identification data. For a complete description of this command, see the sections dealing with node identification requests in the <i>Fibre Channel Generic Services - 4 (FC-GS-4)</i> specification published by the ANSI committee.

The <b>HBA_SendRNID</b> library routine serves a purpose very similar to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565459">SendRNID</a> WMI method. 




## -see-also

<a href="..\hbaapi\nf-hbaapi-hba_sendrnid.md">HBA_SendRNID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565459">SendRNID</a>



 

 


