---
title: Visual Studio 调试器可扩展性 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Visual Studio], Debugging SDK
- Debugging SDK
ms.assetid: c088b6a2-c3ad-446b-830d-9c6f41b2934b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: b0be4a96854315bcf8b83db86692758e198980cd
ms.sourcegitcommit: 3dd15e019cba7d35dbabc1aa3bf55842a59f5278
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2018
ms.locfileid: "46370921"
---
# <a name="visual-studio-debugger-extensibility"></a>Visual Studio 调试器可扩展性
Visual Studio 提供了完全交互式源代码调试器，跟踪的错误在程序中提供一个功能强大且易于使用的工具。 调试器具有全面的支持 Visual Basic、 C#、 C/c + + 和 JavaScript。 但是，对于[!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)]，即从可用[Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkId=214453)，可以使用相同的丰富功能在调试器中支持其他编程语言。  
  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]调试器是常见的前端 （即，用户界面），接下来，特定于正在调试的语言的调试组件。 对于新语言，所有所需的支持通过[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]调试器将创建必要的后端组件，如调试引擎 (DE)。 这一点是 where[!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)]传入。  
  
 [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)]包括所有的完整参考资料[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]创建新部署所需的元素。 此外，还有示例和教程，可帮助您入门。  
  
 具有调试支持的语言项目系统的完整示例，请参阅[IronPython 示例](https://www.microsoft.com/download/details.aspx?id=55984)。  
  
 以下部分介绍如何使用扩展调试器[!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)]。  
  
## <a name="in-this-section"></a>本节内容  
 [入门](../../extensibility/debugger/getting-started-with-debugger-extensibility.md)  
 描述什么[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]调试产品/服务和如何安装 SDK。  
  
 [创建自定义调试引擎](../../extensibility/debugger/creating-a-custom-debug-engine.md)  
 记录 DE 自定义过程中，从为到分离 DE DE 准备您的程序。  
  
 [编写 CLR 表达式计算器](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)  
 说明是否必须编写的表达式计算器。  
  
 [选择调试引擎实施策略](../../extensibility/debugger/choosing-a-debug-engine-implementation-strategy.md)  
 讨论如何实现您 DE。  
  
 [参考](../../extensibility/debugger/reference/reference-visual-studio-debugging-apis.md)  
 文档[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]调试 API。  
  
 [示例](../../extensibility/debugger/visual-studio-debugging-samples.md)  
 包含公共语言运行时表达式计算器示例和调试引擎示例的链接。
