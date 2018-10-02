---
title: 'Procedura: Limitare la strumentazione a specifiche DLL | Microsoft Docs'
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
- performance tools, runtime profiling control window
ms.assetid: 17c5996f-e3d0-4e44-b175-52b401b0f2d5
caps.latest.revision: 24
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b99a67921739f620c908f1551f0f8a29a5aac73a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47517676"
---
# <a name="how-to-limit-instrumentation-to-specific-dlls"></a>Procedura: Limitare la strumentazione a specifiche DLL
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [procedura: limite di strumentazione a specifiche DLL](https://docs.microsoft.com/visualstudio/profiling/how-to-limit-instrumentation-to-specific-dlls).  
  
Usando il metodo di profilatura della strumentazione, è possibile limitare la raccolta dei dati di profilatura a una o più DLL di un'applicazione. Per profilare una o più DLL di un'applicazione, creare una sessione di prestazioni che includa i file con estensione dll come destinazioni. È possibile specificare le DLL da profilare come progetti in una soluzione di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] o come file binari indipendenti.  
  
### <a name="to-limit-instrumentation-to-specific-dlls-in-a-visual-studio-solution"></a>Per limitare la strumentazione a specifiche DLL di una soluzione di Visual Studio  
  
1.  Aprire la soluzione contenente la DLL in [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)].  
  
2.  Nel menu **Analizza** selezionare **Avvia Creazione guidata sessione di prestazioni**.  
  
3.  Scegliere **Strumentazione** come metodo di profilatura e quindi fare clic su **Avanti**.  
  
4.  In **Specificare le destinazioni da profilare** selezionare il nome del progetto con estensione dll e quindi fare clic su **Avanti**.  
  
5.  Fare clic su **Fine** per chiudere la procedura guidata e visualizzare la nuova sessione di prestazioni nella finestra **Esplora prestazioni**.  
  
6.  Fare clic con il pulsante destro del mouse su **Destinazioni** e quindi selezionare **Aggiungi progetto di destinazione**.  
  
7.  Dall'elenco **Aggiungi progetto di destinazione** selezionare il progetto eseguibile da usare per verificare la DLL.  
  
     Facoltativo. È possibile aggiungere qualsiasi progetto DLL che si vuole profilare.  
  
8.  Per impedire la raccolta di dati per un progetto aggiunto, fare clic con il pulsante destro del mouse sul nome del progetto e quindi deselezionare la casella di controllo **Strumento**.  
  
### <a name="to-specify-specific-dlls-to-profile-as-independent-binaries"></a>Per specificare determinate DLL da profilare come file binari indipendenti  
  
1.  Aprire [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)].  
  
2.  Nel menu **Analizza** selezionare **Avvia Creazione guidata sessione di prestazioni**.  
  
3.  In **Specificare le destinazioni da profilare** selezionare **Profilatura di una libreria a collegamento dinamico (.DLL)** e quindi fare clic su **Avanti**.  
  
4.  Nella seconda pagina della procedura guidata eseguire i passaggi seguenti:  
  
    -   Digitare il percorso e il nome del file con estensione dll da profilare in **Percorso DLL**. È anche possibile fare clic sul pulsante con i puntini di sospensione (...) per individuare il file nella finestra di dialogo **Libreria a collegamento dinamico da profilare**. Si noti che è necessario specificare la copia del file con estensione dll che verrà avviato dal file eseguibile (exe) che si seleziona al passaggio successivo.  
  
    -   Digitare il percorso e il nome del file eseguibile (exe) che verrà usato per verificare il file con estensione dll in **Percorso eseguibile**. È anche possibile fare clic sul pulsante con i puntini di sospensione (...) per individuare il file nella finestra di dialogo **Eseguibile da avviare**.  
  
    -   Facoltativo. Digitare gli argomenti della riga di comando da passare al file eseguibile in **Argomenti della riga di comando**. Se necessario, specificare la directory di lavoro per l'applicazione in **Directory di lavoro**.  
  
    -   Scegliere **Avanti**.  
  
5.  Scegliere **Strumentazione** come metodo di profilatura e quindi fare clic su **Avanti**.  
  
6.  Fare clic su **Fine** per chiudere la procedura guidata e visualizzare la nuova sessione di prestazioni nella finestra **Esplora prestazioni**.  
  
7.  Facoltativo. Per aggiungere altri file con estensione dll, fare clic con il pulsante destro del mouse su **Destinazioni** e quindi selezionare **Aggiungi binario di destinazione**. Selezionare i file dalla finestra di dialogo **Aggiungi binario di destinazione**.  
  
    > [!NOTE]
    >  Non specificare il file eseguibile (exe) che verifica le DLL.  
  
## <a name="see-also"></a>Vedere anche  
 [Controllo della raccolta di dati](../profiling/controlling-data-collection.md)   
 [Procedura: Limitare la strumentazione a specifiche funzioni](../profiling/how-to-limit-instrumentation-to-specific-functions.md)


