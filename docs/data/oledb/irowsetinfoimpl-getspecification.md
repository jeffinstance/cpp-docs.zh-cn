---
title: "Irowsetinfoimpl:: Getspecification |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- IRowsetInfoImpl::GetSpecification
- ATL.IRowsetInfoImpl.GetSpecification
- IRowsetInfoImpl.GetSpecification
- GetSpecification
- ATL::IRowsetInfoImpl::GetSpecification
dev_langs:
- C++
helpviewer_keywords:
- GetSpecification method
ms.assetid: 8e14289d-9cca-4df7-a9e0-f4ef03c61e30
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 0d740431452dd37de9cd361e524b45d99a6325f3
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="irowsetinfoimplgetspecification"></a>IRowsetInfoImpl::GetSpecification
返回创建下一个行集合的对象 （命令或会话） 上的接口指针。  
  
## <a name="syntax"></a>语法  
  
```cpp
      STDMETHOD (GetSpecification )(REFIID riid,  
   IUnknown** ppSpecification);  
```  
  
#### <a name="parameters"></a>参数  
 请参阅[IRowsetInfo::GetSpecification](https://msdn.microsoft.com/en-us/library/ms716746.aspx)中*OLE DB 程序员参考*。  
  
## <a name="remarks"></a>备注  
 使用此方法与[IGetDataSourceImpl](../../data/oledb/igetdatasourceimpl-class.md)从数据源对象中检索属性。  
  
## <a name="requirements"></a>惠?  
 **标头：** atldb.h  
  
## <a name="see-also"></a>请参阅  
 [IRowsetInfoImpl 类](../../data/oledb/irowsetinfoimpl-class.md)   
 [IRowsetInfoImpl::GetReferencedRowset](../../data/oledb/irowsetinfoimpl-getreferencedrowset.md)   
 [IRowsetInfoImpl::GetProperties](../../data/oledb/irowsetinfoimpl-getproperties.md)