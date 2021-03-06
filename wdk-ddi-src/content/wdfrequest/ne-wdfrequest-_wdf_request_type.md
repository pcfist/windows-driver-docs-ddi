---
UID: NE:wdfrequest._WDF_REQUEST_TYPE
title: "_WDF_REQUEST_TYPE"
author: windows-driver-content
description: The WDF_REQUEST_TYPE enumeration type identifies types of requests that a framework request object might contain.
old-location: wdf\wdf_request_type.htm
old-project: wdf
ms.assetid: 91c036a0-7fce-4c7d-a217-eb1c487a15d0
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DFRequestObjectRef_43f31fe0-45c1-45d2-adcc-d0d931327eeb.xml, WDF_REQUEST_TYPE, WDF_REQUEST_TYPE enumeration, WdfRequestTypeCleanup, WdfRequestTypeClose, WdfRequestTypeCreate, WdfRequestTypeCreateMailSlot, WdfRequestTypeCreateNamedPipe, WdfRequestTypeDeviceChange, WdfRequestTypeDeviceControl, WdfRequestTypeDeviceControlInternal, WdfRequestTypeDirectoryControl, WdfRequestTypeFileSystemControl, WdfRequestTypeFlushBuffers, WdfRequestTypeLockControl, WdfRequestTypeMax, WdfRequestTypeNoFormat, WdfRequestTypeOther, WdfRequestTypePnp, WdfRequestTypePower, WdfRequestTypeQueryEA, WdfRequestTypeQueryInformation, WdfRequestTypeQueryQuota, WdfRequestTypeQuerySecurity, WdfRequestTypeQueryVolumeInformation, WdfRequestTypeRead, WdfRequestTypeSetEA, WdfRequestTypeSetInformation, WdfRequestTypeSetQuota, WdfRequestTypeSetSecurity, WdfRequestTypeSetVolumeInformation, WdfRequestTypeShutdown, WdfRequestTypeSystemControl, WdfRequestTypeUsb, WdfRequestTypeWrite, _WDF_REQUEST_TYPE, kmdf.wdf_request_type, wdf.wdf_request_type, wdfrequest/WDF_REQUEST_TYPE, wdfrequest/WdfRequestTypeCleanup, wdfrequest/WdfRequestTypeClose, wdfrequest/WdfRequestTypeCreate, wdfrequest/WdfRequestTypeCreateMailSlot, wdfrequest/WdfRequestTypeCreateNamedPipe, wdfrequest/WdfRequestTypeDeviceChange, wdfrequest/WdfRequestTypeDeviceControl, wdfrequest/WdfRequestTypeDeviceControlInternal, wdfrequest/WdfRequestTypeDirectoryControl, wdfrequest/WdfRequestTypeFileSystemControl, wdfrequest/WdfRequestTypeFlushBuffers, wdfrequest/WdfRequestTypeLockControl, wdfrequest/WdfRequestTypeMax, wdfrequest/WdfRequestTypeNoFormat, wdfrequest/WdfRequestTypeOther, wdfrequest/WdfRequestTypePnp, wdfrequest/WdfRequestTypePower, wdfrequest/WdfRequestTypeQueryEA, wdfrequest/WdfRequestTypeQueryInformation, wdfrequest/WdfRequestTypeQueryQuota, wdfrequest/WdfRequestTypeQuerySecurity, wdfrequest/WdfRequestTypeQueryVolumeInformation, wdfrequest/WdfRequestTypeRead, wdfrequest/WdfRequestTypeSetEA, wdfrequest/WdfRequestTypeSetInformation, wdfrequest/WdfRequestTypeSetQuota, wdfrequest/WdfRequestTypeSetSecurity, wdfrequest/WdfRequestTypeSetVolumeInformation, wdfrequest/WdfRequestTypeShutdown, wdfrequest/WdfRequestTypeSystemControl, wdfrequest/WdfRequestTypeUsb, wdfrequest/WdfRequestTypeWrite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdfrequest.h
req.include-header: Wdf.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
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
-	wdfrequest.h
api_name:
-	WDF_REQUEST_TYPE
product: Windows
targetos: Windows
req.typenames: WDF_REQUEST_TYPE
req.product: Windows 10 or later.
---

# _WDF_REQUEST_TYPE enumeration


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_REQUEST_TYPE</b> enumeration type identifies types of requests that a framework request object might contain.


## -syntax


````
typedef enum _WDF_REQUEST_TYPE { 
  WdfRequestTypeCreate                  = 0x0,
  WdfRequestTypeCreateNamedPipe         = 0x1,
  WdfRequestTypeClose                   = 0x2,
  WdfRequestTypeRead                    = 0x3,
  WdfRequestTypeWrite                   = 0x4,
  WdfRequestTypeQueryInformation        = 0x5,
  WdfRequestTypeSetInformation          = 0x6,
  WdfRequestTypeQueryEA                 = 0x7,
  WdfRequestTypeSetEA                   = 0x8,
  WdfRequestTypeFlushBuffers            = 0x9,
  WdfRequestTypeQueryVolumeInformation  = 0xa,
  WdfRequestTypeSetVolumeInformation    = 0xb,
  WdfRequestTypeDirectoryControl        = 0xc,
  WdfRequestTypeFileSystemControl       = 0xd,
  WdfRequestTypeDeviceControl           = 0xe,
  WdfRequestTypeDeviceControlInternal   = 0xf,
  WdfRequestTypeShutdown                = 0x10,
  WdfRequestTypeLockControl             = 0x11,
  WdfRequestTypeCleanup                 = 0x12,
  WdfRequestTypeCreateMailSlot          = 0x13,
  WdfRequestTypeQuerySecurity           = 0x14,
  WdfRequestTypeSetSecurity             = 0x15,
  WdfRequestTypePower                   = 0x16,
  WdfRequestTypeSystemControl           = 0x17,
  WdfRequestTypeDeviceChange            = 0x18,
  WdfRequestTypeQueryQuota              = 0x19,
  WdfRequestTypeSetQuota                = 0x1A,
  WdfRequestTypePnp                     = 0x1B,
  WdfRequestTypeOther                   = 0x1C,
  WdfRequestTypeUsb                     = 0x40,
  WdfRequestTypeNoFormat                = 0xFF,
  WdfRequestTypeMax                     = 0x100
} WDF_REQUEST_TYPE;
````


## -enum-fields




### -field WdfRequestTypeCreate

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548630">IRP_MJ_CREATE</a> request. The framework delivers this type of request to a driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_file_create.md">EvtDeviceFileCreate</a> callback function.


### -field WdfRequestTypeCreateNamedPipe

The request object represents an <b>IRP_MJ_CREATE_NAMED_PIPE</b> request. The framework does not handle this type of request.


### -field WdfRequestTypeClose

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff550720">IRP_MJ_CLOSE</a> request. The framework delivers this type of request to a driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_file_close.md">EvtFileClose</a> callback function.


### -field WdfRequestTypeRead

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549327">IRP_MJ_READ</a> request. The framework delivers this type of request to a driver's <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/request-handlers">request handler</a>.


### -field WdfRequestTypeWrite

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff550819">IRP_MJ_WRITE</a> request. The framework delivers this type of request to a driver's <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/request-handlers">request handler</a>.


### -field WdfRequestTypeQueryInformation

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549283">IRP_MJ_QUERY_INFORMATION</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeSetInformation

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549366">IRP_MJ_SET_INFORMATION</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeQueryEA

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549279">IRP_MJ_QUERY_EA</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeSetEA

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549346">IRP_MJ_SET_EA</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeFlushBuffers

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549235">IRP_MJ_FLUSH_BUFFERS</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeQueryVolumeInformation

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549318">IRP_MJ_QUERY_VOLUME_INFORMATION</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeSetVolumeInformation

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549415">IRP_MJ_SET_VOLUME_INFORMATION</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeDirectoryControl

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548658">IRP_MJ_DIRECTORY_CONTROL</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeFileSystemControl

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff550751">IRP_MJ_FILE_SYSTEM_CONTROL</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeDeviceControl

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548649">IRP_MJ_DEVICE_CONTROL</a> request. The framework delivers this type of request to a driver's <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/request-handlers">request handler</a>.


### -field WdfRequestTypeDeviceControlInternal

The request object represents an  <a href="https://msdn.microsoft.com/library/windows/hardware/ff550766">IRP_MJ_INTERNAL_DEVICE_CONTROL</a> request. The framework delivers this type of request to a driver's <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/request-handlers">request handler</a>.


### -field WdfRequestTypeShutdown

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549423">IRP_MJ_SHUTDOWN</a> request. The framework handles this type of request for the driver, but the framework also calls the driver's <a href="https://msdn.microsoft.com/365e669b-b4a1-432a-ab0c-9292a910256e">EvtDeviceShutdownNotification</a> callback function, if it exists.


### -field WdfRequestTypeLockControl

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549251">IRP_MJ_LOCK_CONTROL</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeCleanup

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548608">IRP_MJ_CLEANUP</a> request. The framework delivers this type of request to a driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_file_cleanup.md">EvtFileCleanup</a> callback function.


### -field WdfRequestTypeCreateMailSlot

The request object represents an <b>IRP_MJ_CREATE_MAILSLOT</b> request. The framework does not handle this type of request.


### -field WdfRequestTypeQuerySecurity

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549298">IRP_MJ_QUERY_SECURITY</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeSetSecurity

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549407">IRP_MJ_SET_SECURITY</a> request. The framework does not handle this type of request.


### -field WdfRequestTypePower

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff550784">IRP_MJ_POWER</a> request. The framework handles this type of request for the driver, but the framework also calls the driver's <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/dn265631">general</a>, <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/dn265631">FDO</a>, and <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/dn265631">PDO</a> callback functions for Plug and Play (PnP) and power management, if the callback functions exist.


### -field WdfRequestTypeSystemControl

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff550813">IRP_MJ_SYSTEM_CONTROL</a> request. The framework handles this type of request for the driver, if the driver supports <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/supporting-wmi-in-kmdf-drivers">Windows Management Instrumentation (WMI)</a>.


### -field WdfRequestTypeDeviceChange

The request object represents an <b>IRP_MJ_DEVICE_CHANGE</b> request. The framework does not handle this type of request.


### -field WdfRequestTypeQueryQuota

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549293">IRP_MJ_QUERY_QUOTA</a> request. The framework does not handle this type of request.


### -field WdfRequestTypeSetQuota

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549401">IRP_MJ_SET_QUOTA</a> request. The framework does not handle this type of request.


### -field WdfRequestTypePnp

The request object represents an <a href="https://msdn.microsoft.com/library/windows/hardware/ff549268">IRP_MJ_PNP</a> request. The framework handles this type of request for the driver, but the framework also calls the driver's <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/dn265631">general</a>, <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/dn265631">FDO</a>, and <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/dn265631">PDO</a> callback functions for PnP and power management, if the callback functions exist.


### -field WdfRequestTypeOther

A driver receives this request type in its <a href="..\wdfrequest\nc-wdfrequest-evt_wdf_request_completion_routine.md">CompletionRoutine</a> event callback function when requests formatted with <a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetformatrequestforinternalioctlothers.md">WdfIoTargetFormatRequestForInternalIoctlOthers</a> are completed.


### -field WdfRequestTypeUsb

The target device is a USB device. (This value is used only in <a href="..\wdfrequest\ns-wdfrequest-_wdf_request_completion_params.md">WDF_REQUEST_COMPLETION_PARAMS</a> structures.)


### -field WdfRequestTypeNoFormat

The request object's type has not been specified.


### -field WdfRequestTypeMax

The maximum value that has been assigned to a valid IRP major function code.


## -remarks



The <b>WDF_REQUEST_TYPE</b> enumeration type is used in the <a href="..\wdfrequest\ns-wdfrequest-_wdf_request_parameters.md">WDF_REQUEST_PARAMETERS</a> and <a href="..\wdfrequest\ns-wdfrequest-_wdf_request_completion_params.md">WDF_REQUEST_COMPLETION_PARAMS</a> structures.

For information about how a framework-based driver can handle request types that the framework does not support, see <a href="https://msdn.microsoft.com/0481f335-f63b-4f93-8eb4-523a70082302">Handling an IRP that the Framework Does Not Support</a>.

For the UMDF version of this enumeration, see <a href="..\wdfrequest\ne-wdfrequest-_wdf_request_type.md">WDF_REQUEST_TYPE (UMDF)</a>.




## -see-also

<a href="..\wdfdevice\nc-wdfdevice-evt_wdf_file_cleanup.md">EvtFileCleanup</a>



<a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_file_create.md">EvtDeviceFileCreate</a>



<a href="..\wdfdevice\nc-wdfdevice-evt_wdf_file_close.md">EvtFileClose</a>



<a href="https://msdn.microsoft.com/365e669b-b4a1-432a-ab0c-9292a910256e">EvtDeviceShutdownNotification</a>



 

 


