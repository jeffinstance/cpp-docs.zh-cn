---
title: "非 MFC Dll： 概述 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- non-MFC DLLs [C++]
- DLLs [C++], non-MFC
ms.assetid: 1ed5d1ee-e20c-47d7-801d-87ea26a73842
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 3ce755f88e8a9efaaacd456206d599dd5db75443
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="non-mfc-dlls-overview"></a>非 MFC DLL：概述
非 MFC DLL 是在内部，不使用 MFC 的 DLL，可以由 MFC 或非 MFC 可执行文件调用 DLL 中导出的函数。 函数通常被导出从非 MFC DLL 使用标准的 C 接口。  
  
 有关非 MFC Dll 的详细信息，请参阅[动态链接库](http://msdn.microsoft.com/library/windows/desktop/ms682589)中[!INCLUDE[winsdkshort](../atl-mfc-shared/reference/includes/winsdkshort_md.md)]。  
  
## <a name="what-do-you-want-to-do"></a>你希望做什么？  
  
-   [演练： 创建和使用动态链接库](../build/walkthrough-creating-and-using-a-dynamic-link-library-cpp.md)  
  
-   [从 DLL 导出](../build/exporting-from-a-dll.md)  
  
-   [将可执行文件链接到 DLL](../build/linking-an-executable-to-a-dll.md)  
  
-   [初始化 DLL](../build/run-time-library-behavior.md#initializing-a-dll)  
  
## <a name="what-do-you-want-to-know-more-about"></a>你想进一步了解什么？  
  
-   [静态链接到 MFC 的规则 MFC Dll](../build/regular-dlls-statically-linked-to-mfc.md)  
  
-   [动态链接到 MFC 的规则 MFC Dll](../build/regular-dlls-dynamically-linked-to-mfc.md)  
  
-   [MFC 扩展 DLL：概述](../build/extension-dlls-overview.md)  
  
## <a name="see-also"></a>请参阅  
 [DLL 的类型](../build/kinds-of-dlls.md)