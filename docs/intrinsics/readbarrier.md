---
title: _ReadBarrier | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- _ReadBarrier
dev_langs:
- C++
helpviewer_keywords:
- _ReadBarrier intrinsic
ms.assetid: f9e54a92-61bc-4f55-8195-b8932065a796
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: d76238ed0c3ae66dc153a0a2066d5463a130b859
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/23/2018
---
# <a name="readbarrier"></a>_ReadBarrier  
  
**Microsoft 专用**  
  
 限制可重新排列调用点上的内存访问操作的编译器优化。  
  
> [!CAUTION]
>  已全部弃用且不应使用 `_ReadBarrier`、`_WriteBarrier` 和 `_ReadWriteBarrier` 编译器内部函数和 `MemoryBarrier` 宏。 对于线程间通信使用机制例如[atomic_thread_fence](../standard-library/atomic-functions.md#atomic_thread_fence)和[std::atomic\<T >](../standard-library/atomic.md)中定义[c + + 标准库](../standard-library/cpp-standard-library-reference.md). 硬件访问，请使用[/volatile:iso](../build/reference/volatile-volatile-keyword-interpretation.md)一起使用的编译器选项[易失性](../cpp/volatile-cpp.md)关键字。  
  
## <a name="syntax"></a>语法  
  
```  
void _ReadBarrier(void);  
```  
  
## <a name="requirements"></a>惠?  
  
|内部函数|体系结构|  
|---------------|------------------|  
|`_ReadBarrier`|x86, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
  
 **标头文件** \<intrin.h >  
  
## <a name="remarks"></a>备注  
 `_ReadBarrier` 内部函数将限制可删除或重新排列调用点上的内存访问操作的编译器优化。  
  
**结束 Microsoft 专用**  
  
## <a name="see-also"></a>请参阅  
 [编译器内部函数](../intrinsics/compiler-intrinsics.md)   
 [关键字](../cpp/keywords-cpp.md)