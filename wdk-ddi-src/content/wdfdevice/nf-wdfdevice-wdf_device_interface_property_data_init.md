---
UID: NF:wdfdevice.WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT
title: WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT function
author: windows-driver-content
description: The WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT function initializes a driver's WDF_DEVICE_INTERFACE_PROPERTY_DATA structure.
old-location: wdf\wdf_device_interface_property_data_init.htm
old-project: wdf
ms.assetid: 8B3D6F59-BA76-4B14-9570-57263D204BFE
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT, WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT function, wdf.wdf_device_interface_property_data_init, wdfdevice/WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfdevice.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 2.0
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
-	wdfdevice.h
api_name:
-	WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT
product: Windows
targetos: Windows
req.typenames: WDF_STATE_NOTIFICATION_TYPE
req.product: Windows 10 or later.
---

# WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT function


## -description


<p class="CCE_Message">[Applies to UMDF only]

The <b>WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT</b> function initializes a driver's <a href="..\wdfdevice\ns-wdfdevice-_wdf_device_interface_property_data.md">WDF_DEVICE_INTERFACE_PROPERTY_DATA</a> structure.


## -syntax


````
void WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT(
  _In_       PWDF_DEVICE_INTERFACE_PROPERTY_DATA PropertyData,
  _In_ const GUID                                *InterfaceClassGUID,
  _In_ const DEVPROPKEY                          *PropertyKey
);
````


## -parameters




### -param PropertyData [in]

A pointer to <a href="..\wdfdevice\ns-wdfdevice-_wdf_device_interface_property_data.md">WDF_DEVICE_INTERFACE_PROPERTY_DATA</a> structure.


### -param InterfaceClassGUID [in]

A pointer to a GUID that identifies the device interface class.


### -param PropertyKey [in]

A pointer to a <b>DEVPROPKEY</b> structure that specifies the device property key.


## -returns



This function does not return a value.




## -remarks



Before calling the following methods, a driver must call <b>WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT</b> to initialize a <a href="..\wdfdevice\ns-wdfdevice-_wdf_device_interface_property_data.md">WDF_DEVICE_INTERFACE_PROPERTY_DATA</a> structure.

<ul>
<li>
<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceallocandqueryinterfaceproperty.md">WdfDeviceAllocAndQueryInterfaceProperty</a>
</li>
<li>
<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceassigninterfaceproperty.md">WdfDeviceAssignInterfaceProperty</a>
</li>
<li>
<a href="..\wdfdevice\nf-wdfdevice-wdfdevicequeryinterfaceproperty.md">WdfDeviceQueryInterfaceProperty</a>
</li>
</ul>
The <b>WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT</b> function zeros the specified <a href="..\wdfdevice\ns-wdfdevice-_wdf_device_interface_property_data.md">WDF_DEVICE_INTERFACE_PROPERTY_DATA</a> structure and sets the structure's <b>Size</b> member. It also sets the structure's <b>InterfaceClassGUID</b> and <b>PropertyKey</b> members to the specified values.

For a code example that uses <b>WDF_DEVICE_INTERFACE_PROPERTY_DATA_INIT</b>, see <a href="..\wdfdevice\nf-wdfdevice-wdfdeviceassigninterfaceproperty.md">WdfDeviceAssignInterfaceProperty</a>.




## -see-also

<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceallocandqueryinterfaceproperty.md">WdfDeviceAllocAndQueryInterfaceProperty</a>



<a href="..\wdfdevice\nf-wdfdevice-wdfdevicequeryinterfaceproperty.md">WdfDeviceQueryInterfaceProperty</a>



<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceassigninterfaceproperty.md">WdfDeviceAssignInterfaceProperty</a>



<a href="..\wdfdevice\ns-wdfdevice-_wdf_device_interface_property_data.md">WDF_DEVICE_INTERFACE_PROPERTY_DATA</a>



 

 


