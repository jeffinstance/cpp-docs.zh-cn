---
title: "CBookmark 类 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- ATL.CBookmark
- ATL::CBookmark<nSize>
- CBookmark
- ATL.CBookmark<nSize>
- ATL::CBookmark
dev_langs:
- C++
helpviewer_keywords:
- CBookmark class
ms.assetid: bc942f95-6f93-41d9-bb6e-bcdae4ae0b7a
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: b5c0f5f7a2af7c5b744fcad31ae6901988e92b9e
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="cbookmark-class"></a>CBookmark 类
在其缓冲区中包含一个书签值。  
  
## <a name="syntax"></a>语法

```cpp
template < DBLENGTH nSize = 0 >  
class CBookmark : public CBookmarkBase
  
template <>  
class CBookmark< 0 > : public CBookmarkBase  
```  
  
#### <a name="parameters"></a>参数  
 `nSize`  
 以字节为单位的书签缓冲区的大小。 当`nSize`为零，将在运行时动态创建书签缓冲区。  
  
## <a name="members"></a>成员  
  
### <a name="methods"></a>方法  
  
|||  
|-|-|  
|[CBookmark](../../data/oledb/cbookmark-class.md)|构造函数|  
|[GetBuffer](../../data/oledb/cbookmark-getbuffer.md)|检索指向缓冲区的指针。|  
|[GetSize](../../data/oledb/cbookmark-getsize.md)|检索以字节为单位的缓冲区的大小。|  
|[SetBookmark](../../data/oledb/cbookmark-setbookmark.md)|设置书签值。|  
  
### <a name="operators"></a>运算符  
  
|||  
|-|-|  
|[operator =](../../data/oledb/cbookmark-operator-equal.md)|将分配一个`CBookmark`到另一个类。|  
  
## <a name="remarks"></a>备注  
 **CBookmark\<0 >**模板专用化`CBookmark`; 在运行时动态创建其缓冲区。  
  
## <a name="requirements"></a>惠?  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [OLE DB 使用者模板](../../data/oledb/ole-db-consumer-templates-cpp.md)   
 [OLE DB 使用者模板参考](../../data/oledb/ole-db-consumer-templates-reference.md)