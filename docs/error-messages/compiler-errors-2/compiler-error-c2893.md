---
title: "编译器错误 C2893 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2893
dev_langs:
- C++
helpviewer_keywords:
- C2893
ms.assetid: ec0cbe43-005d-45da-8742-aaeb9b81d28e
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: d6a926b6cf935d1910681b77d95f60847205bc05
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2893"></a>编译器错误 C2893
未能特殊化函数模板的模板名称  
  
 编译器未能特殊化函数模板。 可以有多种原因会导致此错误。  
  
 通常情况下，解决 C2893 错误的方法是先查看函数的签名并确保可以实例化每个类型。  
  
## <a name="example"></a>示例  
 C2893 的发生是因为`f`的模板参数`T`推导为`std::map<int,int>`，但`std::map<int,int>`不具备成员`data_type`(`T::data_type`不使用实例化`T = std::map<int,int>`。)。 下面的示例生成 C2893。  
  
```  
// C2893.cpp  
// compile with: /c /EHsc  
#include<map>  
using namespace std;  
class MyClass {};  
  
template<class T>   
inline typename T::data_type  
// try the following line instead  
// inline typename  T::mapped_type  
f(T const& p1, MyClass const& p2);  
  
template<class T>  
void bar(T const& p1) {  
    MyClass r;  
    f(p1,r);   // C2893  
}  
  
int main() {  
   map<int,int> m;  
   bar(m);  
}  
```