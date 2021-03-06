---
title: 'Idiaaddressmap:: Put_imagealign |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::put_imageAlign method
ms.assetid: f9ce875d-c263-43e5-a534-f34c37f9866f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 06110568e0854692b19c3c118e948024bd346295
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49903993"
---
# <a name="idiaaddressmapputimagealign"></a>IDiaAddressMap::put_imageAlign
设置的图像对齐方式。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT put_imageAlign (   
   DWORD NewVal  
);  
```  
  
#### <a name="parameters"></a>参数  
 NewVal  
 [in]新的图像对齐方式可执行文件有值。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 指定的内存边界对齐图像 （加载可执行文件）。 由当前的系统体系结构以及编译和链接时间选项，可能会影响此对齐方式。 图像对齐方式是始终在字节边界上。 下面的图像对齐方式列出有效值： 1、 2、 4、 8、 16、 32 和 64 字节边界。  
  
 可以通过调用检索当前的图像对齐方式[idiaaddressmap:: Get_imagealign](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md)方法。  
  
> [!NOTE]
>  可以调用此方法时已加载图像。 `put_imageAlign`图像已被移动或更改和新的对齐方式是所需时通常使用方法。  
  
## <a name="see-also"></a>请参阅  
 [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [IDiaAddressMap::get_imageAlign](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md)