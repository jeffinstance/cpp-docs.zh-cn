---
title: numpunct_byname 类 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- xlocnum/std::numpunct_byname
dev_langs:
- C++
helpviewer_keywords:
- numpunct_byname class
ms.assetid: 18412924-e085-4771-b5e9-7a200cbdd7c0
caps.latest.revision: 24
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: cfa7b3071f75784b7aece2fdd391775eae9027a5
ms.sourcegitcommit: dd1a509526fa8bb18e97ab7bc7b91cbdb3ec7059
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="numpunctbyname-class"></a>numpunct_byname 类

一种派生模板类，用于描述一个对象来充当给定区域设置的 `numpunct` facet，从而对数字和布尔表达式进行格式化和标点设置。

## <a name="syntax"></a>语法

```cpp
template <class CharType>
class numpunct_byname : public numpunct<Elem> {
public:
    explicit numpunct_byname(
    const char* _Locname,
    size_t _Refs = 0);

    explicit numpunct_byname(
    const string& _Locname,
    size_t _Refs = 0);

protected:
    virtual ~numpunct_byname();

};
```

## <a name="remarks"></a>备注

其行为由[已命名的](../standard-library/locale-class.md#name)区域设置 `_Locname` 决定。 构造函数通过 [numpunct](../standard-library/numpunct-class.md#numpunct)\<CharType>( `_Refs`) 初始化其基对象。

## <a name="requirements"></a>要求

**标头：** \<locale>

**命名空间：** std

## <a name="see-also"></a>请参阅

[C++ 标准库中的线程安全](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
