---
title: "stack:: pop (STL/CLR) |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- cliext::stack::pop
dev_langs:
- C++
helpviewer_keywords:
- pop member [STL/CLR]
ms.assetid: b7565385-9e6b-432d-8c71-c62c9c6ad90d
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 059e65ff61f478a854364c7c128573f2b3486bd1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="stackpop-stlclr"></a>stack::pop (STL/CLR)
移除的最后一个元素。  
  
## <a name="syntax"></a>语法  
  
```  
void pop();  
```  
  
## <a name="remarks"></a>备注  
 成员函数删除受控序列，必须为非空的最后一个元素。 你可以使用它来缩短在后面的一个元素的堆栈。  
  
## <a name="example"></a>示例  
  
```  
// cliext_stack_pop.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// pop an element and redisplay   
    c1.pop();   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
a b  
```  
  
## <a name="requirements"></a>惠?  
 **标头：** \<cliext/堆栈 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>请参阅  
 [堆栈 (STL/CLR)](../dotnet/stack-stl-clr.md)   
 [stack::push (STL/CLR)](../dotnet/stack-push-stl-clr.md)