---
title: 'Procedura: creare una libreria attività | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1eeebe74-7303-4345-8a83-fe37a26bc84b
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 341e87459cbaae204baba66108a5944eb1f7f97f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49271831"
---
# <a name="how-to-create-an-activity-library"></a>Procedura: creare una libreria attività
Le attività personalizzate sono usate per modellare i processi aziendali particolari in un flusso di lavoro. Il modello Libreria attività in [!INCLUDE[vs2010](../includes/vs2010-md.md)] è stato fornito per consentire di creare tali attività personalizzate usando visivamente [!INCLUDE[wfd1](../includes/wfd1-md.md)].  
  
### <a name="to-create-a-workflow-activity-library"></a>Per creare una libreria attività flussi di lavoro  
  
1.  Avviare [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
2.  Nel **File** dal menu **New**, quindi selezionare **progetto...** .  
  
     Verrà visualizzata la finestra di dialogo **Nuovo progetto** .  
  
3.  Nel **tipi di progetto** riquadro, selezionare **flusso di lavoro** dal **Visual c#** progetti o **Visual Basic** raggruppamenti in base il preferenze della lingua.  
  
4.  Nel **modelli** riquadro, selezionare **libreria attività**.  
  
5.  Nel **nome** casella, digitare un nome descrittivo per il progetto affinché sia facilmente identificabile.  
  
6.  Nel **posizione** casella, digitare nella directory in cui si desidera salvare il progetto oppure fare clic su **Sfoglia** per spostarsi su di esso.  
  
7.  Nel **soluzione** casella, digitare un nome descrittivo per la soluzione, quindi fare clic su **OK**.  
  
    > [!NOTE]
    >  Se si desidera aggiungere un'applicazione console flusso di lavoro a una soluzione esistente, aprire la soluzione in [!INCLUDE[vs2010](../includes/vs2010-md.md)], fare clic con il pulsante destro la soluzione in **Esplora soluzioni**e selezionare **Add**, quindi  **Nuovo progetto...** Per aprire la **nuovo progetto** nella finestra di dialogo. Procedere come descritto sopra in questa procedura.  
  
8.  Il modello di progetto crea una definizione di attività in XAML. [!INCLUDE[wfd1](../includes/wfd1-md.md)] verrà visualizzato con l'area di disegno per l'attività personalizzata.  
  
9. Trascinare un'attività dal **casella degli strumenti** all'area di progettazione per includerla nell'attività personalizzata.  
  
    > [!CAUTION]
    >  È consentita una sola attività figlio nel corpo dell'attività personalizzata. L'attività in questione può tuttavia essere un oggetto CompositeActivity, quale <xref:System.Activities.Statements.Sequence> o <xref:System.Activities.Statements.Flowchart>.  
  
## <a name="see-also"></a>Vedere anche  
 [Procedura: creare un'attività](http://msdn.microsoft.com/library/c09b1e99-21b5-4d96-9c04-ec31db3f4436)   
 [Creazione di un progetto flusso di lavoro](../workflow-designer/creating-a-workflow-project.md)