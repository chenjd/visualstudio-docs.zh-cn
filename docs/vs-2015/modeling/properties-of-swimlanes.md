---
title: 泳道属性 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.dsltools.dsldesigner.swimlane
helpviewer_keywords:
- Domain-Specific Language, swimlane
ms.assetid: 47edbc2d-09e4-48ac-b4d1-5268a06a27e6
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: c914703d4cbe48e516d1d4e1aa48afb20c9e1cfe
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49189925"
---
# <a name="properties-of-swimlanes"></a>泳道属性
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

可以将泳道添加到关系图。 泳道将关系图划分为垂直或水平区域。 您可以定义要显示在泳道内其他形状。 有关详细信息，请参阅[如何定义特定于域的语言](../modeling/how-to-define-a-domain-specific-language.md)。 有关如何使用这些属性的详细信息，请参阅[自定义和扩展域特定语言](../modeling/customizing-and-extending-a-domain-specific-language.md)。  
  
 泳道具有下表中列出的属性。  
  
|属性|描述|默认|  
|--------------|-----------------|-------------|  
|正文填充颜色|泳道主体的填充颜色。|白色|  
|标头填充颜色|泳道标头填充颜色。|深灰|  
|分隔符颜色|分隔线的颜色。|LightGray|  
|分隔符行样式|分隔线的样式 (`Solid`， `Dash`， `Dot`， `DashDot`， `DashDotDot`，或`Custom`)。|`Dash`|  
|分隔符宽度|以英寸为单位分隔线的粗细。|0.03125|  
|文本颜色|使用与此泳道相关联的文本修饰器的颜色。|黑色|  
|访问修饰符|类的访问级别 (`public`或`internal`)。|Public|  
|自定义特性|用于将属性添加到此泳道从生成的代码类。|\<无 >|  
|生成双派生|如果`True`，将生成的基类和一个分部类 （以支持通过重写自定义）。 有关详细信息，请参阅[重写和扩展生成的类](../modeling/overriding-and-extending-the-generated-classes.md)。|False|  
|具有自定义构造函数|如果`True`，将在源代码中提供自定义构造函数。 有关详细信息，请参阅[重写和扩展生成的类](../modeling/overriding-and-extending-the-generated-classes.md)。|False|  
|继承修饰符|介绍的从泳道生成源代码类的继承的类型 (`none`，`abstract`或`sealed`)。|无|  
|基本泳道|此泳道的基类。|(无)|  
|name|此泳道的名称。|当前名称|  
|命名空间|隶属于此泳道的命名空间。|当前命名空间|  
|工具提示类型|如何定义工具提示 (`fixed`， `variable`，或`none`)。 如果`fixed`，则将的值`Fixed Tooltip Text`使用属性; 如果`variable`，然后在自定义代码中定义工具提示。|\<无 >|  
|说明|此泳道与相关联的非正式说明。|\<无 >|  
|对齐方式|水平或垂直对齐方式。|垂直|  
|初始高度|此泳道，以英寸为单位的初始高度。 仅适用于水平泳道。|0|  
|初始宽度|此泳道，以英寸为单位的初始宽度。 仅适用于垂直泳道。|0|  
|公开文本颜色|如果`True`，用户可以在生成的设计器中设置颜色的泳道。 若要将此项设置，请右击泳道形状，然后单击**公开添加**。|False|  
|描述|用于记录生成的设计器。|\<无 >|  
|显示名称|将显示在生成的设计器来指代此泳道类名称。|\<无 >|  
|固定工具提示文本|用于固定工具提示文本。|\<无 >|  
|帮助关键字|用于索引此泳道的 F1 帮助关键字。|\<无 >|  
  
## <a name="see-also"></a>请参阅  
 [域特定语言工具术语表](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)



