---
title: Gli ActivityDesigner del flusso di controllo | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ba74af23-5398-4e62-bd90-c50612e3bfef
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 58ddd15d37e36494fef9488638727c7bc2142aa3
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47531783"
---
# <a name="control-flow-activity-designers"></a>ActivityDesigner Flusso di controllo
[!INCLUDE[wfd1](../includes/wfd1-md.md)] include alcune attività fornite dal sistema che è possibile usare per la costruzione di flussi di lavoro. Contenuto della sezione sono presentate le attività fornite dal sistema usate per controllare il flusso all'interno di un flusso di lavoro. Negli argomenti riportati di seguito vengono illustrate queste attività e viene fornito materiale sussidiario sulle relative modalità di utilizzo.  
  
## <a name="in-this-section"></a>In questa sezione  
 [DoWhile](../workflow-designer/dowhile-activity-designer.md)  
 Esegue l'attività contenuta nel rispettivo corpo almeno una volta, fino a quando una condizione specificata viene valutata **true**.  
  
 [ForEach\<T >](http://msdn.microsoft.com/en-us/a680cddd-2760-497a-b27b-c023fcbc6f33)  
 Esegue l'attività contenuta nel rispettivo corpo per ogni elemento di una raccolta specificata.  
  
 [Se](../workflow-designer/if-activity-designer.md)  
 Valuta una condizione ed esegue un'attività che dipende dai risultati di tale valutazione.  
  
 [Parallel](../workflow-designer/parallel-activity-designer.md)  
 Esegue contemporaneamente una raccolta delle attività figlio.  
  
 [Attività ParallelForEach\<T >](../workflow-designer/parallelforeach-t-activity-designer.md)  
 Enumera gli elementi di una raccolta ed esegue un'istruzione incorporata per ogni elemento della raccolta in parallelo.  
  
 [Pick](../workflow-designer/pick-activity-designer.md)  
 Esegue uno di diversi rami in risposta a un evento che fornisce controllo di flusso basato sull'evento.  
  
 [PickBranch](../workflow-designer/pickbranch-activity-designer.md)  
 Offre un percorso potenziale di esecuzione all'interno di un'attività <xref:System.Activities.Statements.Pick>.  
  
 [Sequence](../workflow-designer/sequence-activity-designer.md)  
 Contiene una raccolta ordinata di attività figlio eseguite nell'ordine.  
  
 [Commutatore\<T >](http://msdn.microsoft.com/en-us/ce1aa634-c4db-4475-a1c8-a88478a57212)  
 Valuta un'espressione specificata e viene eseguita da una raccolta di attività la cui chiave associata corrisponde al valore ottenuto dalla valutazione.  
  
 [While](../workflow-designer/while-activity-designer.md)  
 Esegue l'attività contenuta nel rispettivo corpo, mentre una condizione specificata viene valutata **true**.  
  
## <a name="reference"></a>Riferimenti  
 <xref:System.Activities.Activity>  
  
 <xref:System.Activities.Statements.DoWhile>  
  
 <xref:System.Activities.Statements.ForEach%601>  
  
 <xref:System.Activities.Statements.If>  
  
 <xref:System.Activities.Statements.Parallel>  
  
 <xref:System.Activities.Statements.ParallelForEach%601>  
  
 <xref:System.Activities.Statements.Pick>  
  
 <xref:System.Activities.Statements.PickBranch>  
  
 <xref:System.Activities.Statements.Sequence>  
  
 <xref:System.Activities.Statements.Switch%601>  
  
 <xref:System.Activities.Statements.While>  
  
## <a name="related-sections"></a>Sezioni correlate  
 Per gli altri tipi di ActivityDesigner, vedere gli argomenti seguenti.  
  
 [Uso degli Activity Designer](../workflow-designer/using-the-activity-designers.md)  
  
 [Diagramma di flusso](../workflow-designer/flowchart-activity-designers.md)  
  
 [Messaging](../workflow-designer/messaging-activity-designers.md)  
  
 [Runtime](../workflow-designer/runtime-activity-designers.md)  
  
 [Primitive](../workflow-designer/primitives-activity-designers.md)  
  
 [Transazione](../workflow-designer/transaction-activity-designers.md)  
  
 [Raccolta](../workflow-designer/collection-activity-designers.md)  
  
 [Gestione degli errori](../workflow-designer/error-handling-activity-designers.md)  
  
## <a name="external-resources"></a>Risorse esterne  
 [Uso degli Activity Designer](../workflow-designer/using-the-activity-designers.md)