---
title: "我是否必须从 CObject 中派生新类？ | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CObject
dev_langs:
- C++
helpviewer_keywords:
- derived classes [MFC], from CObject
- CObject class [MFC], when to use
ms.assetid: 26021031-feaf-424c-80d1-9547c4409d6a
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: c485bba4d62d279b0f17b887080284940a8bbdd5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="do-i-have-to-derive-new-classes-from-cobject"></a>我是否必须从 CObject 中派生新类？
不，您不会。  
  
 从派生类[CObject](../mfc/reference/cobject-class.md)时需要提供，如序列化或动态可的功能。 许多数据类需要序列化到文件中，因此，通常最好从 `CObject` 派生。 从派生类的一个示例的`CObject`，请参阅[Scribble 示例](../visual-cpp-samples.md)。  
  
## <a name="see-also"></a>请参阅  
 [CObject 类：常见问题](../mfc/cobject-class-frequently-asked-questions.md)
