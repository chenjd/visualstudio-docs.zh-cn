---
title: UML 模型元素类型 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- UML API, types
ms.assetid: 25345a53-7246-4eb7-8ad9-0b695aa171a2
caps.latest.revision: 10
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: 782485523cd5c80e61032eafc575c111592895b6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49252377"
---
# <a name="uml-model-element-types"></a>UML 模型元素类型
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

你可以通过编程接口读取和处理 UML 模型。 本主题总结了元素类型的层次结构。 层次结构与 UML 规范中的定义相同。  
  
 中提供了每种类型的详细信息[UML 建模扩展性的 API 参考](../modeling/api-reference-for-uml-modeling-extensibility.md)。  
  
## <a name="element-types"></a>元素类型  
 这是在程序集 `Microsoft.VisualStudio.Uml.Interfaces.dll` 中定义的类型集。  
  
 各个项的完全限定名即列出的名称后的“`Microsoft.VisualStudio.Uml.`”。  
  
 为方便起见，此列表被设计为继承层次结构。 某个类型有多个超类型，则其他超类型会在冒号 (:) 后列出。  
  
```  
  
Classes.IElement  
|  Activities.IActivityGroup  
|  Classes.IComment  
|  Classes.IMultiplicityElement  
|  |  CompositeStructures.IConnectorEnd  
|  Classes.INamedElement  
|  |  Deployments.IDeployedArtifact  
|  |  Deployments.IDeploymentTarget  
|  |  |  Classes.IInstanceSpecification  
             : Deployments.IDeployedArtifact,  
               Deployments.IDeploymentTarget  
|  |  |  |  Classes.IEnumerationLiteral  
|  |  Interactions.IInteractionFragment  
|  |  |  Interactions.ICombinedFragment  
|  |  |  |  Interactions.IConsiderIgnoreFragment  
|  |  |  Interactions.IExecutionSpecification  
|  |  |  |  Interactions.IActionExecutionSpecification  
|  |  |  |  Interactions.IBehaviorExecutionSpecification  
|  |  |  Interactions.IInteraction  : CommonBehaviors.IBehavior  
|  |  |  Interactions.IInteractionOperand : Classes.INamespace  
|  |  |  Interactions.IInteractionUse  
|  |  |  Interactions.IOccurrenceSpecification  
|  |  |  |  Interactions.IExecutionOccurrenceSpecification  
|  |  |  |  Interactions.IMessageOccurrenceSpecification  
                   : Interactions.IMessageEnd  
|  |  |  |  |  Interactions.ILostFoundTarget  
|  |  |  |  Interactions.IOperandOccurrenceSpecification  
|  |  |  Interactions.IStateInvariant  
|  |  Interactions.ILifeline  
|  |  Interactions.IMessage  
|  |  Interactions.IMessageEnd  
|  |  Classes.INamespace  
|  |  |  Classes.IPackage  
             : Classes.IPackageableElement,  
              AuxiliaryConstructs.ITemplateableElement  
|  |  |  |  AuxiliaryConstructs.IModel  
|  |  |  Activities.IState  
|  |  Classes.IPackageableElement        
                   : AuxiliaryConstructs.IParameterableElement  
|  |  |  Classes.IConstraint  
|  |  |  |  Interactions.IInteractionConstraint  
|  |  |  CommonBehaviors.IEvent  
|  |  |  |  Interactions.IExecutionEvent  
|  |  |  |  CommonBehaviors.IMessageEvent  
|  |  |  |  |  CommonBehaviors.ICallEvent  
|  |  |  |  |  Interactions.IReceiveOperationEvent  
|  |  |  |  |  Interactions.IReceiveSignalEvent  
|  |  |  |  |  Interactions.ISendOperationEvent  
|  |  |  |  |  Interactions.ISendSignalEvent  
|  |  |  Classes.IType  
|  |  |  |  Classes.IClassifier : Classes.INamespace, Classes.IRedefinableElement, AuxiliaryConstructs.ITemplateableElement  
|  |  |  |  |  Deployments.IArtifact  
                   : Deployments.IDeployedArtifact  
|  |  |  |  |  |  Deployments.IDeploymentSpecification  
|  |  |  |  |  CommonBehaviors.IBehavioredClassifier  
|  |  |  |  |  |  UseCases.IActor  
|  |  |  |  |  |  Classes.IClass        
                         : CompositeStructures.IEncapsulatedClassifier  
|  |  |  |  |  |  |  CommonBehaviors.IBehavior  
|  |  |  |  |  |  |  |  Activities.IActivity  
|  |  |  |  |  |  |  Components.IComponent  
|  |  |  |  |  |  |  |  UseCases.ISubsystem  
|  |  |  |  |  |  |  Deployments.INode : IDeploymentTarget  
|  |  |  |  |  |  |  |  Deployments.IDevice  
|  |  |  |  |  |  |  |  Deployments.IExecutionEnvironment  
|  |  |  |  |  |  UseCases.IUseCase  
|  |  |  |  |  Classes.IDataType  
|  |  |  |  |  |  Classes.IEnumeration  
|  |  |  |  |  |  Classes.IPrimitiveType  
|  |  |  |  |  Classes.IInterface  
|  |  |  |  |  CompositeStructures.IStructuredClassifier  
|  |  |  |  |  |  CompositeStructures.IEncapsulatedClassifier  
|  |  |  Classes.IValueSpecification : Classes.ITypedElement  
|  |  |  |  Classes.IExpression  
|  |  |  |  Classes.IInstanceValue  
|  |  |  |  Classes.ILiteralSpecification  
|  |  |  |  |  Classes.ILiteralBoolean  
|  |  |  |  |  Classes.ILiteralInteger  
|  |  |  |  |  Classes.ILiteralNull  
|  |  |  |  |  Classes.ILiteralString  
|  |  |  |  |  Classes.ILiteralUnlimitedNatural  
|  |  |  |  Classes.IOpaqueExpression  
|  |  Classes.IRedefinableElement  
|  |  |  Activities.IActivityNode  
|  |  |  |  Activities.IControlNode  
|  |  |  |  |  Activities.IDecisionNode  
|  |  |  |  |  Activities.IFinalNode  
|  |  |  |  |  |  Activities.IActivityFinalNode  
|  |  |  |  |  Activities.IForkNode  
|  |  |  |  |  Activities.IInitialNode  
|  |  |  |  |  Activities.IJoinNode  
|  |  |  |  |  Activities.IMergeNode  
|  |  |  |  Activities.IExecutableNode  
|  |  |  |  |  Actions.IAction  
|  |  |  |  |  |  Actions.IAcceptEventAction  
|  |  |  |  |  |  Actions.ICreateObjectAction  
|  |  |  |  |  |  Actions.IInvocationAction  
|  |  |  |  |  |  |  Actions.ICallAction  
|  |  |  |  |  |  |  |  Actions.ICallBehaviorAction  
|  |  |  |  |  |  |  |  Actions.ICallOperationAction  
|  |  |  |  |  |  |  Actions.ISendSignalAction  
|  |  |  |  |  |  Actions.IOpaqueAction  
|  |  |  |  Activities.IObjectNode  : Classes.ITypedElement  
|  |  |  |  |  Activities.IActivityParameterNode  
|  |  |  |  |  Actions.IPin : Classes.IMultiplicityElement  
|  |  |  |  |  |  Actions.IInputPin  
|  |  |  |  |  |  Actions.IOutputPin  
|  |  |  UseCases.IExtensionPoint  
|  |  |  Classes.IFeature  
|  |  |  |  Classes.IBehavioralFeature  : Classes.INamespace  
|  |  |  |  |  Classes.IOperation  
                   : AuxiliaryConstructs.ITemplateableElement,  
                   AuxiliaryConstructs.IParameterableElement  
|  |  |  |  Classes.IStructuralFeature  
              : Classes.IMultiplicityElement,   
                Classes.ITypedElement  
|  |  |  |  |  Classes.IProperty  
                   : AuxiliaryConstructs.ITemplateableElement,   
                   CompositeStructures.IConnectableElement,   
                   Deployments.IDeploymentTarget  
|  |  |  |  |  |  CompositeStructures.IPort  
|  |  Classes.ITypedElement  
|  |  |  CompositeStructures.IConnectableElement  
             : AuxiliaryConstructs.IParameterableElement  
|  |  |  Classes.IParameter  : Classes.IMultiplicityElement, CompositeStructures.IConnectableElement  
|  AuxiliaryConstructs.IParameterableElement  
|  Classes.IProfileInstance  
  
|  Classes.IRelationship  
|  |  Activities.IActivityEdge : Classes.IRedefinableElement  
|  |  |  Activities.IControlFlow  
|  |  |  Activities.IObjectFlow  
|  |  Classes.IAssociation : IClassifier  
|  |  |  Deployments.ICommunicationPath  
|  |  CompositeStructures.IConnector  
|  |  Classes.IDirectedRelationship  
|  |  |  Classes.IDependency : Classes.IPackageableElement  
|  |  |  |  Classes.IAbstraction  
|  |  |  |  |  Deployments.IManifestation  
|  |  |  |  |  Classes.IRealization  
|  |  |  |  |  |  Classes.IInterfaceRealization  
|  |  |  |  Deployments.IDeployment  
|  |  |  |  Classes.IUsage  
|  |  |  UseCases.IExtend : Classes.INamedElement  
|  |  |  Classes.IGeneralization  
|  |  |  UseCases.IInclude : Classes.INamedElement  
|  |  |  Classes.IPackageImport  
|  |  |  AuxiliaryConstructs.ITemplateBinding  
|  Classes.IStereotypeInstance  
|  Classes.IStereotypePropertyInstance  
|  AuxiliaryConstructs.ITemplateableElement  
|  AuxiliaryConstructs.ITemplateParameter  
|  |  AuxiliaryConstructs.IClassifierTemplateParameter  
|  |  AuxiliaryConstructs.IOperationTemplateParameter  
|  AuxiliaryConstructs.ITemplateParameterSubstitution  
|  AuxiliaryConstructs.ITemplateSignature  
|  |  AuxiliaryConstructs.IRedefinableTemplateSignature   
             : Classes.IRedefinableElement  
```  
  
## <a name="see-also"></a>请参阅  
 [定义用于扩展 UML 的配置文件](../modeling/define-a-profile-to-extend-uml.md)   
 [为 UML 模型定义验证约束](../modeling/define-validation-constraints-for-uml-models.md)   
 [UML 建模扩展性的 API 参考](../modeling/api-reference-for-uml-modeling-extensibility.md)



