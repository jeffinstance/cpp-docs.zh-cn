---
title: "Irowsetimpl:: M_bcanscrollback |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- IRowsetImpl::m_bCanScrollBack
- ATL::IRowsetImpl::m_bCanScrollBack
- IRowsetImpl.m_bCanScrollBack
- ATL.IRowsetImpl.m_bCanScrollBack
- m_bCanScrollBack
dev_langs:
- C++
helpviewer_keywords:
- m_bCanScrollBack
ms.assetid: 69de3179-bf56-415e-935f-e98bcb34debe
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: c388092aaeb935dc8eaf9f76d7d64adb974310b3
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="irowsetimplmbcanscrollback"></a>IRowsetImpl::m_bCanScrollBack
指示提供程序是否可以向后具有其游标滚动。  
  
## <a name="syntax"></a>语法  
  
```cpp
unsigned  m_bCanScrollBack:1;  
  
```  
  
## <a name="remarks"></a>备注  
 链接至**DBPROP_CANSCROLLBACKWARDS**中的属性**DBPROPSET_ROWSET**组。 提供程序必须支持**DBPROP_CANSCROLLBACKWARDS**为**m_bCanFetchBackwards**为 true。  
  
## <a name="requirements"></a>惠?  
 **标头：** atldb.h  
  
## <a name="see-also"></a>请参阅  
 [IRowsetImpl 类](../../data/oledb/irowsetimpl-class.md)   
 [IRowsetImpl::m_bCanFetchBack](../../data/oledb/irowsetimpl-m-bcanfetchback.md)