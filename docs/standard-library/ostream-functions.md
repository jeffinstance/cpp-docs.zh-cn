---
title: '&lt;ostream&gt; 函数 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- ostream/std::swap
- ostream/std::endl
- ostream/std::ends
- ostream/std::flush
ms.assetid: d6e56cc0-c8df-4dbe-be10-98e14c35ed3a
caps.latest.revision: 15
manager: ghogen
helpviewer_keywords:
- std::swap [C++]
- std::endl [C++]
- std::ends [C++]
- std::flush [C++]
ms.openlocfilehash: 41463d912b3ab33812a1f7c0a0ea5f8172036e57
ms.sourcegitcommit: dd1a509526fa8bb18e97ab7bc7b91cbdb3ec7059
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="ltostreamgt-functions"></a>&lt;ostream&gt; 函数

这些是中定义的全局模板函数&lt;ostream&gt;。 对于成员函数，请参阅[basic_ostream 类](basic-ostream-class.md)文档。

||||
|-|-|-|
|[endl](#endl)|[ends](#ends)|[flush](#flush)|
|[swap](#swap)|

## <a name="endl"></a>endl

终止行并刷新缓冲区。

```cpp
template class<Elem, Tr>
basic_ostream<Elem, Tr>& endl(
   basic_ostream<Elem, Tr>& Ostr);
```

### <a name="parameters"></a>参数

*Elem*元素类型。

*Ostr*类型的对象**basic_ostream**。

*Tr*字符特征。

### <a name="return-value"></a>返回值

类型的对象**basic_ostream**。

### <a name="remarks"></a>备注

操控器调用*Ostr*。[put](../standard-library/basic-ostream-class.md#put)(*Ostr*。[扩大](../standard-library/basic-ios-class.md#widen)(\n))，然后调用*Ostr*。[刷新](../standard-library/basic-ostream-class.md#flush)。 它将返回*Ostr*。

### <a name="example"></a>示例

```cpp
// ostream_endl.cpp
// compile with: /EHsc
#include <iostream>

int main( )
{
   using namespace std;
   cout << "testing" << endl;
}
```

```Output
testing
```

## <a name="ends"></a>结尾

终止字符串。

```cpp
template class<Elem, Tr>
basic_ostream<Elem, Tr>& ends(
   basic_ostream<Elem, Tr>& Ostr);
```

### <a name="parameters"></a>参数

*Elem*元素类型。

*Ostr*类型的对象**basic_ostream**。

*Tr*字符特征。

### <a name="return-value"></a>返回值

类型的对象**basic_ostream**。

### <a name="remarks"></a>备注

操控器调用*Ostr*。[put](../standard-library/basic-ostream-class.md#put)(*Elem*(\0'))。 它将返回*Ostr*。

### <a name="example"></a>示例

```cpp
// ostream_ends.cpp
// compile with: /EHsc
#include <iostream>

int main( )
{
   using namespace std;
   cout << "a";
   cout << "b" << ends;
   cout << "c" << endl;
}
```

```Output
ab c
```

## <a name="flush"></a>flush

刷新缓冲区。

```cpp
template class<Elem, Tr>
basic_ostream<Elem, Tr>& flush(
   basic_ostream<Elem, Tr>& Ostr);
```

### <a name="parameters"></a>参数

*Elem*元素类型。

*Ostr*类型的对象**basic_ostream**。

*Tr*字符特征。

### <a name="return-value"></a>返回值

类型的对象**basic_ostream**。

### <a name="remarks"></a>备注

操控器调用*Ostr*。[刷新](../standard-library/basic-ostream-class.md#flush)。 它将返回*Ostr*。

### <a name="example"></a>示例

```cpp
// ostream_flush.cpp
// compile with: /EHsc
#include <iostream>

int main( )
{
   using namespace std;
   cout << "testing" << flush;
}
```

```Output
testing
```

## <a name="swap"></a>swap

交换两个值**basic_ostream**对象。

```cpp
template <class Elem, class Tr>
void swap(
   basic_ostream<Elem, Tr>& left,
   basic_ostream<Elem, Tr>& right);
```

### <a name="parameters"></a>参数

*Elem*元素类型。

*Tr*字符特征。

*左*的左值引用**basic_ostream**对象。

*右*的左值引用**basic_ostream**对象。

### <a name="remarks"></a>备注

模板函数**交换**执行`left.swap(right)`。

## <a name="see-also"></a>请参阅

[\<ostream>](../standard-library/ostream.md)
