---
title: Le descrizioni degli eventi | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], events
ms.assetid: 09f61652-7e16-4bb0-8055-f61a84bf384e
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 160cd1558401e488dec82e79627f306ef98e75ef
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47532777"
---
# <a name="event-descriptions"></a>Descrizioni di eventi
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [descrizioni degli eventi](https://docs.microsoft.com/visualstudio/extensibility/debugger/event-descriptions).  
  
Ogni tipo di evento ha uno scopo specifico.  
  
## <a name="events-and-the-reasons-for-their-use"></a>Gli eventi e i motivi per l'uso  
  
|event|Descrizione|  
|-----------|-----------------|  
|Attivare gli eventi del documento|Si verificano quando il motore di debug (DE) richiede l'IDE per aprire o visualizzare un documento in primo piano.|  
|Punto di interruzione associata o eventi di errore punto di interruzione|Inviato quando è associato un punto di interruzione o quando non è possibile associare un punto di interruzione e viene restituito un errore.|  
|Eventi punto di interruzione non associato|Si verificano quando un punto di interruzione associato viene disassociata dal codice.|  
|Può arrestare eventi|Inviato all'IDE per determinare se l'utente desidera arrestare in un momento specificato nel codice.|  
|Eventi punto di interruzione|Si verifica quando viene raggiunto un punto di interruzione di dati o codice.|  
|Eventi di testo di documenti|Si verifica quando viene modificato il testo in un documento. Questi eventi non vengono inviati tramite il `IDebugEventCallBack2::Event` (metodo).|  
|Motore di creare eventi|Inviato quando un motore viene inizialmente creato.|  
|Eventi punto di ingresso|Inviato quando il programma in fase di debug ha eseguito il codice di inizializzazione e raggiunto il primo punto di ingresso utente.|  
|Eventi di eccezione|Inviato quando un programma in esecuzione raggiunge un'eccezione.|  
|Eventi di completamento valutazione di espressioni|Inviato quando la valutazione dell'espressione asincrona è stata completata.|  
|Trovare gli eventi di simboli|Inviato ogni volta che la Germania deve richiedere all'utente di trovare i simboli per un modulo.|  
|Eventi di caricamento completati|Inviato solo quando il carico iniziale del programma è stato completato e il primo codice sta per eseguire il programma.|  
|Eventi dei messaggi|Inviato quando i messaggi vengono inviati agli utenti.|  
|Eventi modulo di caricamento|Inviato quando un nuovo modulo viene caricato o scaricato.|  
|Eventi di stringa di output|Inviato quando il programma scrive l'output di debug.|  
|Creare e distruggere gli eventi|Invio di annunciare la creazione o l'eliminazione di processi, programmi, proprietà, le sessioni e i thread in modo che l'IDE di Visual Studio può tenere traccia dello stato dei programmi in fase di debug.|  
|Eventi di passaggio completati|Inviato quando un passaggio è stato completato.|  
|Eventi di modifica nome thread|Inviato quando l'utente modifica il nome di un thread.|  
|Eventi di modifica nome programma|Inviato quando l'utente modifica il nome di un programma.|  
  
## <a name="see-also"></a>Vedere anche  
 [Invio di eventi](../../extensibility/debugger/sending-events.md)
