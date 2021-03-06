---
title: "生成并运行的 c + + 控制台应用程序项目 |Microsoft 文档"
description: "生成并运行 Visual c + + 中的 Hello World 控制台应用程序"
ms.custom: mvc
ms.date: 12/12/2017
ms.topic: get-started-article
ms.technology:
- devlang-C++
ms.devlang: C++
dev_langs:
- C++
ms.assetid: 45138d71-719d-42dc-90d7-1d0ca31a2f55
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 119d39c6aac479c8e08cd017b4d5f8da794c836d
ms.sourcegitcommit: a5a69d2dc3513261e9e28320e4e067aaf40d2ef2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/21/2018
---
# <a name="build-and-run-a-c-console-app-project"></a>生成并运行的 c + + 控制台应用程序项目

时创建的 c + + 控制台应用程序项目并输入你的代码后，你可以生成和运行 Visual Studio 中，，然后从命令行运行作为一个独立应用。

## <a name="prerequisites"></a>系统必备

- 具有 c + + 工作负荷安装并在计算机上运行与桌面开发的 Visual Studio。 如果未尚未安装，请按照本文[Visual Studio 中的安装 c + + 支持](../build/vscpp-step-0-installation.md)。

- 创建一个"Hello，World ！" 项目，然后输入其源代码。 如果尚未执行此操作，请按照中的步骤[创建 c + + 控制台应用程序项目](../build/vscpp-step-1-create.md)。

Visual Studio 类似如下所示，如果你已准备好生成并运行你的应用程序：

   ![准备好生成新项目](../build/media/vscpp-ready-to-build.png "准备好生成新项目")

## <a name="build-and-run-your-code-in-visual-studio"></a>生成并运行 Visual Studio 中的代码

1. 若要生成项目时，选择**生成解决方案**从**生成**菜单。 **输出**窗口演示生成过程的结果。

   ![生成项目](../build/media/vscpp-build-solution.gif "生成项目")

1. 若要运行这些代码，在菜单栏上，选择**调试**，**启动而不调试**。

   ![启动项目](../build/media/vscpp-start-without-debugging.gif "启动项目")

    控制台窗口将打开并运行你的应用程序。 Visual Studio 中启动控制台应用程序时，它运行你的代码，然后打印"按任意键继续。 . ." 从而使你有机会以查看输出。

祝贺你！ 你已创建你的第一个"Hello，world ！" Visual Studio 中的控制台应用程序 ！ 按某个键，以关闭控制台窗口并返回到 Visual Studio。

[我遇到了问题。](#build-and-run-your-code-in-visual-studio-issues)

## <a name="run-your-code-in-a-command-window"></a>在命令窗口中运行你的代码

通常情况下，在命令提示符下，Visual Studio 中不运行控制台应用。 由 Visual Studio 生成你的应用程序后，你可以从任何命令窗口中运行它。 下面介绍了如何查找并在命令提示符窗口中运行新的应用程序。

1. 在**解决方案资源管理器**、 选择 HelloWorld 解决方案，然后右键单击以打开上下文菜单。 选择**在文件资源管理器中打开文件夹**以打开**文件资源管理器**HelloWorld 解决方案文件夹中的窗口。

1. 在**文件资源管理器**窗口中，打开的调试文件夹。 这包括你的应用程序、 HelloWorld.exe 和几个其他调试文件。 选择 HelloWorld.exe，请按住 Shift 键然后右键单击以打开上下文菜单。 选择**复制路径为**将路径复制到你的应用到剪贴板。

1. 若要打开命令提示符窗口，请按 Windows-R，打开**运行**对话框。 输入*cmd.exe*中**打开**文本框中，然后选择**确定**运行的命令提示符窗口。

1. 在命令提示符窗口中，右键单击要将你的应用程序的路径粘贴到命令提示符处。 按 enter 键以运行你的应用。

   ![在命令提示符下运行应用程序](../build/media/vscpp-run-in-cmd.gif "在命令提示符下运行应用程序")

祝贺你，你已生成，Visual Studio 中运行控制台应用程序 ！

[我遇到了问题。](#run-your-code-in-a-command-window-issues)

## <a name="next-steps"></a>后续步骤

一旦生成并运行此简单的应用程序后，你就准备好进行更复杂的项目。 请参阅[使用适用于 c + + 桌面开发的 Visual Studio IDE](../ide/using-the-visual-studio-ide-for-cpp-desktop-development.md)更多详细的演练，了解中的 Visual Studio 中的 Visual c + + 的功能。

## <a name="troubleshooting-guide"></a>故障排除指南

出于此处解决方案的常见问题时创建第一个 c + + 项目。

### <a name="build-and-run-your-code-in-visual-studio-issues"></a>生成并运行你的代码在 Visual Studio 的问题

如果红色波浪线显示在源代码编辑器中的任何内容，生成可能具有错误或警告。 检查你的代码匹配拼写、 标点符号和用例中的示例。

[回去。](#build-and-run-your-code-in-visual-studio)

### <a name="run-your-code-in-a-command-window-issues"></a>问题在命令窗口中运行你的代码

你还可以导航到通过在命令行运行你的应用的解决方案调试文件夹。 你无法从其他目录运行你的应用程序，而无需指定应用程序的路径。 但是，你可以将你的应用程序复制到另一个目录，并从该处运行它。

如果看不到**复制路径为**在快捷菜单中，取消菜单，然后按住 Shift 键，再次打开。 这是仅为方便起见。 此外可以从文件资源管理器搜索栏中，复制到的文件夹的路径，并将其粘贴到**运行**对话框中，然后输入结束时可执行文件的名称。 它是得更多键入，但它具有相同的结果。

[回去。](#run-your-code-in-a-command-window)


<iframe src="" height="0" width="0" frameborder="0" name="frameTarget" />
