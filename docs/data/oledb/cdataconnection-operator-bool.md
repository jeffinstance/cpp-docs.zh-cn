---
title: "Cdataconnection:: Operator BOOL |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CDataConnection::operatorBOOL
- ATL::CDataConnection::operatorBOOL
- CDataConnection.operatorBOOL
- ATL.CDataConnection.operatorBOOL
dev_langs:
- C++
helpviewer_keywords:
- BOOL operator
- operator bool
ms.assetid: ad0bea7f-61ff-47f7-8127-32a31e3e9b9d
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: a29d4a3878750f2ca7e70eff032ac9d2cb6b986c
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="cdataconnectionoperator-bool"></a>CDataConnection::operator BOOL
确定当前会话是否为打开。  
  
## <a name="syntax"></a>语法  
  
```cpp
operator BOOL() throw();  
  
```  
  
## <a name="remarks"></a>备注  
 返回**BOOL** (MFC typedef) 值。 **TRUE**意味着当前会话处于打开状态;**FALSE**意味着关闭当前会话。  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [CDataConnection 类](../../data/oledb/cdataconnection-class.md)   
 [Cdataconnection:: Operator bool](../../data/oledb/cdataconnection-operator-bool-ole-db.md)