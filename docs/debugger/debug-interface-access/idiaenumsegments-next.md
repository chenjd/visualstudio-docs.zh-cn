---
title: 'Idiaenumsegments:: Next |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSegments::Next method
ms.assetid: 53f61874-d821-47ab-a1f5-27e982804a6a
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7c9966555c673904a423de1b215e438b5db15479
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49951023"
---
# <a name="idiaenumsegmentsnext"></a>IDiaEnumSegments::Next
检索指定的数目的枚举序列中的段。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT Next (   
   ULONG         celt,   
   IDiaSegment** rgelt,  
   ULONG*        pceltFetched  
);  
```  
  
#### <a name="parameters"></a>参数  
 celt  
 [in]要检索的枚举器中的段的数目。  
  
 rgelt  
 [out]数组，它是要填充与所需[IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)表示段的对象。  
  
 pceltFetched  
 [out]返回在提取枚举器中的段数。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`。 返回`S_FALSE`如果没有更多的段。 否则，返回错误代码。  
  
## <a name="see-also"></a>请参阅  
 [IDiaEnumSegments](../../debugger/debug-interface-access/idiaenumsegments.md)   
 [IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)