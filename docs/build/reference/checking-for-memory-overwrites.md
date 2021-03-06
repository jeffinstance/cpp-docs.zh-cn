---
title: "检查内存改写 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- memory, overwrites
ms.assetid: da7c5d77-a267-415f-a8ab-ee5ce5bfc286
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 573710ae62384c8674009770b3c4fb29100db446
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="checking-for-memory-overwrites"></a>检查内存改写
如果在堆操作函数调用中获取访问冲突，则可能你的程序损坏了堆。 将这种情况下的常见的症状：  
  
```  
Access Violation in _searchseg  
```  
  
 [_Heapchk](../../c-runtime-library/reference/heapchk.md)函数是适用于这两个调试和发布版本 (仅适用于 Windows NT) 验证运行的时库堆的完整性。 你可以使用`_heapchk`方式与得多相同`AfxCheckMemory`函数来隔离出堆覆盖，例如：  
  
```  
if(_heapchk()!=_HEAPOK)  
   DebugBreak();  
```  
  
 如果此函数失败，你需要找出堆已损坏的位置。  
  
## <a name="see-also"></a>请参阅  
 [修复发行版本问题](../../build/reference/fixing-release-build-problems.md)