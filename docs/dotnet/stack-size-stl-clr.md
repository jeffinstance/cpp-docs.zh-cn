---
title: "stack:: size (STL/CLR) |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- cliext::stack::size
dev_langs:
- C++
helpviewer_keywords:
- size member [STL/CLR]
ms.assetid: 6113e649-a4f9-4021-8131-34cee4bc8ca0
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 960a32b259069fc110ba1dd910c9f11cf9423726
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="stacksize-stlclr"></a>stack::size (STL/CLR)
对元素数进行计数。  
  
## <a name="syntax"></a>语法  
  
```  
size_type size();  
```  
  
## <a name="remarks"></a>备注  
 成员函数将返回受控序列的长度。 用于确定当前受控序列中的元素的数目。 如果你关注的只是序列是否具有非零大小，请参阅[stack:: empty (STL/CLR)](../dotnet/stack-empty-stl-clr.md)`()`。  
  
## <a name="example"></a>示例  
  
```  
// cliext_stack_size.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine("size() = {0} starting with 3", c1.size());   
  
// pop an item and reinspect   
    c1.pop();   
    System::Console::WriteLine("size() = {0} after popping", c1.size());   
  
// add two elements and reinspect   
    c1.push(L'a');   
    c1.push(L'b');   
    System::Console::WriteLine("size() = {0} after adding 2", c1.size());   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
size() = 3 starting with 3  
size() = 2 after popping  
size() = 4 after adding 2  
```  
  
## <a name="requirements"></a>惠?  
 **标头：** \<cliext/堆栈 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>请参阅  
 [堆栈 (STL/CLR)](../dotnet/stack-stl-clr.md)   
 [stack::empty (STL/CLR)](../dotnet/stack-empty-stl-clr.md)