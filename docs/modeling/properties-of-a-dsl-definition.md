---
title: DSL 定义的属性
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Domain-Specific Language, definition file
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: 990b55f4ba78f32acba40c325ade596f5628c54f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49893931"
---
# <a name="properties-of-a-dsl-definition"></a>DSL 定义的属性
DslDefinition 属性定义*域特定语言*定义属性，如版本编号。 DslDefinition 属性将显示在**属性**窗口时单击关系图中的空白区域*域特定语言设计器*。

 有关详细信息，请参阅[如何定义特定于域的语言](../modeling/how-to-define-a-domain-specific-language.md)。 有关如何使用这些属性的详细信息，请参阅[自定义和扩展域特定语言](../modeling/customizing-and-extending-a-domain-specific-language.md)。

 DslDefinition 具有下表中的属性：

|属性|描述|默认|
|-|-|-|
|访问修饰符|确定域类的访问修饰符是否为公用或内部。|public|
|自定义特性|自定义的域类的属性。<br /><br /> **请注意**使用浏览按钮将属性添加。|\<无 >|
|公司名称|在系统注册表中的当前公司名称的名称。|当前的公司名称|
|name|此域类的名称。|当前名称|
|命名空间|隶属于此域类的命名空间。|当前命名空间|
|包 Guid|为此 DSL 生成的 Visual Studio 包 guid。|\<无 >|
|包 Namespace|为此 DSL 生成的 Visual Studio 包命名空间。|\<无 >|
|产品名称|将注册为此 DSL 生成的 Visual Studio 包的产品名称。|\<无 >|
|说明|与此域类相关联的注释。|\<无 >|
|描述|此域类的说明。|\<无 >|
|显示名称|将此域类生成的设计器中显示的名称。|\<无 >|
|帮助关键字|与此域类关联的帮助关键字。|\<无 >|
|生成|有关此特定于域的语言定义的增量生成数。|0|
|主要版本|有关此特定于域的语言定义的增量的主要版本号。|1|
|次要版本|有关此特定于域的语言定义的增量的次要版本号。|0|
|Revision|有关此特定于域的语言定义的递增修订版本号。|0|

## <a name="see-also"></a>请参阅

- [域特定语言工具术语表](http://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)