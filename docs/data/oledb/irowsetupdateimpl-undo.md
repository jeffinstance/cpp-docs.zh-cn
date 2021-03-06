---
title: "Irowsetupdateimpl:: Undo |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- ATL.IRowsetUpdateImpl.Undo
- ATL::IRowsetUpdateImpl::Undo
- IRowsetUpdateImpl::Undo
- IRowsetUpdateImpl.Undo
dev_langs:
- C++
helpviewer_keywords:
- Undo method
ms.assetid: f3dc7764-050c-4322-9b2f-9ca772a0fb88
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: da14d4451a209202f63d54d876bc48aba3e3e5ad
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="irowsetupdateimplundo"></a>IRowsetUpdateImpl::Undo
自上次提取或更新以来撤消对行的任何更改。  
  
## <a name="syntax"></a>语法  
  
```cpp
      STDMETHOD (Undo )(HCHAPTER /* hReserved */,  
   DBCOUNTITEM cRows,  
   const HROW rghRows[ ],  
   DBCOUNTITEM* pcRowsUndone,  
   HROW** prgRowsUndone,  
   DBROWSTATUS** prgRowStatus);  
```  
  
#### <a name="parameters"></a>参数  
 `hReserved`  
 [in]对应于`hChapter`中的参数[IRowsetUpdate::Undo](https://msdn.microsoft.com/en-us/library/ms719655.aspx)。  
  
 *pcRowsUndone*  
 [out]对应于`pcRows`中的参数[IRowsetUpdate::Undo](https://msdn.microsoft.com/en-us/library/ms719655.aspx)。  
  
 *prgRowsUndone*  
 [in]对应于*prgRows*中的参数[IRowsetUpdate::Undo](https://msdn.microsoft.com/en-us/library/ms719655.aspx)。  
  
 其他参数，请参阅[IRowsetUpdate::Undo](https://msdn.microsoft.com/en-us/library/ms719655.aspx)中*OLE DB 程序员参考*。  
  
## <a name="requirements"></a>惠?  
 **标头：** atldb.h  
  
## <a name="see-also"></a>请参阅  
 [IRowsetUpdateImpl 类](../../data/oledb/irowsetupdateimpl-class.md)