---
title: "编译器错误 C2051 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2051
dev_langs:
- C++
helpviewer_keywords:
- C2051
ms.assetid: 81c0469a-78e2-49fa-bd76-97cdb135e3ea
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: a6e2cb09a0789516913ea88818d110c756cb2bd4
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2051"></a>编译器错误 C2051
case 表达式不是常量  
  
 Case 表达式必须是整数常量。  
  
 下面的示例生成 C2051:  
  
```  
// C2051.cpp  
class X {};  
  
int main() {  
   static X x;  
   int i = 0;  
  
   switch (i) {  
      case x:   // C2051 use constant expression to resolve error  
         break;  
      default:  
         break;  
   }  
}  
```  
  
 可能的解决方法：  
  
```  
// C2051b.cpp  
class X {};  
  
int main() {  
   static X x;  
   int i = 0;  
  
   switch (i) {  
      case 1:  
         break;  
      default:  
         break;  
   }  
}  
```