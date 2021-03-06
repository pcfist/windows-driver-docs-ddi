---
UID: NF:wdfdevice.WdfDeviceReadFromHardware
title: WdfDeviceReadFromHardware function
author: windows-driver-content
description: The WdfDeviceReadFromHardware method is used internally by the framework. Do not use.
old-location: wdf\wdfdevicereadfromhardware.htm
old-project: wdf
ms.assetid: 3E9ECB09-39DD-4A16-B096-24AAD96D52E9
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFN_WDFDEVICEREADFROMHARDWARE, WdfDeviceReadFromHardware, WdfDeviceReadFromHardware method, wdf.wdfdevicereadfromhardware, wdfdevice/WdfDeviceReadFromHardware, wdfhwaccess/WdfDeviceReadFromHardware
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfdevice.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.11
req.umdf-ver: 2.0
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (see Framework Library Versioning.)
req.dll: 
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Wdf01000.sys
-	Wdf01000.sys.dll
api_name:
-	WdfDeviceReadFromHardware
product: Windows
targetos: Windows
req.typenames: WDF_STATE_NOTIFICATION_TYPE
req.product: Windows 10 or later.
---

# WdfDeviceReadFromHardware function


## -description


The <b>WdfDeviceReadFromHardware</b> method is used internally by the framework. Do not use.

Instead, use the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265662">WDF Register/Port Access Functions</a>.


## -syntax


````
SIZE_T WdfDeviceReadFromHardware(
  _In_      WDFDEVICE                       Device,
  _In_      WDF_DEVICE_HWACCESS_TARGET_TYPE Type,
  _In_      WDF_DEVICE_HWACCESS_TARGET_SIZE Size,
  _In_      PVOID                           TargetAddress,
  _Out_opt_ PVOID                           Buffer,
  _In_opt_  ULONG                           Count
);
````


## -parameters




### -param Device [in]


### -param Type [in]


### -param Size [in]


### -param TargetAddress [in]


### -param Buffer [out, optional]


### -param Count [in, optional]


## -see-also

<a href="https://msdn.microsoft.com/19B472D0-D607-4874-ADB9-232C379B0DFD">ReadFromHardware</a>



 

 


