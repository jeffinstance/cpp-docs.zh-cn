---
title: "创建工具提示的方法 |Microsoft 文档"
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
- CToolTipCtrl class [MFC], creating tool tips
- tool tips [MFC], tool tip controls
- tool tips [MFC], creating
ms.assetid: b015e9f4-ddfb-49a4-a5a6-fa2d45e4d328
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: c2d38bd76ff5c8d06daf474cf1c1dcc0286183bc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="methods-of-creating-tool-tips"></a>创建工具提示的方法
MFC 提供了三个类来创建和管理工具提示控件： [CWnd](../mfc/reference/cwnd-class.md)， [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md)， [CToolTipCtrl](../mfc/reference/ctooltipctrl-class.md)和[CMFCToolTipCtrl](../mfc/reference/cmfctooltipctrl-class.md). 这些类中的工具提示成员函数包装 Windows 公共控件 API。 类 `CToolBarCtrl` 和类 `CToolTipCtrl` 类派生自类 `CWnd`。  
  
 `CWnd`提供四个成员函数，以创建和管理工具提示： [EnableToolTips](../mfc/reference/cwnd-class.md#enabletooltips)， [CancelToolTips](../mfc/reference/cwnd-class.md#canceltooltips)， [FilterToolTipMessage](../mfc/reference/cwnd-class.md#filtertooltipmessage)，和[OnToolHitTest](../mfc/reference/cwnd-class.md#ontoolhittest)。 有关它们如何实现工具提示的详细信息，请参阅这些单独的成员函数。  
  
 如果你创建工具栏使用`CToolBarCtrl`，可实现直接使用以下成员函数为工具栏的工具提示： [GetToolTips](../mfc/reference/ctoolbarctrl-class.md#gettooltips)和[SetToolTips](../mfc/reference/ctoolbarctrl-class.md#settooltips)。 请参阅这些单独的成员函数和[处理工具提示通知](../mfc/handling-tool-tip-notifications.md)有关它们如何实现工具提示的详细信息。  
  
 `CToolTipCtrl` 类提供了 Windows 公共工具提示控件的功能。 一个工具提示控件可以提供多个工具的信息。 工具是一个窗口（如子窗口或控件）或窗口工作区中应用程序定义的矩形区域。 [CMFCToolTipCtrl](../mfc/reference/cmfctooltipctrl-class.md)类派生自`CToolTipCtrl`，并提供其他可视样式和功能。  
  
## <a name="see-also"></a>请参阅  
 [使用 CToolTipCtrl](../mfc/using-ctooltipctrl.md)   
 [控件](../mfc/controls-mfc.md)

