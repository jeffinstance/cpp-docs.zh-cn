---
title: "编译器错误 C2186 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2186
dev_langs:
- C++
helpviewer_keywords:
- C2186
ms.assetid: 284bfb7e-ab85-4fcb-9864-1ddf7f6c94ae
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: a037382ebbc87cbb480a78eadd9439c1ce48bee7
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2186"></a>编译器错误 C2186
“operator”：“void”类型的操作数非法  
  
 运算符有 `void` 操作数。  
  
 下面的示例生成 C2186：  
  
```  
// C2186.cpp  
// compile with: /c  
void func1( void );  
int  func2( void );  
int i = 2 + func1();   // C2186 func1() is type void  
int j = 2 + func2();   // OK both operands are type int  
```