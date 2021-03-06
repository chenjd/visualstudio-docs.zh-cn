---
title: 工作流设计器-CancellationScope 活动设计器
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.Activities.Statements.CancellationScope.UI
ms.assetid: 2c85d663-b219-4142-9866-7693ffd46379
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d3b9e565e5579405fa73ea6a3de12d7c27ed7edc
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49926834"
---
# <a name="cancellationscope-activity-designer"></a>CancellationScope 活动设计器

**CancellationScope**活动设计器用于创建和配置<xref:System.Activities.Statements.CancellationScope>活动。

## <a name="the-cancellationscope-activity"></a>CancellationScope 活动

使用 <xref:System.Activities.Statements.CancellationScope> 活动可指定要执行的活动以及该活动的取消逻辑。

### <a name="using-the-cancellationscope-activity-designer"></a>使用 CancellationScope 活动设计器

**CancellationScope**活动设计器可在**事务**类别**工具箱**。 若要打开**工具箱**，选择**工具箱**工作流设计器选项卡。 或者，选择**工具箱**从**视图**菜单中或按**Ctrl**+**Alt** + **X**。

**CancellationScope**活动设计器可以从拖动**工具箱**无论在何处放置活动的如内放置到工作流设计器图面和<xref:System.Activities.Statements.Sequence>。 删除**CancellationScope**活动设计器创建<xref:System.Activities.Statements.CancellationScope>默认值的活动<xref:System.Activities.Activity.DisplayName%2A>CancellationScope。 编辑<xref:System.Activities.Activity.DisplayName%2A>的标头的值**CancellationScope**活动设计器。 你还可以编辑在**DisplayName**属性网格的框。

### <a name="the-cancellationscope-properties"></a>CancellationScope 属性

下表列出 <xref:System.Activities.Statements.CancellationScope> 属性并说明如何在设计器中使用它们。 <xref:System.Activities.Activity.DisplayName%2A>属性可以在属性网格中编辑，但其他属性必须编辑工作流设计器图面上。

|属性名|必需|用法|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|<xref:System.Activities.Statements.CancellationScope> 活动的可选友好名称。 默认值为 CancellationScope。 虽然 <xref:System.Activities.Activity.DisplayName%2A> 值不是绝对必需的，但最好使用该属性值。|
|<xref:System.Activities.Statements.CancellationScope.Body%2A>|True|指定为其提供取消逻辑的活动。 若要添加<xref:System.Activities.Statements.CancellationScope.Body%2A>活动，请将活动从拖**工具箱**到**正文**框**CancellationScope**活动设计器。 添加提示文本"此处放置活动"。|
|<xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A>|True|指定如果没有取消执行的活动。 若要添加<xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A>活动，请将活动从拖**工具箱**到**CancellationHandler**框**CancellationScope**活动设计器。 添加提示文本"此处放置活动"。|

## <a name="see-also"></a>请参阅

- [事务](../workflow-designer/transaction-activity-designers.md)
- [CompensableActivity](../workflow-designer/compensableactivity-activity-designer.md)
- [Compensate](../workflow-designer/compensate-activity-designer.md)
- [Confirm](../workflow-designer/confirm-activity-designer.md)
- [TransactionScope](../workflow-designer/transactionscope-activity-designer.md)