---
title: "Procedura: creare un'applicazione Console flusso di lavoro | Microsoft Docs"
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a2eea7-921c-49f1-b358-68afc27f1ee9
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 8a6b38f6026e7a9bba1e668f47a37b32feaa2b7f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47517480"
---
# <a name="how-to-create-a-workflow-console-application"></a>Procedura: creare un'applicazione console flusso di lavoro
[!INCLUDE[wf](../includes/wf-md.md)] consente di creare flussi di lavoro per l'esecuzione di processi di utenti o di sistema. [!INCLUDE[wfd1](../includes/wfd1-md.md)] fornisce l'area di progettazione per la creazione di tali flussi. La [!INCLUDE[wfd2](../includes/wfd2-md.md)] può essere usata per creare flussi di lavoro dall'interno di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] o può essere integrata in altre applicazioni che riallocano la finestra di progettazione.  
  
 In questo argomento viene descritto come usare la [!INCLUDE[wfd2](../includes/wfd2-md.md)] in [!INCLUDE[vs2010](../includes/vs2010-md.md)] per creare un flusso di lavoro in un'applicazione console.  
  
### <a name="to-create-a-workflow-console-application"></a>Per creare un'applicazione console flusso di lavoro  
  
1.  Avviare [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
2.  Nel **File** dal menu **New**, quindi selezionare **progetto...** .  
  
     Verrà visualizzata la finestra di dialogo **Nuovo progetto** .  
  
3.  Nel **modelli installati** riquadro, selezionare **flusso di lavoro** dal **Visual c#** o **Visual Basic** raggruppamenti, a seconda di lingua di preferenza.  
  
4.  Nel riquadro centrale, selezionare **applicazione Console flusso di lavoro**.  
  
5.  Nel **nome** immettere un nome descrittivo per il progetto affinché sia facilmente identificabile.  
  
6.  Nel **posizione** casella, immettere la directory in cui si desidera salvare il progetto oppure fare clic su **Sfoglia** per spostarsi su di esso.  
  
7.  Nel **soluzione** immettere il nome per la nuova soluzione. Fare clic su **OK** per creare l'applicazione.  
  
    > [!NOTE]
    >  Se si desidera aggiungere un'applicazione console flusso di lavoro a una soluzione esistente, aprire la soluzione in [!INCLUDE[vs2010](../includes/vs2010-md.md)], fare clic con il pulsante destro la soluzione in **Esplora soluzioni**e selezionare **Add**, quindi  **Nuovo progetto...** Per aprire la **nuovo progetto** nella finestra di dialogo. Procedere come descritto sopra in questa procedura.  
  
8.  Il modello di progetto crea una definizione del flusso di lavoro in XAML mentre la definizione dell'applicazione console è in codice sorgente. In [!INCLUDE[wfd2](../includes/wfd2-md.md)] verrà visualizzata l'area di disegno per il flusso di lavoro creato.  
  
9. Per creare un flusso di lavoro, trascinare attività o altri elementi del flusso di lavoro dal **casella degli strumenti** all'area di progettazione del flusso di lavoro.  
  
## <a name="see-also"></a>Vedere anche  
 [Creazione di un progetto flusso di lavoro](../workflow-designer/creating-a-workflow-project.md)