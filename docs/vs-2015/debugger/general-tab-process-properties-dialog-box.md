---
title: 常规选项卡上，处理属性对话框 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: 86f4d61d-a594-4aac-8960-c5279b4a10fd
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1acc3826521ca6bd15b60563f9bd5e99ba70988e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49282069"
---
# <a name="general-tab-process-properties-dialog-box"></a>“进程属性”对话框 ->“常规”选项卡
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

使用**常规**选项卡以找出特定过程的详细信息。 若要显示[进程属性对话框](../debugger/process-properties-dialog-box.md)，将焦点移至[进程视图](../debugger/processes-view.md)窗口。 在树中，选择任何进程节点，然后选择**属性**从**视图**菜单。  
  
 以下设置位于**常规**选项卡：  
  
|条目|描述|  
|-----------|-----------------|  
|**模块名**|模块的名称。|  
|**进程 ID**|此进程的唯一 ID。 进程 ID 号可以重新使用，所以它们仅为该进程的生存期标识的进程。 运行程序时创建的进程对象类型。 在进程中的所有线程共享相同的地址空间，并有权访问相同的数据。|  
|**优先级基数**|此进程的当前基优先级。 进程中的线程可以通过提高和降低其自身相对于该进程的基本优先级的基本优先级。|  
|**线程**|在此过程中当前处于活动状态的线程数。|  
|**CPU 时间**|在此过程，并且其线程上花费的总 CPU 时间。 用户以及特权的时间等于。|  
|**用户时间**|累计的已用时间此进程的线程所用在非空闲线程在用户模式下执行代码。 子系统，如窗口管理器和图形引擎一样，应用程序以用户模式下执行。|  
|**特权的时间**|总运行时间此进程已运行在特权模式下在非空闲线程中。 服务层、 高级管理人员例程和内核在特权模式下中执行。 图形适配器和打印机以外的大多数设备的设备驱动程序还在特权模式下执行。 Windows 为您的应用程序执行一些操作可能出现在 Privileged Time 除了其他子系统进程。|  
|**已用时间**|此进程已运行总运行时间。|



