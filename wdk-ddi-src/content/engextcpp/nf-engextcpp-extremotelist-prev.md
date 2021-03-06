---
UID: NF:engextcpp.ExtRemoteList.Prev
title: ExtRemoteList::Prev method
author: windows-driver-content
description: The Prev method changes the current item to the previous item in the list.
old-location: debugger\extremotelist_prev.htm
old-project: debugger
ms.assetid: 0dc65a1a-2188-417b-9f5c-4a3d2dc0bbb0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: EngExtCpp_Ref_46ab35be-6259-4fe5-95fe-06c99244f6bb.xml, ExtRemoteList, ExtRemoteList class [Windows Debugging], Prev method, ExtRemoteList::Prev, Prev method [Windows Debugging], Prev method [Windows Debugging], ExtRemoteList class, Prev,ExtRemoteList.Prev, debugger.extremotelist_prev
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: engextcpp.hpp
req.include-header: Engextcpp.hpp
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	engextcpp.hpp
api_name:
-	ExtRemoteList.Prev
product: Windows
targetos: Windows
req.typenames: SILO_DRIVER_CAPABILITIES, *PSILO_DRIVER_CAPABILITIES
---

# ExtRemoteList::Prev method


## -description


The <b>Prev</b> method changes the current item to the previous item in the list.


## -syntax


````
void Prev();
````


## -parameters






## -returns



This method does not return a value.




## -remarks



This method can only be used when iterating over doubly-linked lists.

If <b>Prev</b> reaches the end of the list, subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff544136">ExtRemoteList::HasNode</a> will return <code>false</code>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff544136">ExtRemoteList::HasNode</a>



<a href="..\engextcpp\nl-engextcpp-extremotelist.md">ExtRemoteList</a>



 

 


