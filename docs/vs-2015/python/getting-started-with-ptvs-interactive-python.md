---
title: 'Introduzione a PTVS: Python interattivo | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-python
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: fa594314-bdd0-4da5-874a-57b03414b675
caps.latest.revision: 5
author: kraigb
ms.author: kraigb
manager: ghogen
ms.openlocfilehash: 7d9438d7d80480349dd53384c2538742a22b4d36
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49183911"
---
# <a name="getting-started-with-ptvs-interactive-python"></a>Introduzione a PTVS: Python interattivo
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

I prompt o i cicli REPL (read-eval-print) interattivi sono uno strumento chiave per i linguaggi di programmazione produttivi,  che consentono di eseguire frammenti di codice per rilevare ed esaminare le API, sperimentare con il relativo uso e sviluppare in maniera interattiva codice di funzionamento da includere in progetti o programmi.  
  
 È possibile seguire queste istruzioni in un brevissimo [video di youtube](https://www.youtube.com/watch?v=yc2CROtTsC0&index=5&list=PLReL099Y5nRdLgGAdrb_YeTdEnd23s6Ff).  
  
 Nella finestra Python Environments è visibile un elenco di tutti gli ambienti Python.  È possibile selezionarne uno per aprire una finestra interattiva o REPL.  Se è mai stato eseguito Python.exe in un prompt dei comandi si conosce già un REPL di Python.  Alla richiesta di REPL, si immette il codice e si preme Invio: in tal modo, verranno immediatamente visualizzati i risultati del codice.  Si tratta di un contesto di esecuzione attiva che include gli stati di tutte le esecuzioni, le assegnazioni variabili, ecc.  È possibile fare riferimento alle variabili che contengono risultati nei successivi invii al prompt REPL.  È possibile scrivere più righe di codice ed eseguirle in una sola volta (ad esempio, una dichiarazione di metodo o più istruzioni).  
  
 REPL rappresenta un modo eccezionale per provare una nuova libreria.  È possibile importare la libreria, esaminare i sottopacchetti, le classi e le funzioni.  Python offre tutte queste informazioni tramite la relativa funzione `help()`.  Inoltre, Python Tools for Visual Studio (PTVS) offre suggerimenti e documentazione basati sui modelli di codice usati nell'editor, senza dover eseguire la libreria.  Quando si esegue il codice, PTVS usa informazioni dal runtime di Python per migliorare i suggerimenti di PTVS.  
  
 La Finestra interattiva è utile anche per lo sviluppo di codice iterativo o evolutivo, incluso il test del codice durante il relativo sviluppo.  È possibile selezionare una funzione in una finestra dell'editor, premere il pulsante del puntatore a destra e scegliere Invia a Interactive.  Questo comando copia la selezione nella finestra interattiva come input successivo e la esegue.  I risultati vengono visualizzati immediatamente.  Se è necessario apportare modifiche a input precedente, è possibile premere freccia su per ottenere il codice, modificarlo, quindi premere Ctrl + INVIO per eseguire il codice.  Premendo INVIO alla fine dell'input viene eseguito, ma premendo INVIO al centro del'input viene inserita un carattere di nuova riga.  
  
 È possibile aprire una finestra interattiva per ogni installazione di Python, senza alcun limite.  Nella parte superiore della finestra sono disponibili dei pulsante per cancellare la schermata, reimpostare il contesto di esecuzione, ecc.  La cronologia rimarrà invariata.  
  
 È possibile seguire queste istruzioni in un brevissimo [video di youtube](https://www.youtube.com/watch?v=yc2CROtTsC0&index=5&list=PLReL099Y5nRdLgGAdrb_YeTdEnd23s6Ff).  
  
## <a name="see-also"></a>Vedere anche  
 [Documentazione wiki](https://github.com/Microsoft/PTVS/wiki/Interactive-REPL)   
 [Video introduttivi e dettagliati su PTVS](https://www.youtube.com/playlist?list=PLReL099Y5nRdLgGAdrb_YeTdEnd23s6Ff)

