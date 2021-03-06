---
title: "图像列表类型 |Microsoft 文档"
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
- lists [MFC], image
- image lists [MFC], types of
- CImageList class [MFC], types
ms.assetid: bee5e7c3-78f5-4037-a136-9c50d67cdee5
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 84a2118978d5ebd722d4fe56cdeec2aa0f74a94e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="types-of-image-lists"></a>图像列表类型
有两种类型的图像列表 ([CImageList](../mfc/reference/cimagelist-class.md)): 未添加蒙板和掩码。 "未添加蒙板的图像列表"包含颜色位图，其中包含一个或多个映像。 "蒙板的图像列表"包含的大小相等的两个位图。 第一个是包含的图像的颜色位图，第二个是包含一系列的掩码的单色位图 — 一个用于在第一个位图中的每个图像。  
  
 重载之一**创建**成员函数采用一个标志，用于指示是否屏蔽的图像列表。 （其他重载创建蒙板的图像列表。）  
  
 未添加蒙板的图像绘制时，只需复制到目标设备上下文;也就是说，它通过设备上下文的现有背景色绘制。 蒙板的图像绘制时，使用的位掩码，其中的目标设备上下文的背景色显示通过，则通常生成在位图中的透明区域合并的映像的位。 在绘制蒙板的图像时，你可以指定多个绘制样式。 例如，你可以指定抖色映像以指示所选的对象。  
  
## <a name="see-also"></a>请参阅  
 [使用 CImageList](../mfc/using-cimagelist.md)   
 [控件](../mfc/controls-mfc.md)

