---
UID: NS:d3d10umddi.D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT
title: D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT
author: windows-driver-content
description: Contains the response to a QueryAuthenticatedChannel(D3D11_1) query with a D3D11_1DDI_AUTHENTICATED_QUERY_OUTPUT.QueryType value of D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE.
old-location: display\d3d11_1ddi_authenticated_query_device_handle_output.htm
old-project: display
ms.assetid: 3433fb92-b7e1-48c4-bd0b-98b794b3f454
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT, D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT structure [Display Devices], d3d10umddi/D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT, display.d3d11_1ddi_authenticated_query_device_handle_output
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
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
-	HeaderDef
api_location:
-	D3d10umddi.h
api_name:
-	D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT
product: Windows
targetos: Windows
req.typenames: D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT
---

# D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT structure


## -description


Contains the response to a <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_queryauthenticatedchannel.md">QueryAuthenticatedChannel(D3D11_1)</a> query with a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_authenticated_query_output.md">D3D11_1DDI_AUTHENTICATED_QUERY_OUTPUT</a>.<b>QueryType</b> value of <b>D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE</b>.


## -syntax


````
typedef struct D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT {
  D3D11_1DDI_AUTHENTICATED_QUERY_OUTPUT Output;
  HANDLE                                DeviceHandle;
} D3D11_1DDI_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT;
````


## -struct-fields




### -field Output

A <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_authenticated_query_output.md">D3D11_1DDI_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.


### -field DeviceHandle

A handle to the device.


## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_queryauthenticatedchannel.md">QueryAuthenticatedChannel(D3D11_1)</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_authenticated_query_output.md">D3D11_1DDI_AUTHENTICATED_QUERY_OUTPUT</a>



 

 


