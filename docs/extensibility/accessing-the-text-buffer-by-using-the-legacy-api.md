---
title: 使用旧版 API 访问的文本缓冲区 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - text buffers
ms.assetid: cd6cf4ae-fff5-4e23-b293-7cbafdb8aed2
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3347fc2fd03a2eb6b466145672d3aebb77ad71a6
ms.sourcegitcommit: 8ee7efb70a1bfebcb6dd9855b926a4ff043ecf35
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2018
ms.locfileid: "39078009"
---
# <a name="access-the-text-buffer-by-using-the-legacy-api"></a>通过使用传统的 API 访问的文本缓冲区
文本是负责管理文本流和文件暂留。 尽管缓冲区可以读取或写入其他格式与缓冲区的所有普通通信执行通过使用 Unicode。 在传统的 Api 中的文本缓冲区可以使用一个-或二维坐标系统以确定在缓冲区中的字符位置。  
  
## <a name="one--and-two-dimension-coordinate-systems"></a>一个和两个维度协调系统  
 一维的坐标位置开始算起的第一个字符的缓冲区，例如 147 中的某个字符的位置。 您使用<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream>界面来访问缓冲区中的一维位置。 二维坐标系统基于行和索引对。 例如，43 缓冲区中的字符，5 将在第 43 行，该行中的第一个字符右侧的五个字符。 访问在缓冲区中使用的二维位置<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>接口。 同时<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>并<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream>接口的实现文本缓冲区对象 (<xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>)，并且可以通过使用从相互访问`QueryInterface`。 下图显示了这些和其他关键接口上<xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>。  
  
 ![文本缓冲区对象](../extensibility/media/vstextbuffer.gif "vsTextBuffer")  
文本缓冲区对象  
  
 尽管任一坐标系统中的文本缓冲区工作原理，但它经过优化，可使用二维坐标。 一维的坐标系统可以创建性能开销。 因此，使用尽可能对二维坐标系统。  
  
 文本缓冲区的第二项责任是文件暂留。 若要执行此操作，该文本缓冲区对象实现<xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2>并且可作为项目项的文档数据对象组件和参与持久性的其他环境组件。 有关详细信息，请参阅[打开和保存项目项](../extensibility/internals/opening-and-saving-project-items.md)。  
  
## <a name="in-this-section"></a>本节内容  
 [通过使用传统的 API 更改视图设置](../extensibility/changing-view-settings-by-using-the-legacy-api.md)  
 说明如何更改视图设置，请使用传统的 API。  
  
 [使用文本管理器来监视全局设置](../extensibility/using-the-text-manager-to-monitor-global-settings.md)  
 介绍如何使用文本管理器来监视全局设置。  
  
## <a name="see-also"></a>请参阅  
 [在核心编辑器](../extensibility/inside-the-core-editor.md)