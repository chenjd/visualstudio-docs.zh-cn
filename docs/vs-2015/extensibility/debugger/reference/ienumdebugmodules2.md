---
title: IEnumDebugModules2 |Microsoft Docs
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
- IEnumDebugModules2
helpviewer_keywords:
- IEnumDebugModules2
ms.assetid: 4fe28074-a960-41ad-b74d-b57f04c0c0ad
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8177463d1eabf222c34fefc09eb7115cd010e97f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49266729"
---
# <a name="ienumdebugmodules2"></a>IEnumDebugModules2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

此接口枚举的模块的列表。  
  
## <a name="syntax"></a>语法  
  
```  
IEnumDebugModules2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 调试引擎 (DE) 实现此接口来表示某个程序的加载模块的列表。  
  
## <a name="notes-for-callers"></a>调用方的说明  
 Visual Studio 调用[EnumModules](../../../extensibility/debugger/reference/idebugprogram2-enummodules.md)若要获取此接口。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 下表显示的方法`IEnumDebugModules2`。  
  
|方法|描述|  
|------------|-----------------|  
|[下一篇](../../../extensibility/debugger/reference/ienumdebugmodules2-next.md)|检索指定的枚举序列中的模块数。|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugmodules2-skip.md)|将跳过指定的数目的枚举序列中的模块。|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugmodules2-reset.md)|将枚举序列重置到开头。|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugmodules2-clone.md)|创建一个包含当前枚举数形式的相同枚举状态的枚举器。|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugmodules2-getcount.md)|获取模块的数。|  
  
## <a name="remarks"></a>备注  
 Visual Studio 将使用此接口主要用于更新**模块**窗口。  
  
 为了在 Visual Studio 中进行调试，程序是可以跨越模块边界，因此代码说明一个逻辑序列的单个模块的列表需要[IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)接口。 在列表中的第一个模块通常包含关联的程序的初始入口点。  
  
## <a name="requirements"></a>要求  
 标头： msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [EnumModules](../../../extensibility/debugger/reference/idebugprogram2-enummodules.md)

