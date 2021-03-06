---
title: "Cenumerator:: Find |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CEnumerator::Find
- ATL::CEnumerator::Find
- ATL.CEnumerator.Find
- CEnumerator.Find
dev_langs:
- C++
helpviewer_keywords:
- Find method
ms.assetid: 69a153af-d6c3-40fd-9018-27c7d2f344c6
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 66298c4be2bb1e43aa37899fe652ccbf6694faae
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="cenumeratorfind"></a>CEnumerator::Find
在可用提供程序之间查找指定名称。  
  
## <a name="syntax"></a>语法  
  
```cpp
      bool Find(TCHAR* szSearchName) throw();  
```  
  
#### <a name="parameters"></a>参数  
 *szSearchName*  
 [in] 要搜索的名称。  
  
## <a name="return-value"></a>返回值  
 **true**如果找到名称。 否则为**false**。  
  
## <a name="remarks"></a>备注  
 此名称将映射到**SOURCES_NAME**的成员[ISourcesRowset](https://msdn.microsoft.com/en-us/library/ms715969.aspx)接口。  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [CEnumerator 类](../../data/oledb/cenumerator-class.md)