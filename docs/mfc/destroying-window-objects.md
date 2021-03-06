---
title: "销毁窗口对象 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- frame windows [MFC], destroying
- window objects [MFC], deleting
- window objects [MFC], destroying
- window objects [MFC], removing
ms.assetid: 3241fea0-c614-4a25-957d-20f21bd5fd0c
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 8e7b8b2cf605e0f53418755b65151fd9eb2cff5d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="destroying-window-objects"></a>销毁窗口对象
必须格外小心使用你自己的子窗口时用户已完成与窗口销毁 c + + 窗口对象。 如果这些对象不会被销毁，你的应用程序将不会恢复其内存。 幸运的是，框架管理窗口析构，以及创建框架窗口、 视图和对话框。 如果你创建其他 windows，你将负责销毁它们。  
  
## <a name="what-do-you-want-to-know-more-about"></a>你想进一步了解什么  
  
-   [窗口析构序列](../mfc/window-destruction-sequence.md)  
  
-   [分配和取消分配窗口内存](../mfc/allocating-and-deallocating-window-memory.md)  
  
-   [将 CWnd 从其 HWND 分离](../mfc/detaching-a-cwnd-from-its-hwnd.md)  
  
-   [常用窗口创建序列](../mfc/general-window-creation-sequence.md)  
  
-   [销毁框架窗口](../mfc/destroying-frame-windows.md)  
  
## <a name="see-also"></a>请参阅  
 [窗口对象](../mfc/window-objects.md)

