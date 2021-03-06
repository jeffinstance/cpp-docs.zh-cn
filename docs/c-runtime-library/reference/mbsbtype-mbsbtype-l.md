---
title: _mbsbtype、_mbsbtype_l | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- _mbsbtype_l
- _mbsbtype
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
- api-ms-win-crt-multibyte-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- mbsbtype
- mbsbtype_l
- _mbsbtype_l
- _mbsbtype
dev_langs:
- C++
helpviewer_keywords:
- _mbsbtype function
- mbsbtype function
- _mbsbtype_l function
- mbsbtype_l function
ms.assetid: 0d5dd91a-d32d-4f98-ac57-98dfc9e98eac
caps.latest.revision: 19
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: a8108372cd40aba6770136908b177dc82a9ff25e
ms.sourcegitcommit: ef859ddf5afea903711e36bfd89a72389a12a8d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2018
---
# <a name="mbsbtype-mbsbtypel"></a>_mbsbtype、_mbsbtype_l

返回字符串中字节的类型。

> [!IMPORTANT]
> 此 API 不能用于在 Windows 运行时中执行的应用程序。 有关详细信息，请参阅[通用 Windows 平台应用中不支持的 CRT 函数](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md)。

## <a name="syntax"></a>语法

```C
int _mbsbtype(
   const unsigned char *mbstr,
   size_t count
);
int _mbsbtype_l(
   const unsigned char *mbstr,
   size_t count,
   _locale_t locale
);
```

### <a name="parameters"></a>参数

*mbstr*<br/>
多字节字符序列的地址。

*count*<br/>
字符串头中的字节偏移量。

*locale*<br/>
要使用的区域设置。

## <a name="return-value"></a>返回值

**_mbsbtype**和 **_mbsbtype_l**返回一个整数值，该值指示指定的字节上测试的结果。 下表中的清单常量在 Mbctype.h 中定义。

|返回值|字节类型|
|------------------|---------------|
|**_MBC_SINGLE** (0)|单字节字符。 例如，在代码页 932， **_mbsbtype**如果指定的字节在范围内 0x20-0x7E 或 0xA1-0xDF 返回 0。|
|**_MBC_LEAD** (1)|多字节字符的前导字节。 例如，在代码页 932， **_mbsbtype**返回 1，如果指定的字节在范围内 0x81-0x9F 或 0xE0-0xFC。|
|**_MBC_TRAIL** (2)|多字节字符的尾随字节。 例如，在代码页 932， **_mbsbtype**返回 2，如果指定的字节在范围内 0x40-0x7E 或 0x80-0xFC。|
|**_MBC_ILLEGAL** (-1)|**NULL**字符串、 无效的字符，或**NULL**字节的字节偏移量位置之前找到*计数*中*mbstr*。|

## <a name="remarks"></a>备注

**_Mbsbtype**函数确定多字节字符字符串中字节的类型。 该函数将检查仅的字节偏移量位置*计数*中*mbstr*，忽略之前指定的字节的无效字符。

输出值受的设置**LC_CTYPE**的区域设置的类别设置影响; 请参阅[setlocale](setlocale-wsetlocale.md)有关详细信息。 此函数而无需的版本 **_l**后缀使用当前区域设置区域设置相关的行为; 的版本与 **_l**后缀是相同，但它使用传递的区域设置参数在相反。 有关详细信息，请参阅 [Locale](../../c-runtime-library/locale.md)。

如果输入的字符串是**NULL**，则调用无效参数处理程序，如中所述[参数验证](../../c-runtime-library/parameter-validation.md)。 如果允许执行继续，则**errno**设置为**EINVAL**和该函数将返回 **_MBC_ILLEGAL**。

## <a name="requirements"></a>要求

|例程|必需的标头|可选标头|
|-------------|---------------------|---------------------|
|**_mbsbtype**|\<mbstring.h>|\<mbctype.h>*|
|**_mbsbtype_l**|\<mbstring.h>|\<mbctype.h>*|

\*用作返回值的清单常量。

有关更多兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="see-also"></a>请参阅

[字节分类](../../c-runtime-library/byte-classification.md)<br/>
