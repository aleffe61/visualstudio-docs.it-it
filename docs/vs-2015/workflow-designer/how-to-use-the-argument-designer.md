---
title: 'Procedura: usare la finestra di progettazione argomenti | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Presentation.View.ArgumentDesigner.UI
- System.Activities.Presentation.View.DesignTimeArgument.UI
ms.assetid: 64813fd5-1ea1-499a-98b4-ab2a44b7ee5e
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 81b24b8c0344cc6a8cf1559126a4faf0bc2b6f4e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49206622"
---
# <a name="how-to-use-the-argument-designer"></a>Procedura: utilizzare la finestra di progettazione argomenti
Se confrontata con le versioni precedenti di [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)], la finestra di progettazione argomenti semplifica il flusso di dati da e verso un'attività. Viene visualizzata la finestra di progettazione facendo il **argomenti** pulsante nell'angolo inferiore sinistro dell'area di progettazione. La finestra di progettazione contiene un elenco di argomenti che vengono visualizzati in un formato tabulare e possono essere ordinati per ognuna delle intestazioni di colonna, tranne per il **il valore predefinito** colonna. Ogni argomento include un nome, una direzione per la proprietà in/out/in-out, un tipo e un valore di espressione predefinito (se presente). Il nome e il valore di espressione predefinito sono campi di testo modificabili, mentre il tipo e la direzione sono elenchi a discesa. [!INCLUDE[crabout](../includes/crabout-md.md)] gli argomenti, vedere [variabili e argomenti](http://msdn.microsoft.com/library/d03dbe34-5b2e-4f21-8b57-693ee49611b8).  
  
### <a name="to-create-a-new-argument"></a>Per creare un nuovo argomento  
  
1.  Aprire una soluzione per flusso di lavoro o attività in [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
2.  Aprire la finestra di progettazione scegliendo il **argomenti** pulsante nell'angolo inferiore sinistro dell'area di progettazione. Verrà visualizzata la finestra di progettazione argomenti.  
  
3.  Fare clic sulla riga vuota denominata **Crea argomento**. Verrà aggiunta una nuova riga con un nuovo argomento usando i valori predefiniti seguenti: argumentx per il **Name** dove x è di tipo integer e un valore iniziale pari a 1 che viene incrementato automaticamente per creare i nomi di argomento univoco, **In**  per il **direzione**, e **stringa** per i **tipo di argomento**. Non vengono aggiunti valori per **il valore predefinito**. Tali valori possono essere modificati in qualsiasi momento durante il processo di progettazione del flusso di lavoro.  
  
    > [!NOTE]
    >  Per eliminare un argomento, selezionare l'argomento facendovi clic sopra e quindi premere il **eliminare** chiave.  
  
## <a name="see-also"></a>Vedere anche  
 [Usando la finestra di progettazione del flusso di lavoro](../workflow-designer/using-the-workflow-designer.md)   
 [Variabili e argomenti](http://msdn.microsoft.com/library/d03dbe34-5b2e-4f21-8b57-693ee49611b8)