---
title: "编译器错误 C3004 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3004
dev_langs:
- C++
helpviewer_keywords:
- C3004
ms.assetid: 819c2b57-8366-4ca7-9135-1f0c5e5b6bb6
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 1e1e82f2128725b585e7ed266fd1e977e79196f8
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3004"></a>编译器错误 C3004
“clause”：OpenMP“directive”指令上的子句无效  
  
 在指令上使用了不支持的 OpenMP 子句。  
  
 下面的示例生成 C3004：  
  
```  
// C3004.c  
// compile with: /openmp  
int main()  
{  
   int x, y, z;  
  
   // Shared clause not allowed for 'single' directive.  
   #pragma omp single shared(x, y)   // C3004  
  
   x = y;  
}  
```