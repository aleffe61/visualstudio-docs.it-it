---
title: Debug di applicazioni multithreading in Visual Studio | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.gputthreads
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- threading [Visual Studio], debugging
- debugging [Visual Studio], high-performance computing
- debugging [Visual Studio], multithreaded
- multithreaded debugging
- high-performance debugging
ms.assetid: 9d175bc2-1d95-4c47-9bc3-9755af968a9c
caps.latest.revision: 28
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f5b9ff27a8a864d648b5e9c545cee72ee64a4901
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51758434"
---
# <a name="debug-multithreaded-applications-in-visual-studio"></a>Debug di applicazioni multithreading in Visual Studio
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Un thread è una sequenza di istruzioni in base alla quale il sistema operativo esegue l'allocazione del tempo processore. Ogni processo in esecuzione nel sistema operativo è composto da almeno un thread. I processi composti da più di un thread sono detti multithreading.  
  
 I computer multiprocessore, i processori multicore e i processi hyperthreading sono in grado di eseguire contemporaneamente più thread. Se da un lato l'elaborazione parallela di più thread può migliorare notevolmente le prestazioni dei programmi, dall'altro può rendere il debug più difficoltoso poiché introduce la necessità di tenere traccia di più thread.  
  
 Il multithreading introduce inoltre nuovi tipi di possibili bug. Accade spesso, ad esempio, che due o più thread debbano accedere alla stessa risorsa, alla quale però può accedere un solo thread alla volta. Deve necessariamente esistere una qualche forma di esclusione reciproca per garantire l'accesso alla risorsa di un solo thread alla volta. Se l'esclusione reciproca viene eseguita in modo non corretto, è possibile creare un *deadlock* condizione in cui è possibile eseguire alcun thread. I deadlock possono rappresentare un problema particolarmente difficile da risolvere con il debug.  
  
 Visual Studio offre un' **thread** finestra, una finestra thread GPU, una finestra Espressioni di controllo parallelo e altre funzionalità che rendono il debug multithreading. Il modo migliore per acquisire ulteriori informazioni sulle nuove funzionalità dell'interfaccia di threading consiste nell'eseguire le procedure dettagliate. Visualizzare [procedura dettagliata: debug di un'applicazione multithreading](../debugger/walkthrough-debugging-a-multithreaded-application.md) e [procedura dettagliata: debug di un'applicazione C++ AMP](http://msdn.microsoft.com/library/40e92ecc-f6ba-411c-960c-b3047b854fb5).  
  
 Visual Studio offre anche potenti punti di interruzione e punti di analisi che possono rivelarsi molto utili per il debug di applicazioni multithreading. È possibile applicare filtri dei punti di interruzione per inserire punti di interruzione in corrispondenza di singoli thread. Vedere [usando i punti di interruzione](../debugger/using-breakpoints.md)  
  
 Il debug di un'applicazione multithreading dotata di un'interfaccia utente può essere particolarmente complesso. In tal caso, potrebbe essere necessario eseguire l'applicazione in un secondo computer e utilizzare il debug remoto. Per informazioni, vedere [debug remoto](../debugger/remote-debugging.md).  
  
## <a name="in-this-section"></a>In questa sezione  
 [Debug di thread e processi](../debugger/debug-threads-and-processes.md)  
 Vengono illustrate le nozioni fondamentali di debug di thread e processi.  
  
 [Eseguire il debug di più processi](../debugger/debug-multiple-processes.md)  
 Spiega la procedura per eseguire il debug di più processi  
  
 [Procedura: Usare la finestra Thread](../debugger/how-to-use-the-threads-window.md)  
 Procedure utili per il debug dei thread con il **thread** finestra.  
  
 [Procedura: Passare a un altro thread durante il debug](../debugger/how-to-switch-to-another-thread-while-debugging.md)  
 Tre modi per passare il contesto di debug a un altro thread.  
  
 [Procedura: Impostare e rimuovere i flag dei thread](../debugger/how-to-flag-and-unflag-threads.md)  
 Aggiunta di contrassegni o flag ai thread a cui è opportuno prestare particolare attenzione durante il debug.  
  
 [Procedura: Impostare il nome di un thread in codice nativo](../debugger/how-to-set-a-thread-name-in-native-code.md)  
 Assegnare un nome da visualizzare nel thread di **thread** finestra.  
  
 [Procedura: Impostare il nome di un thread in codice gestito](../debugger/how-to-set-a-thread-name-in-managed-code.md)  
 Assegnare un nome da visualizzare nel thread di **thread** finestra.  
  
 [Procedura dettagliata: Debug di un'applicazione multithreading](../debugger/walkthrough-debugging-a-multithreaded-application.md).  
 Presentazione guidata delle funzionalità di debug dei thread, con particolare attenzione alle funzionalità procedura [!INCLUDE[vs_orcas_long](../includes/vs-orcas-long-md.md)].  
  
 [Procedura: Eseguire il debug su un cluster ad alte prestazioni](../debugger/how-to-debug-on-a-high-performance-cluster.md)  
 Tecniche per il debug di applicazioni in esecuzione su un cluster ad alte prestazioni.  
  
 [Suggerimenti per il debug dei thread in codice nativo](../debugger/tips-for-debugging-threads-in-native-code.md)  
 Semplici tecniche utili per il debug di thread nativi.  
  
 [Uso della finestra Attività](../debugger/using-the-tasks-window.md)  
 Visualizza un elenco di tutti gli oggetti attività gestiti o nativi con il rispettivo stato e altre informazioni utili.  
  
 [Uso della finestra Stack in parallelo](../debugger/using-the-parallel-stacks-window.md)  
 Visualizza gli stack di chiamate di più thread (o attività) in un'unica visualizzazione e riunisce inoltre i segmenti dello stack comuni ai vari thread (o attività).  
  
 [Procedura dettagliata: debug di un'applicazione parallela](../debugger/walkthrough-debugging-a-parallel-application.md)  
 Procedura dettagliata che illustra come utilizzare le finestre Attività in parallelo e Stack in parallelo.  
  
 [Procedura: Usare la finestra Espressione di controllo in parallelo](../debugger/how-to-use-the-parallel-watch-window.md)  
 Controllare i valori e le espressioni in più thread.  
  
 [Procedura: Usare la finestra Thread GPU](../debugger/how-to-use-the-gpu-threads-window.md)  
 Esaminare e utilizzare i thread in esecuzione sulla GPU durante il debug.  
  
## <a name="related-sections"></a>Sezioni correlate  
 [Uso di punti di interruzione](../debugger/using-breakpoints.md)  
 -   Usare filtri dei punti di interruzione per inserire un punto di interruzione in corrispondenza di un singolo thread.  
  
- I punti di traccia consentono di tracciare l'esecuzione dei programmi senza interruzioni. Ciò può risultare utile nello studio di problemi quali i deadlock.  
  
  [Threading](http://msdn.microsoft.com/library/7b46a7d9-c6f1-46d1-a947-ae97471bba87)  
  Informazioni sul threading ed esempio di codice nella programmazione di [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)].  
  
  [Multithreading nei componenti](http://msdn.microsoft.com/library/2fc31e68-fb71-4544-b654-0ce720478779)  
  Utilizzo del multithreading nei componenti di [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)].  
  
  [Supporto del multithreading per il codice precedente (Visual C++)](http://msdn.microsoft.com/library/24425b1f-5031-4c6b-aac7-017115a40e7c)  
  Informazioni sul threading ed esempio di codice per programmatori C++ che utilizzano MFC.  
  
## <a name="see-also"></a>Vedere anche  
 [Eseguire il debug di thread e processi](../debugger/debug-threads-and-processes.md)   
 [Remote Debugging](../debugger/remote-debugging.md)



