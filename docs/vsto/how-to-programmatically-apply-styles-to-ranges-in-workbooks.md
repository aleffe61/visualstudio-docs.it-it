---
title: 'Procedura: A livello di programmazione applicare stili agli intervalli in cartelle di lavoro'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, styles
- styles, workbook ranges
- workbooks, styles
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: d12b42d7af92204992f1e32cbb29f311d337b70f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096129"
---
# <a name="how-to-programmatically-apply-styles-to-ranges-in-workbooks"></a>Procedura: A livello di programmazione applicare stili agli intervalli in cartelle di lavoro
  È possibile applicare stili denominati alle aree nelle cartelle di lavoro. Excel fornisce alcuni stili predefiniti:  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
 La finestra di dialogo **Formato celle** mostra tutte le opzioni che è possibile usare per formattare le celle e ognuna di queste opzioni è disponibile dal codice. Per visualizzare questa finestra di dialogo in Excel, scegliere **Celle** dal menu **Formato** .  
  
## <a name="to-apply-a-style-to-a-named-range-in-a-document-level-customization"></a>Per applicare uno stile a un intervallo denominato in una personalizzazione a livello di documento  
  
1.  Creare un nuovo stile e impostare i relativi attributi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#53](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#53)]
     [!code-vb[Trin_VstcoreExcelAutomation#53](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#53)]  
  
2.  Creare un controllo <xref:Microsoft.Office.Tools.Excel.NamedRange>, assegnargli un testo e quindi applicare il nuovo stile. Questo codice deve essere inserito in una classe foglio, non nella classe `ThisWorkbook` .  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#54](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#54)]
     [!code-vb[Trin_VstcoreExcelAutomation#54](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#54)]  
  
## <a name="to-clear-a-style-from-a-named-range-in-a-document-level-customization"></a>Per cancellare uno stile da un intervallo denominato in una personalizzazione a livello di documento  
  
1.  Applicare lo stile Normale all'intervallo. Questo codice deve essere inserito in una classe foglio, non nella classe `ThisWorkbook` .  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#55](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#55)]
     [!code-vb[Trin_VstcoreExcelAutomation#55](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#55)]  
  
## <a name="to-apply-a-style-to-a-named-range-in-a-vsto-add-in"></a>Per applicare uno stile a un intervallo denominato in un componente aggiuntivo VSTO  
  
1.  Creare un nuovo stile e impostare i relativi attributi.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#28](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#28)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#28](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#28)]  
  
2.  Creare un oggetto <xref:Microsoft.Office.Interop.Excel.Range>, assegnargli un testo e quindi applicare il nuovo stile.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#29](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#29)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#29](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#29)]  
  
## <a name="to-clear-a-style-from-a-named-range-in-a-vsto-add-in"></a>Per cancellare uno stile da un intervallo denominato in un componente aggiuntivo VSTO  
  
1.  Applicare lo stile Normale all'intervallo.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#56](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#56)]
     [!code-vb[Trin_VstcoreExcelAutomation#56](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#56)]  
  
## <a name="see-also"></a>Vedere anche  
 [Lavorare con intervalli](../vsto/working-with-ranges.md)   
 [NamedRange (controllo)](../vsto/namedrange-control.md)   
 [Accesso globale a oggetti nei progetti di Office](../vsto/global-access-to-objects-in-office-projects.md)   
 [Parametri facoltativi nelle soluzioni Office](../vsto/optional-parameters-in-office-solutions.md)  
