---
UID: NS:wdm._OB_POST_OPERATION_PARAMETERS
title: "_OB_POST_OPERATION_PARAMETERS"
author: windows-driver-content
description: The OB_POST_OPERATION_PARAMETERS union describes the operation-specific parameters for an ObjectPostCallback routine.
old-location: kernel\ob_post_operation_parameters.htm
old-project: kernel
ms.assetid: cd0551fc-c276-45c3-a560-bded300a4535
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: "*POB_POST_OPERATION_PARAMETERS, OB_POST_OPERATION_PARAMETERS, OB_POST_OPERATION_PARAMETERS union [Kernel-Mode Driver Architecture], POB_POST_OPERATION_PARAMETERS, POB_POST_OPERATION_PARAMETERS union pointer [Kernel-Mode Driver Architecture], _OB_POST_OPERATION_PARAMETERS, kernel.ob_post_operation_parameters, kstruct_c_2395a938-5759-44aa-b854-0df3c04d97ec.xml, wdm/OB_POST_OPERATION_PARAMETERS, wdm/POB_POST_OPERATION_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Server 2008 and later versions of the Windows operating system.
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
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdm.h
api_name:
-	OB_POST_OPERATION_PARAMETERS
product: Windows
targetos: Windows
req.typenames: OB_POST_OPERATION_PARAMETERS, *POB_POST_OPERATION_PARAMETERS
req.product: Windows 10 or later.
---

# _OB_POST_OPERATION_PARAMETERS structure


## -description


The <b>OB_POST_OPERATION_PARAMETERS</b> union describes the operation-specific parameters for an <a href="..\wdm\nc-wdm-pob_post_operation_callback.md">ObjectPostCallback</a> routine.


## -syntax


````
typedef union _OB_POST_OPERATION_PARAMETERS {
  OB_POST_CREATE_HANDLE_INFORMATION    CreateHandleInformation;
  OB_POST_DUPLICATE_HANDLE_INFORMATION DuplicateHandleInformation;
} OB_POST_OPERATION_PARAMETERS, *POB_POST_OPERATION_PARAMETERS;
````


## -struct-fields




### -field CreateHandleInformation

An <a href="..\wdm\ns-wdm-_ob_post_create_handle_information.md">OB_POST_CREATE_HANDLE_INFORMATION</a> structure that contains information that is specific to a handle that is being opened.


### -field DuplicateHandleInformation

An <a href="..\wdm\ns-wdm-_ob_post_duplicate_handle_information.md">OB_POST_DUPLICATE_HANDLE_INFORMATION</a> structure that contains information that is specific to a handle that is being duplicated.


## -see-also

<a href="..\wdm\nc-wdm-pob_post_operation_callback.md">ObjectPostCallback</a>



<a href="..\wdm\ns-wdm-_ob_post_duplicate_handle_information.md">OB_POST_DUPLICATE_HANDLE_INFORMATION</a>



<a href="..\wdm\ns-wdm-_ob_post_create_handle_information.md">OB_POST_CREATE_HANDLE_INFORMATION</a>



 

 


