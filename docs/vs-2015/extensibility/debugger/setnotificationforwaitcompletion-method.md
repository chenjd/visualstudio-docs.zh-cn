---
title: SetNotificationForWaitCompletion 方法 |Microsoft Docs
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
- SetNotificationForWaitCompletion method, Task class [.NET Framework debug engines]
ms.assetid: da149c9a-20f4-4543-a29e-429c8c1d2e19
caps.latest.revision: 6
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5654814931904c157f8970ee0a1046820f3be132
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49173363"
---
# <a name="setnotificationforwaitcompletion-method"></a>SetNotificationForWaitCompletion 方法
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

设置或清除 TASK_STATE_WAIT_COMPLETION_NOTIFICATION 状态位。  
  
 **Namespace**：<xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **程序集：** mscorlib （在 mscorlib.dll 中)  
  
## <a name="syntax"></a>语法  
  
```vb  
internal void SetNotificationForWaitCompletion(bool enabled)  
```  
  
#### <a name="parameters"></a>参数  
 `enabled`  
  
 `true` 若要设置的位;`false`取消设置了位。  
  
## <a name="exceptions"></a>异常  
  
## <a name="remarks"></a>备注  
 调试器设置此位，以帮助脱离异步方法正文。 如果`enabled`是`true`，必须仅在尚未完成的任务上调用此方法。 如果`enabled`是`false`，不能对已完成的任务调用此方法。 在既情况下，它应仅用于承诺样式任务。  
  
## <a name="requirements"></a>要求  
  
## <a name="see-also"></a>请参阅  
 [Task 类](../../extensibility/debugger/task-class-internal-members.md)

