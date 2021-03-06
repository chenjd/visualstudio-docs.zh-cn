---
title: IDebugExpression2 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugExpression2
helpviewer_keywords:
- IDebugExpression2 interface
ms.assetid: f5e4b124-1e30-47c8-a511-80084a02dba5
caps.latest.revision: 15
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3db1107ced3601f32ea06857386220b282e6af3c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49217023"
---
# <a name="idebugexpression2"></a>IDebugExpression2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

此接口表示分析的表达式可供绑定和评估。  
  
## <a name="syntax"></a>语法  
  
```  
IDebugExpression2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 调试引擎 (DE) 实现此接口来表示可供计算的已分析的表达式。  
  
## <a name="notes-for-callers"></a>调用方的说明  
 调用[ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md)返回此接口。 [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md)将返回[IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md)接口。 仅当已暂停正在调试的程序和堆栈帧是可用时，这些接口进行访问。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 下表显示的方法`IDebugExpression2`。  
  
|方法|描述|  
|------------|-----------------|  
|[EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)|以异步方式计算此表达式的值。|  
|[Abort](../../../extensibility/debugger/reference/idebugexpression2-abort.md)|结束异步表达式求值。|  
|[EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)|以同步方式计算此表达式的值。|  
  
## <a name="remarks"></a>备注  
 会话调试管理器 (SDM) 时已停止程序，从通过调用 DE 获取堆栈帧[EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)。 然后调用 SDM [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md)若要获取[IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md)接口。 随后调用[ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md)若要创建`IDebugExpression2`接口，它表示分析可供计算的表达式。  
  
 SDM 拨打[EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)或[EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)进行实际计算表达式并生成值。  
  
 实现中`IDebugExpressionContext2::ParseText`，DE 使用 COM 的`CoCreateInstance`函数来实例化的表达式计算器，并获取[IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)接口 (请参阅中的示例`IDebugExpressionEvaluator`接口)。 然后调用 DE[分析](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md)来获取[IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)接口。 实现中使用此接口`IDebugExpression2::EvaluateSync`和`IDebugExpression2::EvaluateAsync`执行计算。  
  
## <a name="requirements"></a>要求  
 标头： msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetExpression](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getexpression.md)

