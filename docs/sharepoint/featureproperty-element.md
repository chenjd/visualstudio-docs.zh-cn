---
title: FeatureProperty 元素 |Microsoft Docs
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- FeatureProperty element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: ccc9e0d628d5c17283368de135c8e83dbd40bec1
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2018
ms.locfileid: "36325977"
---
# <a name="featureproperty-element"></a>FeatureProperty 元素
  表示部署到 SharePoint 时，将包括与某个功能的自定义属性。 将功能部署后，您可以在代码中访问属性。  
  
## <a name="syntax"></a>语法  
  
```xml  
<FeatureProperty Key = "Key of the property value"  
    Value = "Property value" />  
```  
  
## <a name="attributes-and-elements"></a>特性和元素
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|**Key**|所需**xs: string**属性。<br /><br /> 用于存储和检索属性值的键。 每个属性必须具有在该功能中是唯一的密钥。|  
|**值**|所需**xs: string**属性。<br /><br /> 属性值。|  
  
### <a name="child-elements"></a>子元素
 无。  
  
### <a name="parent-elements"></a>父元素
  
|元素|描述|  
|-------------|-----------------|  
|[FeatureProperties](../sharepoint/featureproperties-element.md)|表示部署到 SharePoint 时，包含与某个功能的属性值的集合。|  
  
## <a name="remarks"></a>备注  
 功能属性的详细信息，请参阅[提供在项目项中的包和部署信息](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)。  
  
## <a name="element-information"></a>元素信息
  
|||  
|-|-|  
|**命名空间**|http<nolink>: //schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|  
|**架构名称**|SharePoint 项目项架构|  
|**验证文件**|ProjectItemModelSchema.xsd|  
|**可以为空**|否|  
  
## <a name="see-also"></a>请参阅
 [SharePoint 项目项架构参考](../sharepoint/sharepoint-project-item-schema-reference.md)   
 [提供在项目项中的打包和部署信息](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)  
  
  
