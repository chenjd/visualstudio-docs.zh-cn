---
title: dwTYPE_KIND |Microsoft Docs
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
- dwTYPE_KIND
helpviewer_keywords:
- dwTYPE_KIND enumeration
ms.assetid: 6ff56b0f-c502-4e6c-9829-bfa05361b783
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: adfbd4ce924acb7ef6cd3f22a1a7d4bf5de27683
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49933971"
---
# <a name="dwtypekind"></a>dwTYPE_KIND
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

指定如何解释的类型[IDebugField](../../../extensibility/debugger/reference/idebugfield.md)对象。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
  
typedef DWORD dwTYPE_KIND;  
```  
  
```csharp  
public enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
```  
  
#### <a name="parameters"></a>参数  
 TYPE_KIND_METADATA  
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)并集应被视为[METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)结构。  
  
 TYPE_KIND_PDB  
 `TYPE_INFO`并集应被视为[PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)结构。  
  
 TYPE_KIND_BUILT  
 `TYPE_INFO`并集应被视为[BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)结构。  
  
## <a name="remarks"></a>备注  
 此枚举的值中出现`dwKind`字段[TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)结构，用于确定如何解释`type`联合成员。 `TYPE_INFO`结构返回通过调用[GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md)方法。  
  
## <a name="requirements"></a>要求  
 标头： sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [枚举](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)   
 [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md)   
 [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)   
 [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)   
 [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)

