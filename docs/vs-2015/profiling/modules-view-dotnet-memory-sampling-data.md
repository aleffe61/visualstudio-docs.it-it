---
title: 'Visualizzazione Moduli: dati di campionamento di memoria .NET | Microsoft Docs'
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
- Modules view
ms.assetid: 9c05b51a-8382-44cf-a8f7-3fabdd2e8f1b
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f1596d85e2668090533df9021c964d6767d36b38
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47525840"
---
# <a name="modules-view---net-memory-sampling-data"></a>Visualizzazione Moduli: dati di campionamento di memoria .NET
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [visualizzazione moduli: dati di campionamento di memoria .NET](https://docs.microsoft.com/visualstudio/profiling/modules-view-dotnet-memory-sampling-data).  
  
La visualizzazione Moduli dei dati di allocazione di memoria .NET raccolti tramite il metodo di campionamento raggruppa i dati di memoria in base ai moduli eseguiti nell'esecuzione della profilatura. Ogni modulo è la radice di una struttura gerarchica. Le funzioni del modulo sono elencate sotto il nodo del modulo.  
  
 I numeri di riga dei file di origine delle istruzioni per l'allocazione di memoria vengono elencati sotto il nodo della funzione e gli indirizzi delle istruzioni che eseguono l'allocazione vengono elencati sotto il nodo della riga. I valori inclusivi ed esclusivi sono sempre gli stessi sia per i dati di riga che per quelli di istruzione.  
  
|Colonna|Descrizione|  
|------------|-----------------|  
|**Name**|Nome del modulo, della funzione, del numero di riga o dell'indirizzo dell'istruzione.|  
|**ID processo**|ID di processo (PID) dell'esecuzione della profilatura.|  
|**Nome processo**|Nome del processo.|  
|**Nome modulo**|Nome del modulo che contiene la funzione.|  
|**Percorso modulo**|Percorso del modulo.|  
|**File di origine**|File di origine che contiene la definizione per questa funzione.|  
|**Numero riga funzione**|Numero di riga dell'inizio di questa funzione nel file di origine.|  
|**Allocazioni inclusive**|- Per una funzione, il numero totale di oggetti creati dalla funzione. Il numero include gli oggetti creati in funzioni chiamate da questa funzione.<br />- Per un modulo, il numero di oggetti in un'esecuzione della profilatura che sono stati allocati durante l'esecuzione di almeno una funzione del modulo. Il numero include gli oggetti creati in funzioni chiamate dalle funzioni del modulo.<br />- Per una riga o un'istruzione, il numero totale di oggetti allocati dalla riga o dall'istruzione.|  
|**% allocazioni inclusive**|Percentuale di tutti gli oggetti allocati nell'esecuzione della profilatura che rappresentavano allocazioni inclusive del modulo, della funzione, della riga o dell'istruzione.|  
|**Allocazioni esclusive**|- Per la funzione corrente, il numero di oggetti creati durante l'esecuzione di codice del corpo della funzione, vale a dire quando la funzione si trovava in cima allo stack di chiamate. Il numero non include gli oggetti creati nelle funzioni chiamate da questa funzione.<br />- Per un modulo, la somma delle allocazioni esclusive delle funzioni nel modulo.<br />- Per una riga o un'istruzione, il numero totale di oggetti creati da questa riga o istruzione.|  
|**% allocazioni esclusive**|Percentuale di tutti gli oggetti allocati nell'esecuzione della profilatura che rappresentavano allocazioni esclusive del modulo, della funzione, della riga o dell'istruzione.|  
|**Byte inclusivi**|- Per una funzione, il numero totale di byte allocati dalla funzione. Il numero include i byte allocati nelle funzioni chiamate da questa funzione.<br />- Per un modulo, il numero di byte allocati in un'esecuzione della profilatura che sono stati allocati durante l'esecuzione di almeno una funzione del modulo. Il numero include gli oggetti creati in tutte le funzioni chiamate dalle funzioni del modulo.<br />- Per una riga o un'istruzione, il numero totale di oggetti creati dalla riga o dall'istruzione.|  
|**% byte inclusivi**|Percentuale di tutti i byte allocati nell'esecuzione della profilatura che rappresenta i byte inclusivi del modulo, della funzione, della riga o dell'istruzione.|  
|**Byte esclusivi**|- Per una funzione, il numero totale di byte allocati dalla funzione. Il numero non include i byte allocati nelle funzioni chiamate da questa funzione.<br />- Per un modulo, la somma dei byte esclusivi allocati dalle funzioni nel modulo.<br />- Per una riga o un'istruzione, il numero totale di oggetti allocati da questa riga o istruzione.|  
|**% byte esclusivi**|Percentuale di tutti i byte allocati nell'esecuzione della profilatura che rappresenta i byte esclusivi del modulo, della funzione, della riga o dell'istruzione.|  
  
## <a name="see-also"></a>Vedere anche  
 [Procedura: Personalizzare colonne della visualizzazione report](../profiling/how-to-customize-report-view-columns.md)   
 [Visualizzazione Moduli - Strumentazione](../profiling/modules-view-dotnet-memory-instrumentation-data.md)   
 [Visualizzazione Moduli](../profiling/modules-view-sampling-data.md)   
 [Visualizzazione moduli](../profiling/modules-view-instrumentation-data.md)


