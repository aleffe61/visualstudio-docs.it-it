---
title: Debug cronologico | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 7cc5ddf2-2f7c-4f83-b7ca-58e92e9bfdd2
caps.latest.revision: 9
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d43e48b67cdbfabcb38703469f8570f78336dcab
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51794595"
---
# <a name="historical-debugging"></a>Debug cronologico
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Il debug cronologico è una modalità di debug che dipende dalle informazioni raccolte da IntelliTrace. Consente di tornare indietro e avanti l'esecuzione dell'applicazione e controllare lo stato.  
  
 È possibile utilizzare IntelliTrace in Visual Studio Enterprise edition (ma non le edizioni Professional o Community).  
  
## <a name="why-use-historical-debugging"></a>Perché utilizzare il debug cronologico?  
 Impostazione di punti di interruzione per individuare i bug può essere una questione piuttosto hit-or-miss. È possibile impostare un punto di interruzione simile al punto nel codice in cui si ritiene che il bug sia quindi eseguire l'applicazione nel debugger e spero che il punto di interruzione ottiene accesso e il luogo in cui l'esecuzione si interrompe è in grado di rivelare l'origine del bug. In caso contrario, sarà necessario provare a impostare un punto di interruzione in un'altra posizione nel codice ed eseguire nuovamente il debugger, eseguire i passi del test più volte fino a individuare il problema.  
  
 ![impostare un punto di interruzione](../debugger/media/breakpointprocesa.png "BreakpointProcesa")  
  
 È possibile utilizzare IntelliTrace e il debug cronologico portati in giro nell'applicazione e controllare lo stato (stack di chiamate e le variabili locali) senza dover impostare punti di interruzione, riavviare il debug e ripetere i passi del test. Ciò consente di risparmiare molto tempo, soprattutto quando il bug si trova approfondita in uno scenario di test che richiede molto tempo per eseguire.  
  
## <a name="how-do-i-start-using-historical-debugging"></a>Come iniziare a utilizzare il debug cronologico?  
 IntelliTrace è attivato per impostazione predefinita. È sufficiente è decidere quali eventi e chiamate di funzione sono di interesse. Per altre informazioni sulla definizione di ciò che si desidera cercare, vedere [funzionalità IntelliTrace](../debugger/intellitrace-features.md). Per un account dettagliato di debug con IntelliTrace, vedere [procedura dettagliata: utilizzo di IntelliTrace](../debugger/walkthrough-using-intellitrace.md).  
  
## <a name="navigating-your-code-with-historical-debugging"></a>Esplorazione del codice con il debug cronologico  
 Iniziamo con un semplice programma che dispone di un bug. Aggiungere il codice seguente al file App.xaml.cs nell'applicazione:  
  
```csharp  
static void Main(string[] args)  
{  
    int testInt = 0;  
    int resultInt = AddAll(testInt);  
    Console.WriteLine(resultInt);  
}  
private static int AddAll(int j)  
{  
    for (int i = 0; i < 20; i++)  
    {  
        j = AddInt(j);  
    }  
    return j;  
}  
  
private static int AddInt(int add)  
{  
    if (add == 10)  
    {  
        return add += 25;  
    }  
    return ++add;  
}  
```  
  
 Si presuppone che il valore previsto di `resultInt` dopo la chiamata `AddAll()` è pari a 20 (il risultato di incremento `testInt` 20 volte). (Si presuppone inoltre che non è possibile visualizzare i bug in `AddInt()`). Ma il risultato è effettivamente 44. Come è possibile individuare i bug senza scorrere `AddAll()` 10 volte? È possibile utilizzare il debug cronologico per individuare l'errore in modo più semplice e rapido. Ecco come fare:  
  
1. In Strumenti / opzioni / IntelliTrace / generale, verificare che IntelliTrace è abilitato e selezionare gli eventi di IntelliTrace e chiamare l'opzione di informazioni. Se non si seleziona questa opzione, non sarà in grado di visualizzare la barra di navigazione (come illustrato di seguito).  
  
2. Impostare un punto di interruzione su `Console.WriteLine(resultInt);` linea  
  
3. Avviare il debug. Il codice viene eseguito fino al punto di interruzione. Nel **variabili locali** finestra, è possibile notare che il valore di `resultInt` è 44.  
  
4. Aprire il **strumenti di diagnostica** finestra (**Debug / Mostra strumenti di diagnostica**). La finestra codici dovrebbe risultare simile alla seguente:  
  
    ![Finestra del codice nel punto di interruzione](../debugger/media/historicaldebuggingbreakpoint.png "HistoricalDebuggingBreakpoint")  
  
5. Verrà visualizzata una doppia freccia accanto al margine sinistro, appena sopra il punto di interruzione. Quest'area viene chiamata la barra di navigazione e viene utilizzata per il debug cronologico. Fare clic sulla freccia.  
  
    Nella finestra del codice, si noterà che la riga di codice precedente (`int resultInt = AddIterative(testInt);`) è di colore rosa. Sopra la finestra, si noterà un messaggio che ci si trova nel debug cronologico.  
  
    La finestra del codice è ora simile al seguente:  
  
    ![finestra del codice in modalità debug cronologico](../debugger/media/historicaldebuggingback.png "HistoricalDebuggingBack")  
  
6. A questo punto è possibile eseguire le istruzioni il `AddAll()` metodo (**F11**, oppure il **Esegui istruzione** pulsante nella barra di navigazione. Passo avanti (**F10**, o **passare alla prossima connessione** nella barra di navigazione. La riga rosa contiene ora il `j = AddInt(j);` riga. **F10** in questo caso non esegue le istruzioni per la riga successiva del codice. Al contrario, i passaggi per la successiva chiamata di funzione. Il debug cronologico consente di passare da una chiamata a altra e ignora le righe di codice che non includono una chiamata di funzione.  
  
7. Eseguire un'istruzione nel metodo `AddInt()` Verrà visualizzato immediatamente il bug nel codice.  
  
   Questa procedura solo un assaggio delle operazioni eseguibili con il debug cronologico. Per altre informazioni sulle diverse impostazioni e gli effetti dei diversi pulsanti nella barra di navigazione, vedere [funzionalità IntelliTrace](../debugger/intellitrace-features.md).





