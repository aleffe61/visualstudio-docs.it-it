---
title: 'Errore: La valutazione della funzione &#39;funzione&#39; scaduta e deve essere interrotta in modo non protetto | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.unsafe_func_eval_abort
ms.assetid: 0a9f70ed-21ad-4a10-8535-b9c5885ad8f4
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b78d4b8f433c925521a978ab5c3a5076f329c407
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47528881"
---
# <a name="error-evaluating-the-function-39function39-timed-out-and-needed-to-be-aborted-in-an-unsafe-way"></a>Errore: La valutazione della funzione &#39;funzione&#39; scaduta e deve essere interrotta in modo non sicuro
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [errore: la valutazione della funzione &#39;funzione&#39; verificato il timeout e deve essere interrotta in modo non sicuro](https://docs.microsoft.com/visualstudio/debugger/error-evaluating-the-function-function-timed-out-and-needed-to-be-aborted-in-an-unsafe-way).  
  
Testo del messaggio completo: la valutazione della funzione 'function' scaduta e deve essere interrotta in modo non sicuro. Ciò potrebbe essere danneggiata il processo di destinazione. 

Per renderne più semplice controllare lo stato degli oggetti .NET, il debugger automaticamente forzerà il proseguimento del processo per eseguire codice aggiuntivo (in genere i metodi di richiamo di proprietà e funzioni di ToString). In molti scenari tutte queste funzioni vengono completate rapidamente e semplificare il debug. Tuttavia, il debugger non viene eseguita l'applicazione in un ambiente sandbox. Di conseguenza, un getter della proprietà o metodo ToString che chiama una funzione nativa che si blocca può causare timeout long che potrebbero non essere ripristinabili. Se si verifica questo messaggio di errore, ciò è accaduto.
 
Un motivo comune per questo problema è che quando il debugger valuta una proprietà, consente solo il thread in esame per l'esecuzione. Pertanto, se la proprietà è in attesa di altri thread da eseguire all'interno dell'applicazione sottoposta a debug e se è in attesa in modo che il Runtime .NET non è in grado di interrompere, verrà eseguito questo problema.
 
## <a name="to-correct-this-error"></a>Per correggere l'errore
 
Esistono tre possibili soluzioni al problema.
 
### <a name="solution-1-prevent-the-debugger-from-calling-the-getter-property-or-tostring-method"></a>Soluzione #1: Impedire il debugger di chiamare la proprietà getter o il metodo ToString
 
Il messaggio di errore indicherà il nome della funzione di cui che il debugger ha tentato di chiamare. Se è possibile modificare questa funzione, è possibile impedire al debugger di chiamare il getter della proprietà o il metodo ToString. Provare una delle operazioni seguenti:
 
* Modificare il metodo in un altro tipo di codice diverso da un getter della proprietà o metodo ToString e il problema non viene più visualizzato.
    oppure
* (Per ToString) Definire un attributo DebuggerDisplay sul tipo e sarà possibile utilizzare il debugger di valutare un valore diverso da ToString.
    oppure
* (Per un getter proprietà) Inserire il `[System.Diagnostics.DebuggerBrowsable(DebuggerBrowsableState.Never)]` attributo della proprietà. Ciò può essere utile se si dispone di un metodo che deve rimanere una proprietà per motivi di compatibilità delle API, ma deve essere effettivamente un metodo.
 
### <a name="solution-2-have-the-target-code-ask-the-debugger-to-abort-the-evaluation"></a>Soluzione #2: Impostare il codice di destinazione venga richiesto del debugger per interrompere la valutazione
 
Il messaggio di errore indicherà il nome della funzione di cui che il debugger ha tentato di chiamare. Se il getter della proprietà o metodo ToString a volte non viene eseguita correttamente, specialmente in situazioni in cui il problema è che un altro thread per eseguire il codice è necessario codice e quindi possa chiamare la funzione di implementazione `System.Diagnostics.Debugger.NotifyOfCrossThreadDependency` chiedere il debugger per interrompere la funzione siano stati soddisfacenti. Con questa soluzione, è comunque possibile valutare in modo esplicito queste funzioni, ma il comportamento predefinito prevede che l'esecuzione si arresta quando si verifica alla chiamata NotifyOfCrossThreadDependency.
 
### <a name="solution-3-disable-all-implicit-evaluation"></a>Soluzione #3: Disabilitare tutte le valutazione implicita
 
Se le soluzioni precedenti non risolvono il problema, passare a *degli strumenti* / *opzioni*e deselezionare l'impostazione *debug*  /   *Generali* / *Abilita valutazione delle proprietà e altre chiamate di funzioni implicite*. Questo verrà disabilitata la maggior parte delle valutazioni di funzioni implicite e dovrebbe risolvere il problema.



  



