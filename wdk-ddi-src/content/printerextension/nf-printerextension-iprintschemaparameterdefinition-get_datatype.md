---
UID: NF:printerextension.IPrintSchemaParameterDefinition.get_DataType
title: IPrintSchemaParameterDefinition::get_DataType method
author: windows-driver-content
description: The DataType property gets the PrintSchemaParameterDataType enumerated value that indicates the expected data type for the Print Schema parameter.
old-location: print\_iprintschemaparameterdefinition_datatype.htm
old-project: print
ms.assetid: 82CC79A8-0281-4100-B3FB-1FFFB2454B8D
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DataType property [Print Devices], DataType property [Print Devices], IPrintSchemaParameterDefinition interface, IPrintSchemaParameterDefinition, IPrintSchemaParameterDefinition interface [Print Devices], DataType property, IPrintSchemaParameterDefinition.DataType, IPrintSchemaParameterDefinition::get_DataType, get_DataType, get_DataType,IPrintSchemaParameterDefinition.get_DataType, print._iprintschemaparameterdefinition_datatype, printerextension/IPrintSchemaParameterDefinition::DataType, printerextension/IPrintSchemaParameterDefinition::get_DataType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
-	COM
api_location:
-	Printerextension.h
api_name:
-	IPrintSchemaParameterDefinition.DataType
-	IPrintSchemaParameterDefinition.get_DataType
product: Windows
targetos: Windows
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrintSchemaParameterDefinition::get_DataType method


## -description


The <b>DataType</b> property gets the <a href="..\printerextension\ne-printerextension-tagprintschemaparameterdatatype.md">PrintSchemaParameterDataType</a> enumerated value that indicates the expected data type for the Print Schema parameter.

This property is read-only.


## -syntax


````
HRESULT get_DataType(
  [out, retval] PrintSchemaParameterDataType *pDataType
);
````


## -parameters


## -see-also

<a href="..\printerextension\nn-printerextension-iprintschemaparameterdefinition.md">IPrintSchemaParameterDefinition</a>



<a href="..\printerextension\ne-printerextension-tagprintschemaparameterdatatype.md">PrintSchemaParameterDataType</a>



 

 


