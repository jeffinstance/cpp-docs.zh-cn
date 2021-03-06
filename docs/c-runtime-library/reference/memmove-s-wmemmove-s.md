---
title: memmove_s、wmemmove_s | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- wmemmove_s
- memmove_s
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-string-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- wmemmove_s
- memmove_s
dev_langs:
- C++
helpviewer_keywords:
- wmemmove_s function
- memmove_s function
ms.assetid: a17619e4-1307-4bb0-98c6-77f8c68dab2d
caps.latest.revision: 26
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 8ad54aafb747fcf8504c4a9812b2f09a788933d4
ms.sourcegitcommit: ef859ddf5afea903711e36bfd89a72389a12a8d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2018
---
# <a name="memmoves-wmemmoves"></a>memmove_s、wmemmove_s

将一个缓冲区移到另一个缓冲区。 如 [CRT 中的安全功能](../../c-runtime-library/security-features-in-the-crt.md)中所述，这些版本的 [memmove、wmemmove](memmove-wmemmove.md) 具有安全增强功能。

## <a name="syntax"></a>语法

```C
errno_t memmove_s(
   void *dest,
   size_t numberOfElements,
   const void *src,
   size_t count
);
errno_t wmemmove_s(
   wchar_t *dest,
   size_t numberOfElements,
   const wchar_t *src,
   size_t count
);
```

### <a name="parameters"></a>参数

*dest*<br/>
目标对象。

*numberOfElements*<br/>
目标缓冲区的大小。

*src*<br/>
源对象。

*count*<br/>
字节数 (**memmove_s**) 或字符 (**wmemmove_s**) 来复制。

## <a name="return-value"></a>返回值

如果成功，则为零；如果失败，则为错误代码

### <a name="error-conditions"></a>错误条件

|*dest*|*numberOfElements*|*src*|返回值|内容*目标*|
|------------|------------------------|-----------|------------------|------------------------|
|**NULL**|任何|任何|**EINVAL**|未修改|
|任何|任何|**NULL**|**EINVAL**|未修改|
|任何|< *计数*|任何|**ERANGE**|未修改|

## <a name="remarks"></a>备注

副本*计数*从的字符的字节*src*到*dest*。 如果某些区域的源区域和目标重叠， **memmove_s**可确保重叠区域中的原始源字节，将覆盖之前会复制。

如果*dest*或如果*src*是 null 指针，或者如果目标字符串过小，这些函数将调用无效参数处理程序中中, 所述[参数验证](../../c-runtime-library/parameter-validation.md) . 如果允许执行继续，则这些函数将返回**EINVAL**并设置**errno**到**EINVAL**。

## <a name="requirements"></a>要求

|例程|必需的标头|
|-------------|---------------------|
|**memmove_s**|\<string.h>|
|**wmemmove_s**|\<wchar.h>|

有关其他兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="example"></a>示例

```C
// crt_memmove_s.c
//
// The program demonstrates the
// memmove_s function which works as expected
// for moving overlapping regions.

#include <stdio.h>
#include <string.h>

int main()
{
   char str[] = "0123456789";

   printf("Before: %s\n", str);

   // Move six bytes from the start of the string
   // to a new position shifted by one byte. To protect against
   // buffer overrun, the secure version of memmove requires the
   // the length of the destination string to be specified.

   memmove_s((str + 1), strnlen(str + 1, 10), str, 6);

   printf_s(" After: %s\n", str);
}
```

### <a name="output"></a>输出

```Output
Before: 0123456789
After: 0012345789
```

## <a name="see-also"></a>请参阅

[缓冲区操作](../../c-runtime-library/buffer-manipulation.md)<br/>
[_memccpy](memccpy.md)<br/>
[memcpy、wmemcpy](memcpy-wmemcpy.md)<br/>
[strcpy_s、wcscpy_s、_mbscpy_s](strcpy-s-wcscpy-s-mbscpy-s.md)<br/>
[strcpy、wcscpy、_mbscpy](strcpy-wcscpy-mbscpy.md)<br/>
[strncpy_s、_strncpy_s_l、wcsncpy_s、_wcsncpy_s_l、_mbsncpy_s、_mbsncpy_s_l](strncpy-s-strncpy-s-l-wcsncpy-s-wcsncpy-s-l-mbsncpy-s-mbsncpy-s-l.md)<br/>
[strncpy、_strncpy_l、wcsncpy、_wcsncpy_l、_mbsncpy、_mbsncpy_l](strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l.md)<br/>
