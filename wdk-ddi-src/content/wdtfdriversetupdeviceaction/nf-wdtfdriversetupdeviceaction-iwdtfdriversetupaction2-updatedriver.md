---
UID: NF:wdtfdriversetupdeviceaction.IWDTFDriverSetupAction2.UpdateDriver
title: IWDTFDriverSetupAction2::UpdateDriver method
author: windows-driver-content
description: Updates the target device with a driver from the driver package.
old-location: dtf\iwdtfdriversetupaction2_updatedriver.htm
old-project: dtf
ms.assetid: 4eb49aae-a7de-4038-9d57-003bb30d7ea8
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: IWDTFDriverSetupAction2, IWDTFDriverSetupAction2 interface [Windows Device Testing Framework], UpdateDriver method, IWDTFDriverSetupAction2::UpdateDriver, Microsoft.WDTF.IWDTFDriverSetupAction2.UpdateDriver, Microsoft::WDTF::IWDTFDriverSetupAction2::UpdateDriver, UpdateDriver method [Windows Device Testing Framework], UpdateDriver method [Windows Device Testing Framework], IWDTFDriverSetupAction2 interface, UpdateDriver,IWDTFDriverSetupAction2.UpdateDriver, dtf.iwdtfdriversetupaction2_updatedriver, wdtfdriversetupdeviceaction/IWDTFDriverSetupAction2::UpdateDriver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfdriversetupdeviceaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFDriverSetupDeviceAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverSetupDeviceAction.Interop.dll
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
-	WDTFDriverSetupDeviceAction.Interop.dll
api_name:
-	IWDTFDriverSetupAction2.UpdateDriver
product: Windows
targetos: Windows
req.typenames: TTraceLevel
req.product: Windows 10 or later.
---

# IWDTFDriverSetupAction2::UpdateDriver method


## -description


Updates the target device with a driver from the driver package.


## -syntax


````
HRESULT UpdateDriver(
  [in]          IWDTFDriverPackageAction2 *pDp,
  [out, retval] VARIANT_BOOL              *pbRebootRequired
);
````


## -parameters




### -param pDp [in]

The driver package.


### -param pbReboot






#### - pbRebootRequired [out, retval]

True if the device must reboot after the update; otherwise, false.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\wdtfdriversetupdeviceaction\nn-wdtfdriversetupdeviceaction-iwdtfdriversetupaction2.md">IWDTFDriverSetupAction2</a>



 

 


