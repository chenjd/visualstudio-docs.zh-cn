---
title: 演练： 在设计时调试 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging [Visual Studio], design-time
- breakpoints, design-time debugging
- Immediate window, design-time debugging
- design-time debugging
ms.assetid: 35bfdd2c-6f60-4be1-ba9d-55fce70ee4d8
caps.latest.revision: 23
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a4ff1d0e1c155784bd6116be2bc6eb63e6c53d80
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49227223"
---
# <a name="walkthrough-debugging-at-design-time"></a>演练：在设计时调试
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

可以使用 Visual Studio**即时**窗口在你的应用程序未运行时执行函数或子例程。 如果函数或子例程包含断点，Visual Studio 将在相应的点中断执行。 随后即可使用调试器窗口检查程序状态。 此功能称为在设计时调试。  
  
 下面的过程演示如何使用此功能。  
  
### <a name="to-hit-breakpoints-from-the-immediate-window"></a>以命中断点，从即时窗口  
  
1.  将以下代码粘贴到 Visual Basic 控制台应用程序：  
  
    ```  
    Module Module1  
  
        Sub Main()  
            MySub()  
        End Sub  
  
        Function MyFunction() As Decimal  
            Static i As Integer  
            i = i + 1  
            Dim s As String  
  
            s = "Add Breakpoint here"  
            Return 4  
        End Function  
  
        Sub MySub()  
            MyFunction()  
        End Sub  
    End Module  
    ```  
  
2.  在读取时，在行上设置断点`s="Add BreakPoint Here"`。  
  
3.  键入以下内容中的**即时**窗口： `?MyFunction<enter>`  
  
4.  验证命中断点和调用堆栈准确。  
  
5.  上**调试**菜单上，单击**继续**，并验证是否仍处于设计模式。  
  
6.  键入以下内容中的**即时**窗口： `?MyFunction<enter>`  
  
7.  键入以下内容中的**即时**窗口： `?MySub<enter>`  
  
8.  验证是否命中了断点，并检查静态变量的值`i`中**局部变量**窗口。 它应具有的值为 3。  
  
9. 验证调用堆栈准确。  
  
10. 上**调试**菜单上，单击**继续**，并验证是否仍处于设计模式。  
  
## <a name="see-also"></a>请参阅  
 [调试器安全](../debugger/debugger-security.md)   
 [调试器基础知识](../debugger/debugger-basics.md)



