---
UID: NF:wdfpdo.WdfPdoMarkMissing
title: WdfPdoMarkMissing function
author: windows-driver-content
description: The WdfPdoMarkMissing method informs the framework that a device is no longer accessible.
old-location: wdf\wdfpdomarkmissing.htm
old-project: wdf
ms.assetid: f35e1ed4-eaa9-423c-95cb-5eb96231d592
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DFDeviceObjectFdoPdoRef_a4198313-bd10-4b8a-a032-f253cdaccc7b.xml, WdfPdoMarkMissing, WdfPdoMarkMissing method, kmdf.wdfpdomarkmissing, wdf.wdfpdomarkmissing, wdfpdo/WdfPdoMarkMissing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfpdo.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 
req.ddi-compliance: DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (see Framework Library Versioning.)
req.dll: 
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Wdf01000.sys
-	Wdf01000.sys.dll
api_name:
-	WdfPdoMarkMissing
product: Windows
targetos: Windows
req.typenames: WDF_OBJECT_CONTEXT_TYPE_INFO, *PWDF_OBJECT_CONTEXT_TYPE_INFO
req.product: Windows 10 or later.
---

# WdfPdoMarkMissing function


## -description


<p class="CCE_Message">[Applies to KMDF only]

The <b>WdfPdoMarkMissing</b> method informs the framework that a device is no longer accessible.


## -syntax


````
NTSTATUS WdfPdoMarkMissing(
  _In_ WDFDEVICE Device
);
````


## -parameters




### -param Device [in]

A handle to a framework device object that represents the device's physical device object (PDO).


## -returns



If the operation succeeds, the function returns STATUS_SUCCESS. Additional return values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Device</i> handle does not represent a PDO.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The device object could not be found.

</td>
</tr>
</table>
 

The method might also return other<a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505"> NTSTATUS values</a>.

A system bug check occurs if the driver supplies an invalid object handle.




## -remarks



For more information about <b>WdfPdoMarkMissing</b>, see <a href="https://msdn.microsoft.com/58377f17-a9dc-4096-af23-36f8d8dbb87e">Static Enumeration</a>.


#### Examples

The following code example searches a list of child devices to find one that matches a specified serial number. When the example finds the correct child, it calls <b>WdfPdoMarkMissing</b> to indicate that the child is not accessible. This example was taken from the <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/sample-kmdf-drivers">Toaster</a> sample bus driver and simplified.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>WDFDEVICE  hChild = NULL;
NTSTATUS  status = STATUS_INVALID_PARAMETER;
BOOLEAN  found = FALSE;
PPDO_DEVICE_DATA  pdoData;

WdfFdoLockStaticChildListForIteration(Device);

while ((hChild = WdfFdoRetrieveNextStaticChild(
                                               Device, 
                                               hChild,
                                               WdfRetrieveAddedChildren
                                               )) != NULL) {
    pdoData = PdoGetData(hChild);  // Device object context space
    if (SerialNo == pdoData-&gt;SerialNo) {
        status = WdfPdoMarkMissing(hChild);
        if(!NT_SUCCESS(status)) {
            KdPrint(("WdfPdoMarkMissing failed 0x%x\n", status));
            break;
        }
        found = TRUE;
        break;
    }
}
WdfFdoUnlockStaticChildListFromIteration(Device);</pre>
</td>
</tr>
</table></span></div>



## -see-also

<a href="..\wdffdo\nf-wdffdo-wdffdolockstaticchildlistforiteration.md">WdfFdoLockStaticChildListForIteration</a>



<a href="..\wdffdo\nf-wdffdo-wdffdounlockstaticchildlistfromiteration.md">WdfFdoUnlockStaticChildListFromIteration</a>



<a href="..\wdffdo\nf-wdffdo-wdffdoretrievenextstaticchild.md">WdfFdoRetrieveNextStaticChild</a>



 

 


