---
title: "编译器警告 （等级 1） C4291 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4291
dev_langs:
- C++
helpviewer_keywords:
- C4291
ms.assetid: c2b95dea-38f2-4609-9104-707c30798da4
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 2a1c03e12805c35ce04322a7ffb4d48499a9a9f3
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4291"></a>编译器警告（等级 1）C4291
declaration： 找到了; 不匹配运算符 delete如果初始化引发异常，不会释放内存  
  
 放置[新](../../cpp/new-operator-cpp.md)使用其中没有任何放置[删除](../../cpp/delete-operator-cpp.md)。  
  
 当为具有运算符的对象分配内存**新**，该对象的构造函数中调用。 如果构造函数引发了异常，应释放已为对象分配任何内存。 这不会发生，除非运算符**删除**函数存在匹配运算符**新**。  
  
 如果使用运算符**新**不带任何额外自变量与编译[/GX](../../build/reference/gx-enable-exception-handling.md)， [/EHs](../../build/reference/eh-exception-handling-model.md)，或 /EHa 选项启用异常处理，编译器将生成代码调用运算符**删除**在构造函数引发异常。  
  
 如果你使用的放置形式**新**运算符 （带参数的形式除了大小的分配） 和对象的构造函数引发了异常，则编译器仍将生成代码来调用运算符**删除**; 但它仅会如果运算符的放置形式**删除**存在匹配运算符的放置形式**新**分配内存。 例如:  
  
```  
// C4291.cpp  
// compile with: /EHsc /W1  
#include <malloc.h>  
  
class CList  
{  
public:  
   CList(int)  
   {  
      throw "Fail!";  
   }  
};  
  
void* operator new(size_t size, char* pszFilename, int nLine)  
{  
   return malloc(size);  
}  
  
int main(void)  
{  
   try  
   {  
      // This will call ::operator new(unsigned int) to allocate heap  
      // memory. Heap memory pointed to by pList1 will automatically be  
      // deallocated by a call to ::operator delete(void*) when  
      // CList::CList(int) throws an exception.  
      CList* pList1 = new CList(10);  
   }  
   catch (...)  
   {  
   }  
  
   try  
   {  
      // This will call the overloaded ::operator new(size_t, char*, int)  
      // to allocate heap memory. When CList::CList(int) throws an  
      // exception, ::operator delete(void*, char*, int) should be called  
      // to deallocate the memory pointed to by pList2. Since  
      // ::operator delete(void*, char*, int) has not been implemented,  
      // memory will be leaked when the deallocation cannot occur.  
      CList* pList2 = new(__FILE__, __LINE__) CList(20);   // C4291  
   }  
   catch (...)  
   {  
   }  
}  
```  
  
 上面的示例生成警告 C4291，因为没有的运算符的放置形式**删除**已定义匹配运算符的放置形式**新**。 若要解决此问题，插入以下代码上述**主要**。 请注意，所有重载运算符**删除**函数参数与匹配的重载运算符**新**，除第一个参数。  
  
```  
void operator delete(void* pMem, char* pszFilename, int nLine)  
{  
   free(pMem);  
}  
```