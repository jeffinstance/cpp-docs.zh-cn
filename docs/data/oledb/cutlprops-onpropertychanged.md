---
title: "Cutlprops:: Onpropertychanged |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- OnPropertyChanged
- CUtlProps.OnPropertyChanged
- CUtlProps::OnPropertyChanged
dev_langs:
- C++
helpviewer_keywords:
- OnPropertyChanged method
ms.assetid: c5924210-b685-46c4-87f8-1b81e5bd3378
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: f87f6842f33bd58be9cde515396f495402235a77
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="cutlpropsonpropertychanged"></a>CUtlProps::OnPropertyChanged
设置要处理所链接的属性的属性后调用。  
  
## <a name="syntax"></a>语法  
  
```cpp
      virtual HRESULT OnPropertyChanged(ULONG /* iCurSet */,  
   DBPROP* pDBProp);  
```  
  
#### <a name="parameters"></a>参数  
 `iCurSet`  
 属性集数组中; 中的索引如果只有一个属性集，则为零。  
  
 `pDBProp`  
 属性 ID 和中的新值[需要的 DBPROP](https://msdn.microsoft.com/en-us/library/ms717970.aspx)结构。  
  
## <a name="return-value"></a>返回值  
 一个标准 `HRESULT`。 默认返回值为`S_OK`。  
  
## <a name="remarks"></a>备注  
 如果你想要处理所链接的属性，例如书签或更新其值是依赖于另一个属性的值，应重写此函数。  
  
## <a name="example"></a>示例  
 在此函数中，用户会收到来自的属性 ID`DBPROP*`参数。 现在，它是可以比较针对链接到的属性的 ID。 当找到属性时，`SetProperties`调用来将设置与另一个属性结合使用的属性。 在此情况下，如果一个获取`DBPROP_IRowsetLocate`， `DBPROP_LITERALBOOKMARKS`，或`DBPROP_ORDEREDBOOKMARKS`属性，其中一个可以设置`DBPROP_BOOKMARKS`属性。  
  
 [!code-cpp[NVC_OLEDB_Provider#2](../../data/oledb/codesnippet/cpp/cutlprops-onpropertychanged_1.h)]  
  
## <a name="requirements"></a>惠?  
 **标头：** atldb.h  
  
## <a name="see-also"></a>请参阅  
 [CUtlProps 类](../../data/oledb/cutlprops-class.md)