---
title: "编译器错误 C3032 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3032
dev_langs:
- C++
helpviewer_keywords:
- C3032
ms.assetid: 6a92bd8e-319f-4a99-aef4-a9021f6f9928
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 3b170983c75b5a1fac3bbed02f7c57bcd6c15bbd
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3032"></a>编译器错误 C3032
“var”: “clause”子句中的变量不能是不完整的“类型”类型  
  
 传递给某些子句的类型必须对编译器完全可见。  
  
 下面的示例生成 C3032:  
  
```  
// C3032.cpp  
// compile with: /openmp /link vcomps.lib  
#include "omp.h"  
  
struct Incomplete;  
extern struct Incomplete inc;  
  
int main() {  
   int i = 9;  
   #pragma omp parallel private(inc)   // C3032  
      ;  
  
   #pragma omp parallel private(i)     // OK  
      ;  
  
}  
```