---
title: IDebugPortEvents2 |Microsoft Docs
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
- IDebugPortEvents2
helpviewer_keywords:
- IDebugPortEvents2 interface
ms.assetid: 2c017094-3ba2-4067-83f9-147df1d96bce
caps.latest.revision: 19
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1e0d5a55dd6e6f7b227477b20af4718001ab5a70
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49178901"
---
# <a name="idebugportevents2"></a>IDebugPortEvents2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

此接口通知的过程和程序创建和析构的特定端口上的侦听器 （通常会话调试管理器 [SDM] 或调试引擎）。 此信息可以用于显示进程和端口上运行的程序的实时视图。  
  
## <a name="syntax"></a>语法  
  
```  
IDebugPortEvents2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 Visual Studio 通常实现此接口以接收有关程序创建和析构的通知。 调试引擎还可以实现此接口可侦听对此类端口事件。  
  
## <a name="notes-for-callers"></a>调用方的说明  
 所有[IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)接口可以查询有关<xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer>接口。 然后<xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer.FindConnectionPoint%2A>方法`IDebugPortEvents2`中称为<xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer>接口，用于获取<xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint>接口。 最后，<xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint.Advise%2A>中的方法<xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint>接口调用以通过将事件发送[事件](../../../extensibility/debugger/reference/idebugportevents2-event.md)方法。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 下表显示的方法`IDebugPortEvents2`。  
  
|方法|描述|  
|------------|-----------------|  
|[Event](../../../extensibility/debugger/reference/idebugportevents2-event.md)|将发送描述的创建和析构的流程和端口上的计划事件。|  
  
## <a name="remarks"></a>备注  
 `IDebugPortEvents2` 此外可供 SDM 来调试正在调试的进程中运行的程序。  
  
 此接口传递给 SDM 端口事件。  
  
## <a name="requirements"></a>要求  
 标头： msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)

