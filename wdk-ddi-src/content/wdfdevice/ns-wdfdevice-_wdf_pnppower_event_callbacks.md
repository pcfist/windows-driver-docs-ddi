---
UID: NS:wdfdevice._WDF_PNPPOWER_EVENT_CALLBACKS
title: "_WDF_PNPPOWER_EVENT_CALLBACKS"
author: windows-driver-content
description: The WDF_PNPPOWER_EVENT_CALLBACKS structure contains pointers to a driver's Plug and Play and power event callback functions.
old-location: wdf\wdf_pnppower_event_callbacks.htm
old-project: wdf
ms.assetid: 2bfd677f-f2bd-49d7-b572-d7df4de0425c
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PWDF_PNPPOWER_EVENT_CALLBACKS, DFDeviceObjectGeneralRef_a4b53707-d968-45a7-a5e8-284e9f34f866.xml, PWDF_PNPPOWER_EVENT_CALLBACKS, PWDF_PNPPOWER_EVENT_CALLBACKS structure pointer, WDF_PNPPOWER_EVENT_CALLBACKS, WDF_PNPPOWER_EVENT_CALLBACKS structure, _WDF_PNPPOWER_EVENT_CALLBACKS, kmdf.wdf_pnppower_event_callbacks, wdf.wdf_pnppower_event_callbacks, wdfdevice/PWDF_PNPPOWER_EVENT_CALLBACKS, wdfdevice/WDF_PNPPOWER_EVENT_CALLBACKS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdfdevice.h
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
-	wdfdevice.h
api_name:
-	WDF_PNPPOWER_EVENT_CALLBACKS
product: Windows
targetos: Windows
req.typenames: WDF_PNPPOWER_EVENT_CALLBACKS, *PWDF_PNPPOWER_EVENT_CALLBACKS
req.product: Windows 10 or later.
---

# _WDF_PNPPOWER_EVENT_CALLBACKS structure


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_PNPPOWER_EVENT_CALLBACKS</b> structure contains pointers to a driver's Plug and Play and power event callback functions. 


## -syntax


````
typedef struct _WDF_PNPPOWER_EVENT_CALLBACKS {
  ULONG                                           Size;
  PFN_WDF_DEVICE_D0_ENTRY                         EvtDeviceD0Entry;
  PFN_WDF_DEVICE_D0_ENTRY_POST_INTERRUPTS_ENABLED EvtDeviceD0EntryPostInterruptsEnabled;
  PFN_WDF_DEVICE_D0_EXIT                          EvtDeviceD0Exit;
  PFN_WDF_DEVICE_D0_EXIT_PRE_INTERRUPTS_DISABLED  EvtDeviceD0ExitPreInterruptsDisabled;
  PFN_WDF_DEVICE_PREPARE_HARDWARE                 EvtDevicePrepareHardware;
  PFN_WDF_DEVICE_RELEASE_HARDWARE                 EvtDeviceReleaseHardware;
  PFN_WDF_DEVICE_SELF_MANAGED_IO_CLEANUP          EvtDeviceSelfManagedIoCleanup;
  PFN_WDF_DEVICE_SELF_MANAGED_IO_FLUSH            EvtDeviceSelfManagedIoFlush;
  PFN_WDF_DEVICE_SELF_MANAGED_IO_INIT             EvtDeviceSelfManagedIoInit;
  PFN_WDF_DEVICE_SELF_MANAGED_IO_SUSPEND          EvtDeviceSelfManagedIoSuspend;
  PFN_WDF_DEVICE_SELF_MANAGED_IO_RESTART          EvtDeviceSelfManagedIoRestart;
  PFN_WDF_DEVICE_SURPRISE_REMOVAL                 EvtDeviceSurpriseRemoval;
  PFN_WDF_DEVICE_QUERY_REMOVE                     EvtDeviceQueryRemove;
  PFN_WDF_DEVICE_QUERY_STOP                       EvtDeviceQueryStop;
  PFN_WDF_DEVICE_USAGE_NOTIFICATION               EvtDeviceUsageNotification;
  PFN_WDF_DEVICE_RELATIONS_QUERY                  EvtDeviceRelationsQuery;
  PFN_WDF_DEVICE_USAGE_NOTIFICATION_EX            EvtDeviceUsageNotificationEx;
} WDF_PNPPOWER_EVENT_CALLBACKS, *PWDF_PNPPOWER_EVENT_CALLBACKS;
````


## -struct-fields




### -field Size

The size, in bytes, of this structure.


### -field EvtDeviceD0Entry

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_d0_entry.md">EvtDeviceD0Entry</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceD0EntryPostInterruptsEnabled

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_d0_entry_post_interrupts_enabled.md">EvtDeviceD0EntryPostInterruptsEnabled</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceD0Exit

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_d0_exit.md">EvtDeviceD0Exit</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceD0ExitPreInterruptsDisabled

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_d0_exit_pre_interrupts_disabled.md">EvtDeviceD0ExitPreInterruptsDisabled</a> event callback function, or <b>NULL</b>.


### -field EvtDevicePrepareHardware

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_prepare_hardware.md">EvtDevicePrepareHardware</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceReleaseHardware

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_release_hardware.md">EvtDeviceReleaseHardware</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceSelfManagedIoCleanup

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_self_managed_io_cleanup.md">EvtDeviceSelfManagedIoCleanup</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceSelfManagedIoFlush

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_self_managed_io_flush.md">EvtDeviceSelfManagedIoFlush</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceSelfManagedIoInit

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_self_managed_io_init.md">EvtDeviceSelfManagedIoInit</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceSelfManagedIoSuspend

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_self_managed_io_suspend.md">EvtDeviceSelfManagedIoSuspend</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceSelfManagedIoRestart

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_self_managed_io_restart.md">EvtDeviceSelfManagedIoRestart</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceSurpriseRemoval

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_surprise_removal.md">EvtDeviceSurpriseRemoval</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceQueryRemove

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_query_remove.md">EvtDeviceQueryRemove</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceQueryStop

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_query_stop.md">EvtDeviceQueryStop</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceUsageNotification

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_usage_notification.md">EvtDeviceUsageNotification</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceRelationsQuery

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_relations_query.md">EvtDeviceRelationsQuery</a> event callback function, or <b>NULL</b>.


### -field EvtDeviceUsageNotificationEx

A pointer to the driver's <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_usage_notification_ex.md">EvtDeviceUsageNotificationEx</a> event callback function, or <b>NULL</b>. The <b>EvtDeviceUsageNotificationEx</b> member is available in version 1.11 and later versions of KMDF.
A driver can register either <b>EvtDeviceRelationsQuery</b> or <b>EvtDeviceUsageNotificationEx</b>, but not both.


## -remarks



The <b>WDF_PNPPOWER_EVENT_CALLBACKS</b> structure is used as input to the <a href="..\wdfdevice\nf-wdfdevice-wdfdeviceinitsetpnppowereventcallbacks.md">WdfDeviceInitSetPnpPowerEventCallbacks</a> method.

Your driver should initialize its WDF_PNPPOWER_EVENT_CALLBACKS structure by calling <a href="..\wdfdevice\nf-wdfdevice-wdf_pnppower_event_callbacks_init.md">WDF_PNPPOWER_EVENT_CALLBACKS_INIT</a>.




## -see-also

<a href="..\wdfdevice\ns-wdfdevice-_wdf_power_policy_event_callbacks.md">WDF_POWER_POLICY_EVENT_CALLBACKS</a>



 

 


