---
title: 按钮元素 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Buttons element (VSCT XML schema)
- VSCT XML schema elements, Buttons
ms.assetid: 9f2cf94d-dec5-4776-a836-9a89c75f0c87
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0d11ef8797211939b25629d96020af4ee8daa361
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49865006"
---
# <a name="buttons-element"></a>Buttons 元素
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

组[按钮](../extensibility/button-element.md)元素，它表示单个命令。  
  
## <a name="syntax"></a>语法  
  
```  
<Buttons>  
  <Button>... </Button>  
  <Button>... </Button>  
</Buttons>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|条件|可选。 请参阅[条件属性](../extensibility/vsct-xml-schema-conditional-attributes.md)。|  
  
### <a name="child-elements"></a>子元素  
  
|元素|描述|  
|-------------|-----------------|  
|[Buttons 元素](../extensibility/buttons-element.md)|按钮元素进行分组。|  
|[Button 元素](../extensibility/button-element.md)|定义用户可与之交互的命令。|  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[Commands 元素](../extensibility/commands-element.md)|表示 VSPackage 工具栏上的命令的集合。|  
  
## <a name="example"></a>示例  
  
```  
<Buttons>  
  <Button guid="guidMenuAndCommandsCmdSet" id="cmdidMyCommand"     priority="0x100" type="Button">  
    <Parent guid="guidMenuAndCommandsCmdSet" id="MyMenuGroup"/>  
    <Icon guid="guidGenericCmdBmp" id="bmpArrow"/>  
    <Strings>  
      <ButtonText>C# Command Sample</ButtonText>  
    </Strings>  
  </Button>  
</Buttons>  
```  
  
## <a name="see-also"></a>请参阅  
 [Vspackage 如何添加用户界面元素](../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [命令、菜单和工具栏](../extensibility/internals/commands-menus-and-toolbars.md)

