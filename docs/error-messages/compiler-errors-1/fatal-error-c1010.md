---
title: "错误 C1010 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C1010
dev_langs:
- C++
helpviewer_keywords:
- C1010
ms.assetid: dfd035f1-a7a2-40bc-bc92-dc4d7f456767
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 8b2123118be2a8a382f6b718499c5af16f88d111
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="fatal-error-c1010"></a>错误 C1010
查找预编译头时意外的文件尾。 是否忘记添加 #include 名称对源？  
  
 使用指定的包含文件[/Yu](../../build/reference/yu-use-precompiled-header-file.md)源文件中未列出。  默认情况下，在大多数 Visual c + + 项目类型中启用了此选项，并且"stdafx.h"默认值包括此选项指定的文件。  
  
 在 Visual Studio 环境中，使用以下方法之一来解决此错误：  
  
-   如果你的项目中不使用预编译标头，设置**创建/使用预编译标头**属性源文件复制到**不使用预编译头**。 若要设置此编译器选项，请按照下列步骤：  
  
    1.  在项目的解决方案资源管理器窗格中，右键单击项目名称，然后单击**属性**。  
  
    2.  在左窗格中，单击**C/c + +**文件夹。  
  
    3.  单击**预编译标头**节点。  
  
    4.  在右窗格中，单击**创建/使用预编译标头**，然后单击**不使用预编译头**。  
  
-   请确保不要意外删除、 重命名或删除了标头文件 (默认情况下，stdafx.h) 从当前项目。 此文件还需要在你使用的源文件中的任何其他代码之前包含**#include"stdafx.h"**。 (此标头文件指定为**通过文件创建/使用 PCH**项目属性)