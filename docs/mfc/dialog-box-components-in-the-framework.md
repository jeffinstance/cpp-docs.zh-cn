---
title: "框架中的对话框组件 |Microsoft 文档"
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
- MFC dialog boxes [MFC], creating
- dialog classes [MFC], dialog box components
- MFC dialog boxes [MFC], about MFC dialog boxes
- dialog templates [MFC], MFC framework
- MFC dialog boxes [MFC], dialog resource
ms.assetid: 592db160-0a8a-49be-ac72-ead278aca53f
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 840e66def6a908b26b5021537eddee68c50a9628
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="dialog-box-components-in-the-framework"></a>框架中的对话框组件
在 MFC 框架中，对话框有两个组件：  
  
-   对话框模板资源，用来指定对话框的控件及其位置。  
  
     对话框资源存储 Windows 从中创建并显示对话框窗口的对话框模板。 该模板指定对话框的特征，包括其大小、位置、样式以及对话框的控件的类型和位置。 您通常会使用作为资源存储的对话框模板，但您也可以在内存中创建自己的模板。  
  
-   对话框类，派生自[CDialog](../mfc/reference/cdialog-class.md)，用于提供管理对话框的编程接口。  
  
     对话框是一个窗口，它在可见时将附加到 Windows 窗口。 创建对话框窗口后，对话框模板资源将用作用于创建对话框的子窗口控件的模板。  
  
## <a name="see-also"></a>请参阅  
 [对话框](../mfc/dialog-boxes.md)   
 [对话框的生命周期](../mfc/life-cycle-of-a-dialog-box.md)

