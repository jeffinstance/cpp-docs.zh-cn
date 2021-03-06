---
title: CRowset::GetData | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CRowset<TAccessor>::GetData
- ATL::CRowset<TAccessor>::GetData
- ATL::CRowset::GetData
- ATL.CRowset<TAccessor>.GetData
- CRowset<TAccessor>.GetData
- CRowset::GetData
- CRowset.GetData
- ATL.CRowset.GetData
dev_langs:
- C++
helpviewer_keywords:
- GetData method [OLE DB]
ms.assetid: 1e0347b5-3e24-4ff8-a790-839616c1522f
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 91cd3322461be0cfaaefb793e63cb452253ba2aa
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="crowsetgetdata"></a>CRowset::GetData
从行的行集的副本检索数据。  
  
## <a name="syntax"></a>语法  
  
```cpp
HRESULT GetData() throw();   


HRESULT GetData(int nAccessor) throw();  
```  
  
#### <a name="parameters"></a>参数  
 `nAccessor`  
 [in]访问器可用于访问数据 （零偏移量） 索引号。  
  
## <a name="return-value"></a>返回值  
 一个标准 `HRESULT`。  
  
## <a name="remarks"></a>备注  
 如果指定不是在为自动访问器的访问器[BEGIN_ACCESSOR](../../data/oledb/begin-accessor.md)，使用此方法显式获取数据，通过传递访问器数量。  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [CRowset 类](../../data/oledb/crowset-class.md)