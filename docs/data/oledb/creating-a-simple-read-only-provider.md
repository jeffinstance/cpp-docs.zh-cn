---
title: "创建简单的只读提供程序 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- OLE DB providers, creating
- OLE DB provider templates, creating providers
ms.assetid: ade8ccdd-9ea4-4e46-a964-18460c2a2401
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 830ba99037607f4fc8ceac9bad451381c30c7786
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="creating-a-simple-read-only-provider"></a>创建简单的只读提供程序
如果你已创建使用 ATL 项目向导和 ATL OLE DB 提供程序向导的 OLE DB 提供程序，你可以添加你想要支持其他功能。 开始通过检查什么类型的数据，则将会发送给使用者和在什么条件下设计你的提供商。 尤其是，务必确定你是否需要支持命令、 事务和其他可选对象。 设计良好，预先将加快实现和测试。  
  
 该示例会显示在两个部分：  
  
-   第一个部分演示如何[创建简单的只读提供程序](../../data/oledb/implementing-the-simple-read-only-provider.md)读取一对字符串。  
  
-   第二个部分显示如何[增强简单的只读提供程序](../../data/oledb/enhancing-the-simple-read-only-provider.md)通过添加`IRowsetLocate`接口。  
  
## <a name="see-also"></a>请参阅  
 [创建 OLE DB 提供程序](../../data/oledb/creating-an-ole-db-provider.md)