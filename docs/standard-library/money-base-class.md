---
title: money_base 类 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- xlocmon/std::money_base
dev_langs:
- C++
helpviewer_keywords:
- money_base class
ms.assetid: 1a303c15-9272-4f26-ae16-dcf43a0fd38a
caps.latest.revision: 19
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: a33e60ff54c7ec03ef806f5104513c9838449190
ms.sourcegitcommit: dd1a509526fa8bb18e97ab7bc7b91cbdb3ec7059
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="moneybase-class"></a>money_base 类

此类会描述常用于所有模板类 [moneypunct](../standard-library/moneypunct-class.md) 专用化的枚举和结构。

## <a name="syntax"></a>语法

```cpp
struct pattern
{
   char field[_PATTERN_FIELD_SIZE];
};
```

## <a name="remarks"></a>备注

枚举 **part** 描述结构模式中数组字段元素中的可能值。 **part** 的值为：

- **none** - 用于匹配零个或多个空格，或不生成任何内容。

- **sign** - 用于匹配或生成正负号。

- **space** - 用于匹配零个或多个空格，或生成空格。

- **symbol** - 用于匹配或生成货币符号。

- **value** - 用于匹配或生成货币值。

## <a name="requirements"></a>要求

**标头：** \<locale>

**命名空间：** std

## <a name="see-also"></a>请参阅

[C++ 标准库中的线程安全](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
