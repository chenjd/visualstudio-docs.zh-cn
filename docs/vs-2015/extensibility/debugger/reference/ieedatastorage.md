---
title: IEEDataStorage |Microsoft Docs
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
- IEEDataStorage
helpviewer_keywords:
- IEEDataStorage interface
ms.assetid: 704e932d-2325-410e-89c4-ce88c6ec19da
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 71c41f540be12552c82d714f4c2d388f47539601
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49207982"
---
# <a name="ieedatastorage"></a>IEEDataStorage
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

此接口表示一个字节数组。  
  
## <a name="syntax"></a>语法  
  
```  
IEEDataStorage : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 表达式计算器 (EE) 实现此接口来表示一个字节数组 (由类型可视化工具，用于检索和更改数据通过[IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)接口)。 EE 通常实现此接口以支持外部类型可视化工具。  
  
## <a name="notes-for-callers"></a>调用方的说明  
 上的方法`IPropertyProxyEESide`所有接口都返回此接口。 调用[GetPropertyProxy](../../../extensibility/debugger/reference/ipropertyproxyprovider-getpropertyproxy.md)来获取[IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)接口。 调用[QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3)上[IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)接口，以获得[IPropertyProxyProvider](../../../extensibility/debugger/reference/ipropertyproxyprovider.md)接口。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 `IEEDataStorage`接口实现以下方法：  
  
|方法|描述|  
|------------|-----------------|  
|[GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md)|检索指定的数量的数据字节复制到提供的缓冲区。|  
|[GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md)|检索可用的数据字节数。|  
  
## <a name="remarks"></a>备注  
 类型可视化工具使用此接口访问特定对象持有的数据。 将数据视为数组字节，可让类型可视化工具，用于在需要向用户显示的任何方式对其进行操作。  
  
 自定义查看器还可以使用此接口，如果需要，更常见的做法，自定义查看器将使用自定义接口，尽管[GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md)或[GetStringChars](../../../extensibility/debugger/reference/idebugproperty3-getstringchars.md) （适用于面向字符串的数据）。  
  
## <a name="requirements"></a>要求  
 标头： msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [类型可视化工具和自定义查看器](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)

