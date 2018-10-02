---
title: Informazioni sull'allocazione di memoria e i valori dei dati di durata di un oggetto | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- .NET memory profiling method
- Profiling Tools, .NET memory method
ms.assetid: a22445b3-39a6-4919-8506-2b5b0ceaf77e
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1470e8c279ac47191a8bc91182c67df19a083339
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47525700"
---
# <a name="understanding-memory-allocation-and-object-lifetime-data-values"></a>Informazioni sull'allocazione di memoria e i valori dei dati di durata di un oggetto
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [valori di dati di oggetto durata e allocazione di memoria Understanding](https://docs.microsoft.com/visualstudio/profiling/understanding-memory-allocation-and-object-lifetime-data-values).  
  
Il metodo di profilatura *Allocazione della memoria .NET* degli strumenti di profilatura di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] raccoglie informazioni sulle dimensioni e sul numero degli oggetti che sono stati creati in un'allocazione o eliminati in una Garbage Collection e informazioni aggiuntive sullo *stack di chiamate* della funzione quando si è verificato l'evento. Lo *stack di chiamate* è una struttura dinamica che archivia informazioni sulle funzioni in esecuzione nel processore.  
  
 **Requisiti**  
  
-   [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
 Il profiler della memoria interrompe il processore del computer a ogni allocazione di un oggetto .NET Framework in un'applicazione sottoposta a profilatura. Quando vengono raccolti anche dati sulla durata degli oggetti, il profiler interrompe il processore dopo ogni operazione di Garbage Collection di .NET Framework. I dati vengono aggregati per ogni funzione profilata e per ogni tipo di oggetto.  
  
## <a name="allocation-data"></a>Dati sull'allocazione  
 Quando si verifica un evento .memory, i conteggi e le dimensioni totali degli oggetti di memoria allocati o eliminati vengono incrementati.  
  
 Quando si verifica un evento di allocazione .memory, il profiler incrementa i conteggi dei campioni per ogni funzione nello stack di chiamate. Quando i dati vengono raccolti, solo una funzione nello stack di chiamate esegue il codice nel corpo della funzione. Le altre funzioni nello stack sono elementi padre nella gerarchia delle chiamate di funzioni che sono in attesa dei valori restituiti dalle funzioni che hanno chiamato.  
  
-   Per l'evento di allocazione, il profiler incrementa il conteggio dei campioni *esclusivi* della funzione che sta attualmente eseguendo le proprie istruzioni. Dato che un campione esclusivo fa anche parte del totale (*inclusivo*) dei campioni della funzione, viene incrementato anche il conteggio dei campioni inclusivi della funzione attiva.  
  
-   Il profiler incrementa il numero di campioni inclusivi di tutte le altre funzioni nello stack di chiamate.  
  
## <a name="lifetime-data"></a>Dati sulla durata  
 Il Garbage Collector di .NET Framework gestisce l'allocazione e il rilascio di memoria per l'applicazione. Per ottimizzare le prestazioni del Garbage Collector, l'heap gestito è diviso in tre generazioni: 0, 1 e 2. Il Garbage Collector del runtime archivia i nuovi oggetti nella generazione 0. Gli oggetti non raccolti vengono promossi e archiviati nelle generazioni 1 e 2.  
  
 Il Garbage Collector recupera memoria tramite la deallocazione di un'intera generazione di oggetti. Per gli oggetti creati dall'applicazione sottoposta a profilatura, la visualizzazione Durata oggetti mostra il numero e le dimensioni degli oggetti e la generazione in cui vengono recuperati.


