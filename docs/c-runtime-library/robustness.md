---
title: "可靠性 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- c.runtime
dev_langs:
- C++
helpviewer_keywords:
- robustness [CRT]
ms.assetid: 7f1a87f8-eff9-4b76-ae9b-d133d3de6adf
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: fb071b615d87ab1b605c78e5ba0645be139fba1b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="robustness"></a>稳定性
使用以下 C 运行时库函数以提高程序的可靠性。  
  
### <a name="run-time-robustness-functions"></a>运行时可靠性函数  
  
|函数|使用|  
|--------------|---------|  
|[_set_new_handler](../c-runtime-library/reference/set-new-handler.md)|如果 `new` 运算符无法分配内存，则将控制权传输到错误处理机制。|  
|[_set_se_translator](../c-runtime-library/reference/set-se-translator.md)|将 Win32 异常（C 结构的异常）处理为 C++ 类型的异常。|  
|[set_terminate](../c-runtime-library/reference/set-terminate-crt.md)|安装要由 [terminate](../c-runtime-library/reference/terminate-crt.md) 调用的自身的终止函数。|  
|[set_unexpected](../c-runtime-library/reference/set-unexpected-crt.md)|安装要由 [unexpected](../c-runtime-library/reference/unexpected-crt.md) 调用的自身的终止函数。|  
  
## <a name="see-also"></a>请参阅  
 [按类别分的运行时例程](../c-runtime-library/run-time-routines-by-category.md)   
 [SetUnhandledExceptionFilter](http://msdn.microsoft.com/library/windows/desktop/ms680634.aspx)