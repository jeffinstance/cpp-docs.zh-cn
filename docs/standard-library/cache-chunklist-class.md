---
title: cache_chunklist 类 | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- allocators/stdext::cache_chunklist
- allocators/stdext::cache_chunklist::allocate
- allocators/stdext::cache_chunklist::deallocate
dev_langs:
- C++
helpviewer_keywords:
- stdext::cache_chunklist
- stdext::cache_chunklist [C++], allocate
- stdext::cache_chunklist [C++], deallocate
ms.assetid: af19eccc-4ae7-4a34-bbb2-81e397424cb9
caps.latest.revision: 17
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 8f30cde375f05dbba30da58ad3e71aa5e9bac11c
ms.sourcegitcommit: dd1a509526fa8bb18e97ab7bc7b91cbdb3ec7059
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="cachechunklist-class"></a>cache_chunklist 类

定义分配和释放单个大小内存块的[块分配器](../standard-library/allocators-header.md)。

## <a name="syntax"></a>语法

```cpp
template <std::size_t Sz, std::size_t Nelts = 20>
class cache_chunklist
```

### <a name="parameters"></a>参数

|参数|描述|
|---------------|-----------------|
|`Sz`|数组中要分配的元素数目。|

## <a name="remarks"></a>备注

此模板类使用 `operator new` 分配原始内存的区块，并对块进行细分以在必要时为内存块分配存储空间；其将释放的内存块存储在每个区块的独立释放列表中，并在未使用区块的任何内存块时使用 `operator delete` 释放区块。

每个内存块保留 `Sz` 个字节的可用内存和指向其所属于的区块的指针。 每个区块保留 `Nelts` 内存块、三个指针、一个 int 以及 `operator new` 和 `operator delete` 所需的数据。

### <a name="constructors"></a>构造函数

|构造函数|描述|
|-|-|
|[cache_chunklist](#cache_chunklist)|构造 `cache_chunklist` 类型的对象。|

### <a name="member-functions"></a>成员函数

|成员函数|描述|
|-|-|
|[allocate](#allocate)|分配内存块。|
|[deallocate](#deallocate)|从指定位置开始从存储中释放指定数量的的对象。|

## <a name="requirements"></a>要求

**标头：**\<allocators>

**命名空间：** stdext

## <a name="allocate"></a>  cache_chunklist::allocate

分配内存块。

```cpp
void *allocate(std::size_t count);
```

### <a name="parameters"></a>参数

|参数|描述|
|---------------|-----------------|
|`count`|数组中要分配的元素数目。|

### <a name="return-value"></a>返回值

指向已分配对象的指针。

### <a name="remarks"></a>备注

## <a name="cache_chunklist"></a>  cache_chunklist::cache_chunklist

构造 `cache_chunklist` 类型的对象。

```cpp
cache_chunklist();
```

### <a name="remarks"></a>备注

## <a name="deallocate"></a>  cache_chunklist::deallocate

从指定位置开始从存储中释放指定数量的的对象。

```cpp
void deallocate(void* ptr, std::size_t count);
```

### <a name="parameters"></a>参数

|参数|描述|
|---------------|-----------------|
|`ptr`|指向要从存储中释放的第一个对象的指针。|
|`count`|要从存储中释放的对象数量。|

### <a name="remarks"></a>备注

## <a name="see-also"></a>请参阅

[\<allocators>](../standard-library/allocators-header.md)<br/>
