---
title: 错误： 执行混合模式调试支持对 x64 进程是仅当使用 Microsoft.NET Framework 4 或更高版本 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.interop_unsupported_x64
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: e4b0216c-7006-4832-883f-08e982ba8d3f
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 82440d378e34c5808e9bcb250172f6c1abfbfdf6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49239234"
---
# <a name="error-mixed-mode-debugging-for-x64-processes-is-supported-only-when-using-microsoft-net-framework-4-or-greater"></a>错误：仅当使用 Microsoft .NET Framework 4 或更高版本时才支持对 x64 进程执行混合模式调试
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

若要调试 64 位进程中的混合本机代码和托管代码，你必须安装了 [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] 4 版。 低于 4 的 [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] 版本不支持对 64 位进程进行混合模式调试。  
  
### <a name="to-correct-this-error"></a>更正此错误  
  
-   执行以下步骤之一：  
  
    -   将 [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] 升级到 4 版。  
  
    -   生成 32 位版本的应用程序以进行调试。  
  
## <a name="see-also"></a>请参阅  
 [在设备上安装远程工具](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c)



