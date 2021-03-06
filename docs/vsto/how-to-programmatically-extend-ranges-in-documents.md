---
title: 如何： 以编程方式扩展文档中的范围
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, extending
- documents [Office development in Visual Studio], extending ranges
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 810f65cbb021845c4fa659cd785e83e8c979376d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49888666"
---
# <a name="how-to-programmatically-extend-ranges-in-documents"></a>如何： 以编程方式扩展文档的范围
  定义 Microsoft Office Word 文档中的 <xref:Microsoft.Office.Interop.Word.Range> 对象后，可以通过使用 <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> 和 <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> 方法来更改其起点和终点。 <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A>并<xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A>方法不采用相同的两个自变量*单元*并*计数*。 *计数*参数是要移动的单位数和*单元*参数可以是下列任一<xref:Microsoft.Office.Interop.Word.WdUnits>值：  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdCharacter>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdWord>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdSentence>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdParagraph>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdSection>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdStory>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdCell>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdColumn>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdRow>  
  
- <xref:Microsoft.Office.Interop.Word.WdUnits.wdTable>  
  
  [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
  下面的示例定义了七个字符长的范围。 然后它将在原始开始位置之后移动范围的开始位置七个字符。 因为范围的结束位置也是开始位置之后的 7 个字符，则结果将是零个字符组成的范围。 然后代码在当前结束位置后移动结束位置七个字符。  
  
## <a name="to-extend-a-range"></a>若要扩展范围  
  
1.  定义字符的范围。 有关详细信息，请参阅[如何： 以编程方式定义和在文档中选择范围](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)。  
  
     下面的代码示例可用于文档级自定义项。  
  
     [!code-vb[Trin_VstcoreWordAutomation#39](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#39)]
     [!code-csharp[Trin_VstcoreWordAutomation#39](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#39)]  
  
     以下代码示例可用于 VSTO 外接程序。 本示例使用活动文档。  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#39](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#39)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#39](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#39)]  
  
2.  使用 <xref:Microsoft.Office.Interop.Word.Range.MoveStart%2A> 对象的 <xref:Microsoft.Office.Interop.Word.Range> 方法移动范围的开始位置。  
  
     [!code-vb[Trin_VstcoreWordAutomation#40](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#40)]
     [!code-csharp[Trin_VstcoreWordAutomation#40](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#40)]  
  
3.  使用 <xref:Microsoft.Office.Interop.Word.Range.MoveEnd%2A> 对象的 <xref:Microsoft.Office.Interop.Word.Range> 方法移动范围的结束位置。  
  
     [!code-vb[Trin_VstcoreWordAutomation#41](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#41)]
     [!code-csharp[Trin_VstcoreWordAutomation#41](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#41)]  
  
## <a name="document-level-customization-code"></a>文档级自定义代码  
  
### <a name="to-extend-a-range-in-a-document-level-customization"></a>若要在文档级自定义项中扩展范围  
  
1.  下面的示例显示文档级自定项的完整代码。 若要使用此代码，请从项目中的 `ThisDocument` 类运行它。  
  
     [!code-vb[Trin_VstcoreWordAutomation#38](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#38)]
     [!code-csharp[Trin_VstcoreWordAutomation#38](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#38)]  
  
## <a name="vsto-add-in-code"></a>VSTO 外接程序代码  
  
### <a name="to-extend-a-range-in-an-application-level-vsto-add-in"></a>若要扩展应用程序级 VSTO 外接程序中的范围  
  
1.  下面的示例显示 VSTO 外接程序的完整代码。 若要使用此代码，请从项目中的 `ThisAddIn` 类运行它。  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#38](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#38)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#38](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#38)]  
  
## <a name="see-also"></a>请参阅  
 [如何： 以编程方式重置 Word 文档中的范围](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md)   
 [如何： 以编程方式折叠范围或在文档中的选定内容](../vsto/how-to-programmatically-collapse-ranges-or-selections-in-documents.md)   
 [如何： 以编程方式定义和在文档中选择范围](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)   
 [如何： 以编程方式检索范围中的开始和结束字符](../vsto/how-to-programmatically-retrieve-start-and-end-characters-in-ranges.md)   
 [如何： 以编程方式创建范围时排除段落标记](../vsto/how-to-programmatically-exclude-paragraph-marks-when-creating-ranges.md)  
  