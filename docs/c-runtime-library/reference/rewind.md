---
title: rewind | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- rewind
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
- api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- rewind
dev_langs:
- C++
helpviewer_keywords:
- rewind function
- repositioning file pointers
- file pointers [C++], repositioning
- file pointers [C++]
ms.assetid: 1a460ce1-28d8-4b5e-83a6-633dca29c28a
caps.latest.revision: 11
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 48e3f54f20d763bb396db8671725b8f81ba654a8
ms.sourcegitcommit: ef859ddf5afea903711e36bfd89a72389a12a8d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2018
---
# <a name="rewind"></a>rewind

重新定位指向文件开头的文件指针。

## <a name="syntax"></a>语法

```C
void rewind(
   FILE *stream
);
```

### <a name="parameters"></a>参数

*流*指向**文件**结构。

## <a name="remarks"></a>备注

**Rewind**函数将与关联的文件指针重新定位*流*到文件的开头。 对 **rewind** 的调用类似于

**(void) fseek (** _流_**，0 L，SEEK_SET);**

但是，与不同[fseek](fseek-fseeki64.md)， **rewind**清除流的错误指示符以及文件尾指示器。 此外，与不同[fseek](fseek-fseeki64.md)， **rewind**不返回一个值以指示是否已成功移动指针。

若要清除键盘缓冲区，使用**rewind**与流**stdin**，这是默认情况下与键盘关联。

如果流是**NULL**指针，无效参数处理程序调用中所述，[参数验证](../../c-runtime-library/parameter-validation.md)。 如果允许执行继续，则此函数将返回和**errno**设置为**EINVAL**。

有关这些代码及其他错误代码的信息，请参阅 [_doserrno、errno、_sys_errlist 和 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)。

## <a name="requirements"></a>要求

|例程|必需的标头|
|-------------|---------------------|
|**rewind**|\<stdio.h>|

有关其他兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="libraries"></a>库

[C 运行时库](../../c-runtime-library/crt-library-features.md)的所有版本。

## <a name="example"></a>示例

```C
// crt_rewind.c
/* This program first opens a file named
* crt_rewind.out for input and output and writes two
* integers to the file. Next, it uses rewind to
* reposition the file pointer to the beginning of
* the file and reads the data back in.
*/
#include <stdio.h>

int main( void )
{
   FILE *stream;
   int data1, data2;

   data1 = 1;
   data2 = -37;

   fopen_s( &stream, "crt_rewind.out", "w+" );
   if( stream != NULL )
   {
      fprintf( stream, "%d %d", data1, data2 );
      printf( "The values written are: %d and %d\n", data1, data2 );
      rewind( stream );
      fscanf_s( stream, "%d %d", &data1, &data2 );
      printf( "The values read are: %d and %d\n", data1, data2 );
      fclose( stream );
   }
}
```

### <a name="output"></a>输出

```Output
The values written are: 1 and -37
The values read are: 1 and -37
```

## <a name="see-also"></a>请参阅

[流 I/O](../../c-runtime-library/stream-i-o.md)<br/>
