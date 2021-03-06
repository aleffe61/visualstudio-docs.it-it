---
title: Visualizzazione processi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.externaltools.spyplus.processesview
helpviewer_keywords:
- Processes view
ms.assetid: e144e70e-eef2-45a7-a562-a177f177d9a1
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b898713b456afd72f6453bad01028af9090b8dd2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53922955"
---
# <a name="processes-view"></a>Visualizzazione processi
La visualizzazione dei processi viene visualizzato un albero di tutti i processi attivi nel sistema. Vengono visualizzati il nome del modulo e l'ID processo. Se si vuole esaminare un particolare processo di sistema, che in genere corrisponde a un programma in esecuzione, usare la visualizzazione dei processi. I processi sono identificati da nomi di modulo o vengono designati come "processi di sistema".  
  
 Microsoft Windows supporta più processi. Ogni processo può avere uno o più thread e ogni thread può avere uno o più associate finestre di primo livello. Ogni finestra di primo livello può disporre di una serie di windows. Un simbolo + indica che un livello è compressa. La visualizzazione compressa è costituito da una riga per ogni processo. Scegliere il simbolo + per espandere il livello.  
  
 Se si vuole esaminare un particolare processo di sistema, che in genere corrisponde a un programma in esecuzione, usare la visualizzazione dei processi. I processi sono identificati da nomi di modulo o vengono designati come "processi di sistema". Per trovare un processo, comprimere l'albero e l'elenco di ricerca.  
  
## <a name="procedures"></a>Procedure  
  
#### <a name="to-open-the-processes-view"></a>Per aprire la visualizzazione dei processi  
  
1. Dal **Spy** menu, scegliere **processi**.  
  
   ![Spy&#43; &#43; visualizzazione processi](../debugger/media/spy--_processes.png "Spy + + _Processes")  
   Visualizzazione processi di Spy++  
  
   La figura precedente mostra la visualizzazione dei processi con thread e processi nodi espansi.  
  
### <a name="in-this-section"></a>In questa sezione  
 [La ricerca di un processo nella visualizzazione processi](../debugger/how-to-search-for-a-process-in-processes-view.md)  
 Viene illustrato come trovare un processo specifico nella visualizzazione processi.  
  
 [Visualizzazione delle proprietà processo](../debugger/how-to-display-process-properties.md)  
 Viene illustrato come visualizzare altre informazioni su un messaggio.  
  
### <a name="related-sections"></a>Sezioni correlate  
 [Visualizzazioni di Spy++](../debugger/spy-increment-views.md)  
 Illustra le visualizzazioni dell'albero Spy + + di windows, i messaggi, processi e thread.  
  
 [Uso di Spy++](../debugger/using-spy-increment.md)  
 Introduce lo strumento Spy + + e spiega come può essere usato.  
  
 [Finestra di dialogo Ricerca processi](../debugger/process-search-dialog-box.md)  
 Utilizzato per trovare il nodo per un determinato processo nella visualizzazione processi.  
  
 [Finestra di dialogo Proprietà processo](../debugger/process-properties-dialog-box.md)  
 Visualizza le proprietà di un processo selezionato nella visualizzazione processi.  
  
 [riferimenti per Spy++](../debugger/spy-increment-reference.md)  
 Include varie sezioni che descrivono ogni Spy + + menu e la finestra di dialogo.