---
title: 'Idiasymbol:: Get_language |Microsoft Docs'
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
- IDiaSymbol::get_language method
ms.assetid: c759ad3c-1c21-4234-869b-86aa3a608a38
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d13d11b56359051b2c1b6c824d058345d3517d20
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49898741"
---
# <a name="idiasymbolgetlanguage"></a>IDiaSymbol::get_language
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

检索源的语言。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT get_language (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pRetVal`  
 [out]返回一个值从[CV_CFL_LANG 枚举](../../debugger/debug-interface-access/cv-cfl-lang.md)枚举，用于指定源的语言。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回`S_FALSE`或错误代码。  
  
> [!NOTE]
>  返回值为`S_FALSE`表示该属性不是可用于符号。  
  
## <a name="see-also"></a>请参阅  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [CV_CFL_LANG 枚举](../../debugger/debug-interface-access/cv-cfl-lang.md)



