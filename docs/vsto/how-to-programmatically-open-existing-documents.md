---
title: 'Procedura: A livello di codice aprire documenti esistenti'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], opening
- Word [Office development in Visual Studio], opening documents
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 2163ddc7db3f0fbcf32abaa8c845b3838e9d2c98
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53932155"
---
# <a name="how-to-programmatically-open-existing-documents"></a>Procedura: A livello di codice aprire documenti esistenti
  Il <xref:Microsoft.Office.Interop.Word.Documents.Open%2A> metodo apre il documento di Microsoft Office Word esistente, specificato da un nome di file e percorso completo. Questo metodo restituisce un <xref:Microsoft.Office.Interop.Word.Document> che rappresenta il documento aperto.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="to-open-a-document"></a>Per aprire un documento  
  
-   Chiamare il <xref:Microsoft.Office.Interop.Word.Documents.Open%2A> metodo di <xref:Microsoft.Office.Interop.Word.Documents> raccolta e specificare un percorso del documento.  
  
     [!code-vb[Trin_VstcoreWordAutomation#5](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#5)]
     [!code-csharp[Trin_VstcoreWordAutomation#5](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#5)]  
  
## <a name="to-open-a-document-as-read-only"></a>Per aprire un documento in sola lettura  
  
-   Chiamare il <xref:Microsoft.Office.Interop.Word.Documents.Open%2A> metodo, fornire un percorso del documento e impostare il *ReadOnly* argomento **True** nella chiamata al metodo.  
  
     [!code-vb[Trin_VstcoreWordAutomation#6](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#6)]
     [!code-csharp[Trin_VstcoreWordAutomation#6](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#6)]  
  
## <a name="compile-the-code"></a>Compilare il codice  
 Questo esempio di codice presenta i requisiti seguenti:  
  
-   Un documento denominato *NewDocument. doc* deve essere presente in una directory denominata *Test* nell'unità C.  
  
## <a name="see-also"></a>Vedere anche  
 [Procedura: Creazione di nuovi documenti a livello di codice](../vsto/how-to-programmatically-create-new-documents.md)   
 [Procedura: Chiudere i documenti a livello di codice](../vsto/how-to-programmatically-close-documents.md)   
 [Parametri facoltativi nelle soluzioni Office](../vsto/optional-parameters-in-office-solutions.md)  
