---
title: "运算符&lt;(deque) (STL/CLR) |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- cliext::deque::operator<
dev_langs:
- C++
helpviewer_keywords:
- operator< member [STL/CLR]
ms.assetid: f2fa1bb1-bc0a-4e9e-826b-6b72a5543b29
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 48c88a01bbab5bb6fe6742d568db2f6c8cf11bcc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="operatorlt-deque-stlclr"></a>运算符&lt;(deque) (STL/CLR)
Deque 小于比较。  
  
## <a name="syntax"></a>语法  
  
```  
template<typename Value>  
    bool operator<(deque<Value>% left,  
        deque<Value>% right);  
```  
  
#### <a name="parameters"></a>参数  
 左  
 要比较的左容器。  
  
 右  
 要比较的右容器。  
  
## <a name="remarks"></a>备注  
 运算符函数返回 true 当对于最低的位置`i`为其`!(right[i] < left[i])`很还 true， `left[i] < right[i]`。 否则，它将返回`left->size() < right->size()`用于测试是否`left`进行排序之前`right`两个 deque 何时比较的元素的元素。  
  
## <a name="example"></a>示例  
  
```  
// cliext_deque_operator_lt.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    cliext::deque<wchar_t> c2;   
    c2.push_back(L'a');   
    c2.push_back(L'b');   
    c2.push_back(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] < [a b c] is {0}",   
        c1 < c1);   
    System::Console::WriteLine("[a b c] < [a b d] is {0}",   
        c1 < c2);   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
 a b d  
[a b c] < [a b c] is False  
[a b c] < [a b d] is True  
```  
  
## <a name="requirements"></a>惠?  
 **标头：** \<cliext/q u e >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>请参阅  
 [deque (STL/CLR)](../dotnet/deque-stl-clr.md)   
 [运算符 = = (deque) (STL/CLR)](../dotnet/operator-equality-deque-stl-clr.md)   
 [deque:: operator ！ = (STL/CLR)](../dotnet/deque-operator-inequality-stl-clr.md)   
 [运算符 > = (deque) (STL/CLR)](../dotnet/operator-greater-or-equal-deque-stl-clr.md)   
 [运算符 > (deque) (STL/CLR)](../dotnet/operator-greater-than-deque-stl-clr.md)   
 [operator<= (deque) (STL/CLR)](../dotnet/operator-less-or-equal-deque-stl-clr.md)