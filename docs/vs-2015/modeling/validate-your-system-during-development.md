---
title: 在开发过程中验证您的系统 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-techdebt
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- layer diagrams
ms.assetid: c9dafb47-7b1d-4c72-9432-d43be3db1799
caps.latest.revision: 39
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: 33d5de340455e5e0f6a39dd9ce470d2e96327216
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49262179"
---
# <a name="validate-your-system-during-development"></a>在开发过程中验证系统
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio 可帮助使你的软件与用户的要求和系统的体系结构保持一致。  
  
 若要查看支持各个功能的 Visual Studio 版本，请参阅 [Version support for architecture and modeling tools](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport)。  
  
## <a name="key-tasks"></a>关键任务  
 使用以下任务来验证软件。  
  
|**任务**|**相关主题**|  
|---------------|---------------------------|  
|**请确保你的模型是一致：**<br /><br /> 由于项目使用和解释模型方式会有所不同，因此禁用某些元素组合可能会有所帮助。 例如，可以限制 UML 类，以使它们始终具有符合 [!INCLUDE[TLA2#tla_net](../includes/tla2sharptla-net-md.md)] 的名称。 你可以以这些方式在 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 扩展中定义约束。|-   [验证 UML 模型](../modeling/validate-your-uml-model.md)<br />-   [为 UML 模型定义验证约束](../modeling/define-validation-constraints-for-uml-models.md)|  
|**请确保软件满足用户要求**：<br /><br /> 可以使用要求模型和体系结构模型来帮助组织系统及其组件的测试。 这种做法有助于确保你测试了对于用户和其他利益干系人而言非常重要的要求，并可帮助你在要求发生变化时快速更新测试。|-   [基于模型开发测试](../modeling/develop-tests-from-a-model.md)|  
|**请确保你的软件与系统的预期设计保持一致：**<br /><br /> 层关系图描述了应用程序组件之间的预期依赖关系。 在开发期间，你可以验证代码中的实际依赖关系是否符合预期设计。|-   [从代码创建层关系图](../modeling/create-layer-diagrams-from-your-code.md)<br />-   [使用层关系图验证代码](../modeling/validate-code-with-layer-diagrams.md)|  
  
## <a name="external-resources"></a>外部资源  
  
|**类别**|**链接**|  
|------------------|---------------|  
|**视频**|![视频链接](../data-tools/media/playvideo.gif "播放视频")[第 9 频道： Doug 七： 代码理解和使用 Visual Studio 2010 进行系统设计](http://go.microsoft.com/fwlink/?LinkId=216100)<br /><br /> ![视频链接](../data-tools/media/playvideo.gif "播放视频")[第 9 频道： 构建应用程序使用层关系图](http://go.microsoft.com/fwlink/?LinkID=201117)<br /><br /> ![视频链接](../data-tools/media/playvideo.gif "播放视频") [MSDN 如何实现系列： 如何使用层关系图验证代码](http://go.microsoft.com/fwlink/?LinkID=214405)|  
|**论坛**|-   [Visual Studio 可视化和建模工具](http://go.microsoft.com/fwlink/?LinkId=184720)<br />-   [Visual Studio 可视化和建模 SDK（DSL 工具）](http://go.microsoft.com/fwlink/?LinkId=184721)|  
|**博客**|-   [Visual Studio ALM + Team Foundation Server 博客](http://go.microsoft.com/fwlink/?LinkID=201340)|  
|**技术文章和日志**|[MSDN 体系结构中心](http://go.microsoft.com/fwlink/?LinkId=201343)|  
  
## <a name="see-also"></a>请参阅  
 [测试应用程序](http://msdn.microsoft.com/library/796b7d6d-ad45-4772-9719-55eaf5490dac)   
 [扩展 UML 模型和关系图](../modeling/extend-uml-models-and-diagrams.md)   
 [建立用户需求模型](../modeling/model-user-requirements.md)   
 [体系结构分析和建模](../modeling/analyze-and-model-your-architecture.md)



