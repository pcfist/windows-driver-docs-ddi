---
UID: NF:wudfddi.IWDFDevice2.GetDeviceStackIoTypePreference
title: IWDFDevice2::GetDeviceStackIoTypePreference method
author: windows-driver-content
description: The GetDeviceStackIoTypePreference method retrieves the buffer access methods that the framework is using for a device.
old-location: wdf\iwdfdevice2_getdevicestackiotypepreference.htm
old-project: wdf
ms.assetid: 3a1f6432-3f61-4502-ac98-fa984539f88e
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: GetDeviceStackIoTypePreference method, GetDeviceStackIoTypePreference method, IWDFDevice2 interface, GetDeviceStackIoTypePreference,IWDFDevice2.GetDeviceStackIoTypePreference, IWDFDevice2, IWDFDevice2 interface, GetDeviceStackIoTypePreference method, IWDFDevice2::GetDeviceStackIoTypePreference, UMDFDeviceObjectRef_f6402826-fe3b-46c7-a4a8-d1d4f74e4b5c.xml, umdf.iwdfdevice2_getdevicestackiotypepreference, wdf.iwdfdevice2_getdevicestackiotypepreference, wudfddi/IWDFDevice2::GetDeviceStackIoTypePreference
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.9
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
-	IWDFDevice2.GetDeviceStackIoTypePreference
product: Windows
targetos: Windows
req.typenames: POWER_ACTION, *PPOWER_ACTION
req.product: Windows 10 or later.
---

# IWDFDevice2::GetDeviceStackIoTypePreference method


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>GetDeviceStackIoTypePreference</b> method retrieves the buffer access methods that the framework is using for a device.


## -syntax


````
void GetDeviceStackIoTypePreference(
  [out] WDF_DEVICE_IO_TYPE *ReadWritePreference,
  [out] WDF_DEVICE_IO_TYPE *IoControlPreference
);
````


## -parameters




### -param ReadWritePreference [out]

A pointer to a driver-allocated location that receives a <a href="..\wudfddi_types\ne-wudfddi_types-_wdf_device_io_type.md">WDF_DEVICE_IO_TYPE</a>-typed value. This value identifies the buffer access method that the framework is using for a device's read and write requests.


### -param IoControlPreference [out]

A pointer to a driver-allocated location that receives a <a href="..\wudfddi_types\ne-wudfddi_types-_wdf_device_io_type.md">WDF_DEVICE_IO_TYPE</a>-typed value. This value that identifies the buffer access method that the framework is using for a device's I/O control requests.


## -returns



None.




## -remarks



If your driver calls <b>GetDeviceStackIoTypePreference</b> before the PnP manager has loaded all of the device's drivers, the values that <b>GetDeviceStackIoTypePreference</b> retrieves might not be the values that it actually uses.

For more information about how the framework chooses a buffer access method, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/accessing-data-buffers-in-wdf-drivers">How UMDF Chooses a Buffer Access Method for an I/O Request</a>.


#### Examples

The following code example retrieves the buffer access methods that the framework is using for a device.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>WDF_DEVICE_IO_TYPE ReadWriteAccessMethod;
WDF_DEVICE_IO_TYPE IoControlAccessMethod;

Device2-&gt;GetDeviceStackIoTypePreference(&amp;ReadWriteAccessMethod,
                                        &amp;IoControlAccessMethod); </pre>
</td>
</tr>
</table></span></div>



## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff556969">IWDFDeviceInitialize2::SetIoTypePreference</a>



<a href="..\wudfddi\nn-wudfddi-iwdfdevice2.md">IWDFDevice2</a>



 

 


