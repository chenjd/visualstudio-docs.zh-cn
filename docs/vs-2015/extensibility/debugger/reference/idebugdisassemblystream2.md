---
title: IDebugDisassemblyStream2 |Microsoft Docs
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
- IDebugDisassemblyStream2
helpviewer_keywords:
- IDebugDisassemblyStream2 interface
ms.assetid: b03cab0c-3f0b-4cc6-88dc-acb3b48c567a
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 81210da4d743daac980a363e817b05fe8e3a11f3
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49286814"
---
# <a name="idebugdisassemblystream2"></a>IDebugDisassemblyStream2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

此接口表示指令流。  
  
## <a name="syntax"></a>语法  
  
```  
IDebugDisassemblyStream2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 调试引擎实现此接口以支持反汇编程序的代码。  
  
## <a name="notes-for-callers"></a>调用方的说明  
 调用[GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)方法返回此接口。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 下表显示的方法`IDebugDisassemblyStream2`。  
  
|方法|描述|  
|------------|-----------------|  
|[Read](../../../extensibility/debugger/reference/idebugdisassemblystream2-read.md)|读取从当前位置反汇编流中的说明。|  
|[Seek](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)|将读取的指针移动反汇编流给定数量的相对于指定位置的说明中。|  
|[GetCodeLocationId](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodelocationid.md)|返回特定代码上下文的代码位置标识符。|  
|[GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md)|返回与指定的代码位置标识符相对应的代码上下文对象。|  
|[GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md)|返回表示当前的代码位置的代码位置标识符。|  
|[GetDocument](../../../extensibility/debugger/reference/idebugdisassemblystream2-getdocument.md)|获取与此反汇编流关联的源文档。|  
|[GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md)|获取此反汇编流的范围。|  
|[GetSize](../../../extensibility/debugger/reference/idebugdisassemblystream2-getsize.md)|获取此反汇编流的大小。|  
  
## <a name="remarks"></a>备注  
 可以创建反汇编流来表示整个地址空间或只是函数或模块的空间中。 每个指令都由[DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)由调用返回结构[读取](../../../extensibility/debugger/reference/idebugdisassemblystream2-read.md)方法。  
  
## <a name="requirements"></a>要求  
 标头： msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)   
 [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)

