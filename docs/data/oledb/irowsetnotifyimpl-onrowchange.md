---
title: "Irowsetnotifyimpl:: Onrowchange |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- IRowsetNotifyImpl::OnRowChange
- IRowsetNotifyImpl.OnRowChange
- OnRowChange
dev_langs:
- C++
helpviewer_keywords:
- OnRowChange method
ms.assetid: 148bee03-3707-4bbf-8c51-657efc63645f
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: ae629b0deec2f6b8cf533b41aec4ff3803117324
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="irowsetnotifyimplonrowchange"></a>IRowsetNotifyImpl::OnRowChange
通知使用者的第一个更改行或任何更改的影响到整行。  
  
## <a name="syntax"></a>语法  
  
```cpp
STDMETHOD(OnRowChange)(   
/* [in] */ IRowset* /* pRowset */,  
/* [in] */ DBCOUNTITEM /* cRows */,  
/* [size_is][in] */ const HROW /* rghRows*/ [] ,  
/* [in] */ DBREASON /* eReason */,  
/* [in] */ DBEVENTPHASE /* ePhase */,  
/* [in] */ BOOL /* fCantDeny */)  
```  
  
#### <a name="parameters"></a>参数  
 请参阅[irowsetnotify:: Onrowchange](https://msdn.microsoft.com/en-us/library/ms722694.aspx)有关参数说明。  
  
## <a name="return-value"></a>返回值  
 请参阅[irowsetnotify:: Onrowchange](https://msdn.microsoft.com/en-us/library/ms722694.aspx)有关返回值说明。  
  
## <a name="remarks"></a>备注  
 此方法会包装[irowsetnotify:: Onrowchange](https://msdn.microsoft.com/en-us/library/ms722694.aspx)方法。 有关详细信息，请参阅“OLE DB 程序员参考”中对该方法的描述。  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [IRowsetNotifyImpl 类](../../data/oledb/irowsetnotifyimpl-class.md)   
 [IRowsetNotify::OnRowChange](https://msdn.microsoft.com/en-us/library/ms722694.aspx)