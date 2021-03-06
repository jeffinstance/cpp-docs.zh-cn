---
title: "&lt;c&gt; （Visual c + +） |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-ide
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- <c>
dev_langs:
- C++
helpviewer_keywords:
- <c> C++ XML tag
- c C++ XML tag
ms.assetid: 3b23fc0f-e10d-4dd0-b197-48a46cbddd9f
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: b8d4ea984864975196251c9f362283a0df1932cb
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ltcgt-visual-c"></a>&lt;c&gt; （Visual c + +）
\<C > 标记指示应为代码将标记为说明中的文本。 使用 [\<code>](../ide/code-visual-cpp.md) 指示作为代码的多行文本。  
  
## <a name="syntax"></a>语法  
  
```  
<c>text</c>  
```  
  
#### <a name="parameters"></a>参数  
 `text`  
 你想要指示为代码的文本。  
  
## <a name="remarks"></a>备注  
 使用 [/doc](../build/reference/doc-process-documentation-comments-c-cpp.md) 进行编译可以将文档注释处理到文件中。  
  
## <a name="example"></a>示例  
  
```  
// xml_c_tag.cpp  
// compile with: /doc /LD  
// post-build command: xdcmake xml_c_tag.xdc  
  
/// Text for class MyClass.  
class MyClass {  
public:  
   int m_i;  
   MyClass() : m_i(0) {}  
  
   /// <summary><c>MyMethod</c> is a method in the <c>MyClass</c> class.  
   /// </summary>  
   int MyMethod(MyClass * a) {  
      return a -> m_i;  
   }  
};  
```  
  
## <a name="see-also"></a>请参阅  
 [XML 文档](../ide/xml-documentation-visual-cpp.md)