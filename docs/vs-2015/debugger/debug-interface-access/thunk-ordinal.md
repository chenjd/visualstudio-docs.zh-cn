---
title: THUNK_ORDINAL |Microsoft Docs
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
- C++
helpviewer_keywords:
- Thunk_Ordinal enumeration
ms.assetid: 026f98a9-36b8-41ef-8a72-12d7cbc2d362
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8152b22b229e654b17a2f424694283189c95431b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49834299"
---
# <a name="thunkordinal"></a>THUNK_ORDINAL
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

指定转换 （thunk） 类型。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
typedef enum THUNK_ORDINAL {   
   THUNK_ORDINAL_NOTYPE,  
   THUNK_ORDINAL_ADJUSTOR,  
   THUNK_ORDINAL_VCALL,  
   THUNK_ORDINAL_PCODE,  
   THUNK_ORDINAL_LOAD   
  
   // trampoline thunk ordinals - only for use in Trampoline thunk symbols  
   THUNK_ORDINAL_TRAMP_INCREMENTAL,  
   THUNK_ORDINAL_TRAMP_BRANCHISLAND,  
} THUNK_ORDINAL;  
```  
  
## <a name="elements"></a>元素  
 THUNK_ORDINAL_NOTYPE  
 标准转换 （thunk)。  
  
 THUNK_ORDINAL_ADJUSTOR  
 一个`this`精算师转换 （thunk)。  
  
 THUNK_ORDINAL_VCALL  
 虚调用 thunk。  
  
 THUNK_ORDINAL_PCODE  
 P 代码转换 （thunk)。  
  
 THUNK_ORDINAL_LOAD  
 延迟加载转换 （thunk)。  
  
 THUNK_ORDINAL_TRAMP_INCREMENTAL  
 增量 trampoline thunk （trampoline 转换 （thunk） 用于从一个内存空间之间反弹调用）。  
  
 THUNK_ORDINAL_TRAMP_BRANCHISLAND  
 分支点 trampoline 转换 （thunk)。  
  
## <a name="remarks"></a>备注  
 此枚举中的值返回到调用[idiasymbol:: Get_thunkordinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md)方法。  
  
## <a name="requirements"></a>要求  
 标头： cvconst.h  
  
## <a name="see-also"></a>请参阅  
 [枚举和结构](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaSymbol::get_thunkOrdinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md)



