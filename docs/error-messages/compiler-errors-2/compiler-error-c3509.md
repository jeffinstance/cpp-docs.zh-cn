---
title: "编译器错误 C3509 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3509
dev_langs:
- C++
helpviewer_keywords:
- C3509
ms.assetid: cc2db39a-2f98-4e40-b803-496e585494e6
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 16b9e4c2dd49dc966ccb060553e5fd2f12e7635b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3509"></a>编译器错误 C3509
type： 无效的自动化返回类型;当参数标记 retval，返回类型必须是 void，HRESULT 或 SCODE  
  
 COM 接口中的方法必须返回 void 还是的 HRESULT。  
  
 下面的示例生成 C3509:  
  
```  
// C3509.cpp  
#define _ATL_DEBUG_QI  
  
#define WIN32_LEAN_AND_MEAN   // Exclude rarely-used stuff from Windows headers  
#define STRICT  
#ifndef _WIN32_WINNT  
#define _WIN32_WINNT 0x0400  
#endif  
  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
extern CComModule _Module;  
#include <atlcom.h>  
#include <atlctl.h>  
#include <atlstr.h>  
  
[module(name=oso)];  
  
[dispinterface, uuid(00000000-0000-0000-0000-000000000001)]  
__interface I {  
   [id(1)] int f([out, retval] int*);   // C3509  
   // try the following line instead  
   // [id(1)] void f([out, retval] int*);  
};  
  
[coclass, uuid(00000000-0000-0000-0000-000000000002)]  
struct C : I {  
   int f(int*) {  
   // try the following line instead, and delete return statement  
   // void f(int*) {  
      return 0;  
   }  
};  
  
int main() {  
}  
```