---
title: Registro modifiche (Visual Studio Tools per Unity, Mac) | Microsoft Docs
ms.custom: ''
ms.date: 11/13/2018
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: 33a6ac54-d997-4308-b5a0-af7387460849
author: therealjohn
ms.author: johmil
manager: crdun
ms.workload:
- unity
ms.openlocfilehash: 0b641c9dd1fe797fc036a6ece893ad61fc52ff87
ms.sourcegitcommit: 5c049194fa256b876ad303f491af11edd505756c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/07/2018
ms.locfileid: "53027237"
---
# <a name="change-log-visual-studio-tools-for-unity-mac"></a>Registro modifiche (Visual Studio Tools per Unity, Mac)
Registro delle modifiche di Visual Studio Tools per Unity.

## <a name="1700"></a>1.7.0.0
 Data di rilascio: 13 novembre 2018

### <a name="new-features"></a>Nuove funzionalità

-   **Debugger:**

    -   Aggiunta di altre informazioni sul client (IP, nome del computer) nella finestra di dialogo di connessione.

### <a name="bug-fixes"></a>Correzioni di bug

-   **Debugger:**

     -   Correzione di un deadlock nella libreria usata per comunicare con il motore di debugger di Unity, che blocca Visual Studio o Unity, in particolare al raggiungimento di "Collega a Unity" o al riavvio del gioco.
     
-   **Integrazione:**

     -   Correzione dell'attivazione del plug-in Unity quando veniva selezionato un altro editor predefinito.
     
     -   Correzione della creazione di un modello di file Unity.

## <a name="1602"></a>1.6.0.2
 Data di rilascio: 24 luglio 2018

### <a name="bug-fixes"></a>Correzioni di bug

-   **Integrazione:**

     -   Eseguito il rollback della soluzione alternativa per un bug delle prestazioni di Unity che è stato risolto da Unity.
     
## <a name="1601"></a>1.6.0.1
 Data di rilascio: 10 luglio 2018

### <a name="bug-fixes"></a>Correzioni di bug

-   **Integrazione:**

     -   Correzione del supporto della colorazione del codice di Shader.
     
## <a name="1600"></a>1.6.0.0
 Data di rilascio: 26 giugno 2018

### <a name="bug-fixes"></a>Correzioni di bug

-   **Procedure guidate:**

    -   Correzione di un errore ortografico per il messaggio OnApplicationFocus.

-   **Project Generation:**

     -   Soluzione alternativa temporanea per un bug delle prestazioni Unity: memorizzazione nella cache di MonoIsland durante la generazione di progetti.
     
     -   Non convertire più pdb portabili a mdb quando si usa il nuovo runtime di Unity.
     
## <a name="1502"></a>1.5.0.2
 Data di rilascio: 18 aprile 2018
 
### <a name="new-features"></a>Nuove funzionalità

-   **Integrazione:**

    -   Aggiunta del supporto per il completamento del codice Shader di base.
    
    -   Aggiunta del supporto per attivare e disattivare i commenti nei file di Shader.

## <a name="1501"></a>1.5.0.1
 Data di rilascio: 28 marzo 2018
 
### <a name="new-features"></a>Nuove funzionalità

-   **Integrazione:**

    -   Aggiunta del supporto per modelli aggiuntivi in Esplora progetti Unity.

## <a name="1500"></a>1.5.0.0
 Data di rilascio: 21 marzo 2018
 
### <a name="new-features"></a>Nuove funzionalità

-   **Integrazione:**

    -   Aggiunta del supporto per il rilevamento e la connessione a lettori Android connessi tramite USB.

## <a name="1403"></a>1.4.0.3
 Data di rilascio: 5 marzo 2018
 
### <a name="new-features"></a>Nuove funzionalità

-   **Project Generation:**

    -   Aggiunta del supporto per il nuovo generatore di progetti in Unity 2018.1.

-   **Integrazione:**

    -   Aggiunta del pannello opzioni per le impostazioni dedicate.

## <a name="1402"></a>1.4.0.2
 Data di rilascio: 24 gennaio 2018
 
### <a name="bug-fixes"></a>Correzioni di bug

-   **Project Generation:**

    -   Correzione del rilevamento della versione di Mono.

-   **Integrazione:**

    -   Correzione dei problemi di tempistica per l'attivazione di 2018.1 e plug-in.

    -   Correzione delle notifiche quando si rilevava un nuovo giocatore.

## <a name="1401"></a>1.4.0.1
 Data di rilascio: 23 gennaio 2018
 
### <a name="bug-fixes"></a>Correzioni di bug

-   **Integrazione:**

    -   Correzione delle cartelle Espandi / Comprimi con doppio clic

## <a name="1400"></a>1.4.0.0
 Data di rilascio: 13 dicembre 2017
 
### <a name="new-features"></a>Nuove funzionalità

-   **Project Generation:**

    -   Aggiunta del supporto per .NET Standard.

### <a name="bug-fixes"></a>Correzioni di bug

-   **Integrazione:**

    -   Correzione della conversione automatica dei simboli di debug da pdb a mdb.

## <a name="1301"></a>1.3.0.1
 Data di rilascio: 12 dicembre 2017
 
### <a name="bug-fixes"></a>Correzioni di bug

-   **Integrazione:**

    -   Correzione della chiamata indiretta a EditorPrefs.GetBool con effetti sul controllo durante il tentativo di modifica delle dimensioni della matrice.

-   **Procedure guidate:**

    -   Aggiornamento del contesto roslyn prima dell'inserimento del metodo.

## <a name="1300"></a>1.3.0.0
 Data di rilascio: 20 novembre 2017
 
### <a name="new-features"></a>Nuove funzionalità

-   **Procedure guidate:**

    -   Aggiunta della procedura guidata "Implement Unity message" (Implementare il messaggio di Unity).

    -   Aggiunta del supporto per la nuova API di completamento in VS per Mac 7.4.

## <a name="1200"></a>1.2.0.0
 Data di rilascio: 23 ottobre 2017
 
### <a name="new-features"></a>Nuove funzionalità

-   **Debugger:**

    -   È stato aggiunto il supporto per i file di simboli di debug portatili.

### <a name="bug-fixes"></a>Correzioni di bug

-   **Project Generation:**

    -   È stato corretto il problema dell'aggiunta di estensioni dll in eccesso al nome del file di assembly.

    -   Non forzare il flag Unity AllowAttachedDebuggingOfEditor Unity, il cui valore predefinito è ora 'true'.

## <a name="1103"></a>1.1.0.3
 Data di rilascio: 23 ottobre 2017
 
### <a name="new-features"></a>Nuove funzionalità

-   **Project Generation:**

    -   Aggiunta del supporto per il profilo .NET 4.6.

## <a name="1102"></a>1.1.0.2
 Data di rilascio: 8 agosto 2017
 
### <a name="new-features"></a>Nuove funzionalità

-   **Debugger:**

    -   Avvia il collegamento per elaborare la finestra di dialogo, se non si sa a quale Unity collegarsi.

-   **Project Generation:**

    -   Abilita sempre l'opzione di compilazione non sicura quando viene usato Unity 5.6.

## <a name="1101"></a>1.1.0.1
 Data di rilascio: 20 luglio 2017
 
### <a name="new-features"></a>Nuove funzionalità

-   **Integrazione:**

    -   Aggiunta del supporto per le risorse localizzate.

## <a name="1100"></a>1.1.0.0
 Data di rilascio: 12 luglio 2017
 
### <a name="new-features"></a>Nuove funzionalità

-   **Integrazione:**

    -   Aggiunta del supporto per la connessione ai lettori ed editor tramite la finestra Associa a processo.

-   **Project Generation:**

    -   Riferimenti ai nomi assembly di Fixed con i file mcs.rsp.

    -   Supporto aggiunto per le unità di compilazione assembly.json.    

    -   Fixed è definito con i livelli di API.    

### <a name="bug-fixes"></a>Correzioni di bug

-   **Integrazione:**

    -   Messaggio di errore shader fisso durante la compilazione.

## <a name="1001"></a>1.0.0.1
 Data di rilascio: 4 maggio 2017
 
### <a name="bug-fixes"></a>Correzioni di bug

-   **Integrazione:**

    -   Correzione della verifica dei documenti attivi con progetti regolari e ibridi.

## <a name="1000"></a>1.0.0.0
 Data di rilascio: 3 maggio 2017
