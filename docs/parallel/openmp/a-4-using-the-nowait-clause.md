---
title: "使用 nowait 子句 A.4 |Microsoft 文档"
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
ms.assetid: d3de2111-05ea-4ee3-a66c-57bd988712af
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: bf910f1223a4ccfdd85734ef9bd314d5664679ec
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="a4---using-the-nowait-clause"></a>A.4   使用 nowait 子句
如果有多个独立循环并行区域内的，则可以使用`nowait`子句 ([部分 2.4.1](../../parallel/openmp/2-4-1-for-construct.md)上第 11 页) 以避免末尾的隐含的屏障`for`指令，如下所示：  
  
```  
#pragma omp parallel  
{  
    #pragma omp for nowait  
        for (i=1; i<n; i++)  
             b[i] = (a[i] + a[i-1]) / 2.0;  
    #pragma omp for nowait  
        for (i=0; i<m; i++)  
            y[i] = sqrt(z[i]);  
}  
```