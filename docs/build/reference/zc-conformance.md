---
title: "/Zc （一致性） |Microsoft 文档"
ms.custom: 
ms.date: 03/06/2018
ms.technology:
- cpp-tools
ms.topic: article
f1_keywords:
- /zc
dev_langs:
- C++
helpviewer_keywords:
- /Zc compiler options [C++]
- -Zc compiler options [C++]
- Conformance compiler options
- Zc compiler options [C++]
ms.assetid: db1cc175-6e93-4a2e-9396-c3725d2d8f71
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: dda62dc6644fd49cf9213b176a4efe563474f740
ms.sourcegitcommit: eeb2b5ad8d3d22514a7b9bd7d756511b69ae0ccf
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/15/2018
---
# <a name="zc-conformance"></a>/Zc（一致性）

你可以使用**/Zc**编译器选项来指定标准或特定于 Microsoft 的编译器行为。

## <a name="syntax"></a>语法

> **/Zc:**_option_{,_option_}

## <a name="remarks"></a>备注

在 Visual Studio 已实现 C 或不符合标准的 c + + 的扩展，你可以使用`/Zc`一致性选项以指定符合标准的或特定于 Microsoft 的行为。 对于某些选项的特定于 Microsoft 的行为是默认设置，以防止对现有代码的大规模的重大更改。 在其他情况下，默认为标准的行为，其中在安全性、 性能或兼容性方面的改进带来重大更改的成本。 较新版本的 Visual Studio 可能会改变每个一致性选项的默认设置。 有关每个一致性选项的详细信息，请参阅特定选项的主题。 [/ 宽松-](permissive-standards-conformance.md)编译器选项隐式设置未设置默认情况下，为其符合的设置的一致性选项。

这些是`/Zc`编译器选项：

|选项|行为|
|---|---|
|[alignedNew\[-\]](zc-alignednew.md)|启用 C + + 17 过度对齐动态分配 （在默认在 C + + 17）。|
|[auto\[-\]](zc-auto-deduce-variable-type.md)|强制执行用于新的标准 c + + 意义`auto`(在默认情况下)。|
|[externConstexpr\[-\]](zc-externconstexpr.md)|启用为外部链接`constexpr`变量 （默认情况下关闭）。|
|[forScope\[-\]](zc-forscope-force-conformance-in-for-loop-scope.md)|强制执行标准 c + +`for`作用域规则 (在默认情况下)。|
|[implicitNoexcept\[-\]](zc-implicitnoexcept-implicit-exception-specifiers.md)|启用隐式`noexcept`上所需的功能 (在默认情况下)。|
|[inline\[-\]](zc-inline-remove-unreferenced-comdat.md)|如果它为 COMDAT 或具有内部链接仅删除未引用的函数或数据 （默认情况下关闭）。|
|[noexceptTypes\[-\]](zc-noexcepttypes.md)|强制执行 C + + 17 noexcept 规则 (在默认情况下，C + + 17 中或更高版本)。|
|[referenceBinding\[-\]](zc-referencebinding-enforce-reference-binding-rules.md)|UDT 临时将不会绑定到非 const 左值引用 （默认情况下关闭）。|
|[rvalueCast\[-\]](zc-rvaluecast-enforce-type-conversion-rules.md)|强制执行标准 c + + 显式类型转换规则 （默认情况下关闭）。|
|[sizedDealloc\[-\]](zc-sizeddealloc-enable-global-sized-dealloc-functions.md)|启用 C + + 14 调整了大小的释放全局函数 (在默认情况下)。|
|[strictStrings\[-\]](zc-strictstrings-disable-string-literal-type-conversion.md)|禁用字符串文本到`char*`或`wchar_t*`转换 （默认情况下关闭）。|
|[ternary\[-\]](zc-ternary.md)|强制实施条件运算符对操作数类型的规则 （默认情况下关闭）。|
|[threadSafeInit\[-\]](zc-threadsafeinit-thread-safe-local-static-initialization.md)|启用线程安全的本地静态初始化 (在默认情况下)。|
|[throwingNew\[-\]](zc-throwingnew-assume-operator-new-throws.md)|假定`operator new`失败时引发 （默认情况下关闭）。|
|[trigraphs\[-\]](zc-trigraphs-trigraphs-substitution.md)|启用三元组 （已过时，关闭默认情况下）。|
|[twoPhase-](zc-twophase.md)|使用分析 （默认情况下一致性） 的行为的不符合要求的模板。|
|[wchar_t\[-\]](zc-wchar-t-wchar-t-is-native-type.md)|`wchar_t` 是本机类型，不的 typedef (在默认情况下)。|

有关 Visual C++ 中一致性问题的详细信息，请参阅 [Nonstandard Behavior](../../cpp/nonstandard-behavior.md)。

## <a name="see-also"></a>请参阅

[编译器选项](compiler-options.md)  
[设置编译器选项](setting-compiler-options.md)
