---
title: "-Ob （内联函数展开） |Microsoft 文档"
ms.custom: 
ms.date: 09/25/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- VC.Project.VCCLWCECompilerTool.InlineFunctionExpansion
- VC.Project.VCCLCompilerTool.InlineFunctionExpansion
- /ob
dev_langs:
- C++
helpviewer_keywords:
- inline functions, function expansion compiler option [C++]
- -Ob1 compiler option [C++]
- -Ob0 compiler option [C++]
- /Ob0 compiler option [C++]
- /Ob1 compiler option [C++]
- any suitable compiler option [C++]
- Ob2 compiler option [C++]
- Ob1 compiler option [C++]
- /Ob2 compiler option [C++]
- Ob compiler option [C++]
- -Ob2 compiler option [C++]
- disable compiler option [C++]
- -Ob compiler option [C++]
- /Ob compiler option [C++]
- only __inline compiler option [C++]
- Ob0 compiler option [C++]
- inline expansion, compiler option
ms.assetid: f134e6df-e939-4980-a01d-47425dbc562a
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: b83d470eaf6a30698d8c2836620a0688daa35cc1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="ob-inline-function-expansion"></a>/Ob（内联函数展开）

控制函数的内联扩展。

## <a name="syntax"></a>语法

> /Ob {0 | 1 | 2}

## <a name="arguments"></a>自变量

**0**  
禁用内联扩展。 默认情况下，编译器自行对所有函数进行展开通常称为*自动内联*。

**1**  
允许的标记的函数仅扩展[内联](../../cpp/inline-functions-cpp.md)， `__inline`，或`__forceinline`，或在类声明中定义的 c + + 成员函数。

**2**  
默认值。 允许对标记为 `inline`、`__inline` 或 `__forceinline` 的函数或是编译器选择的任何其他函数进行扩展。

**/Ob2**有效时[/O1、 /O2 （最小化大小、 最大化速度）](../../build/reference/o1-o2-minimize-size-maximize-speed.md)或[/Ox （启用最速度优化）](../../build/reference/ox-full-optimization.md)使用。

此选项要求你启用优化使用**/O1**， **/O2**， **/Ox**，或**/Og**。  

## <a name="remarks"></a>备注

编译器将内联扩展选项和关键字视为建议。 并不保证任何函数都会进行内联扩展。 可以禁用内联扩展，但即使在使用 `__forceinline` 关键字时，也无法强制编译器对特定函数进行内联。

你可以使用`#pragma` [auto_inline](../../preprocessor/auto-inline.md)指令排除考虑的候选项为内联展开的函数。 另请参阅`#pragma`[内部](../../preprocessor/intrinsic.md)指令。

> [!NOTE]
> 通过分析测试运行收集的信息替代本可以生效如果指定的优化**/Ob**， **/Os**，或**/Ot**。 有关详细信息，请参阅[按配置文件优化](../../build/reference/profile-guided-optimizations.md)。

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>在 Visual Studio 开发环境中设置此编译器选项

1. 打开项目的“属性页”  对话框。 有关详细信息，请参阅[使用项目属性](../../ide/working-with-project-properties.md)。

1. 展开**配置属性**， **C/c + +**，然后选择**优化**。

1. 修改**内联函数扩展**属性。

### <a name="to-set-this-compiler-option-programmatically"></a>以编程方式设置此编译器选项

- 请参阅 <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.InlineFunctionExpansion%2A>。

## <a name="see-also"></a>请参阅

[/O 选项 （优化代码）](../../build/reference/o-options-optimize-code.md)  
[编译器选项](../../build/reference/compiler-options.md)  
[设置编译器选项](../../build/reference/setting-compiler-options.md)