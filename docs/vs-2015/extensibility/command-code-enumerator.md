---
title: 命令代码枚举器 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- command code enumerator
- source control plug-ins, command code enumeration
ms.assetid: 5d2c360c-59e4-4da8-bcb4-dd07c7441e40
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0f3e2578a20319e88f048ed0c8ffded5589b286d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49851985"
---
# <a name="command-code-enumerator"></a>命令代码枚举器
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

此枚举器使用的选项中[SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)并[SccPopulateList](../extensibility/sccpopulatelist-function.md)以指示为其指定的选项的命令。  
  
## <a name="syntax"></a>语法  
  
```  
enum SCCCOMMAND {  
   SCC_COMMAND_GET,  
   SCC_COMMAND_CHECKOUT,  
   SCC_COMMAND_CHECKIN,  
   SCC_COMMAND_UNCHECKOUT,  
   SCC_COMMAND_ADD,  
   SCC_COMMAND_REMOVE,  
   SCC_COMMAND_DIFF,  
   SCC_COMMAND_HISTORY,  
   SCC_COMMAND_RENAME,  
   SCC_COMMAND_PROPERTIES,  
   SCC_COMMAND_OPTIONS  
};  
```  
  
## <a name="members"></a>成员  
 SCC_COMMAND_GET  
 对应于[SccGet](../extensibility/sccget-function.md)。  
  
 SCC_COMMAND_CHECKOUT  
 对应于[SccCheckout](../extensibility/scccheckout-function.md)。  
  
 SCC_COMMAND_CHECKIN  
 对应于[SccCheckin](../extensibility/scccheckin-function.md)。  
  
 SCC_COMMAND_UNCHECKOUT  
 对应于[SccUncheckout](../extensibility/sccuncheckout-function.md)。  
  
 SCC_COMMAND_ADD  
 对应于[SccAdd](../extensibility/sccadd-function.md)。  
  
 SCC_COMMAND_REMOVE  
 对应于[SccRemove](../extensibility/sccremove-function.md)。  
  
 SCC_COMMAND_DIFF  
 对应于[SccDiff](../extensibility/sccdiff-function.md)。  
  
 SCC_COMMAND_HISTORY  
 对应于[SccHistory](../extensibility/scchistory-function.md)。  
  
 SCC_COMMAND_RENAME  
 对应于[SccRename](../extensibility/sccrename-function.md)。  
  
 SCC_COMMAND_PROPERTIES  
 对应于[SccProperties](../extensibility/sccproperties-function.md)。  
  
 SCC_COMMAND_OPTIONS  
 对应于[SccSetOption](../extensibility/sccsetoption-function.md)。  
  
## <a name="see-also"></a>请参阅  
 [源代码管理插件](../extensibility/source-control-plug-ins.md)   
 [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)   
 [SccPopulateList](../extensibility/sccpopulatelist-function.md)

