---
title: Architettura plug-in del controllo di origine | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- source control plug-ins, architecture
ms.assetid: 35351d4c-9414-409b-98fc-f2023e2426b7
caps.latest.revision: 25
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c7ded33f6296d9ddb0b87a3d2916a95249169f82
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51805210"
---
# <a name="source-control-plug-in-architecture"></a>Architettura dei plug-in del controllo del codice sorgente
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

È possibile aggiungere il supporto del controllo di origine per il [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] ambiente di sviluppo integrato (IDE) che implementa e collegando un plug-in del controllo del codice sorgente. L'IDE si connette il controllo del codice sorgente del plug-in tramite l'API dei plug-in del controllo origine ben definito. L'IDE espone la funzionalità controllo della versione del sistema di origine, fornendo un'interfaccia utente (UI) che include le barre degli strumenti e comandi di menu. Il plug-in del controllo del codice sorgente implementa la funzionalità di controllo di origine.  
  
## <a name="source-control-plug-in-resources"></a>Risorse di plug-in controllo di origine  
 Il plug-in controllo di origine fornisce le risorse che consentono di creare e connettere l'applicazione di controllo delle versioni per il [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE. Il plug-in controllo di origine contiene la specifica API che deve essere implementata da un plug-in del controllo del codice sorgente in modo che può essere integrato nel [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE. Contiene anche un esempio di codice, scritto in C++, che implementa una struttura del plug-in consentono di illustrare le implementazione del controllo delle funzioni essenziali conforme con l'API dei plug-in del controllo origine.  
  
 La specifica API dei plug-in del controllo origine consente di sfruttare qualsiasi controllo del codice sorgente di propria scelta se si crea un controllo del codice sorgente DLL con il set di funzioni implementati in conformità con l'API dei plug-in del controllo sorgente richiesto.  
  
## <a name="components"></a>Componenti  
 Il pacchetto di scheda di controllo codice sorgente nel diagramma è il componente dell'IDE che traduce la richiesta dell'utente per un'operazione di controllo del codice sorgente in una chiamata di funzione supportata per il plug-in del controllo del codice sorgente. A tale scopo, l'IDE e il plug-in del controllo del codice sorgente devono avere una finestra di dialogo efficace che passa informazioni avanti e indietro tra l'IDE e il plug-in. Per questa finestra di dialogo per l'implementazione, entrambi devono utilizzano la stessa lingua. L'API dei plug-in del controllo origine descritti in questa documentazione è il vocabolario comune per tale scambio.  
  
 ![Diagramma dell'architettura di controllo codice sorgente](../../extensibility/internals/media/vs-sccsdk-plug-in-arch.gif "vs_sccsdk_plug_in_arch")  
Diagramma dell'architettura con plug-in dell'interazione tra Visual Studio e controllo del codice sorgente  
  
 Come illustrato nel diagramma dell'architettura, la [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] shell, etichettata come shell di Visual Studio nel diagramma, ospita i componenti associati, ad esempio l'Editor ed Esplora soluzioni e progetti di lavoro dell'utente. Il pacchetto di scheda di controllo codice sorgente gestisce l'interazione tra l'IDE e il plug-in del controllo del codice sorgente. Il pacchetto di scheda di controllo codice sorgente fornisce il proprio controllo del codice sorgente dell'interfaccia utente. È l'interfaccia utente di primo livello che interagisce con l'utente allo scopo di avviare e definire l'ambito di un'operazione di controllo del codice sorgente.  
  
 Il plug-in del controllo del codice sorgente può avere la propria interfaccia utente, che può essere costituito da due parti come illustrato nella figura. La casella "Fornitore dell'interfaccia utente" rappresenta elementi dell'interfaccia utente personalizzata specificata dall'utente, un autore del plug-in del controllo origine. I requisiti vengono visualizzati direttamente dal controllo del codice sorgente del plug-in quando l'utente richiama un'operazione di controllo avanzate di origine. La casella "Supporto dell'interfaccia utente" è un set di plug-in dell'interfaccia utente funzionalità di controllo sorgente indirettamente richiamati tramite l'IDE. Il plug-in del controllo del codice sorgente passa i messaggi dell'interfaccia utente correlati all'IDE tramite funzioni speciali di callback fornita dall'IDE. L'interfaccia utente del supporto facilita un'integrazione più affidabile con l'IDE (spesso tramite l'uso di un' **avanzate** pulsante) e pertanto offre un'esperienza utente finale più unificata.  
  
 Un plug-in del controllo del codice sorgente non può apportare modifiche per il [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] della shell e, di conseguenza, per il pacchetto di scheda di controllo codice sorgente o l'origine di controllo dell'interfaccia utente fornita dall'IDE. È necessario apportare utilizzo massimo della flessibilità offerta tramite l'implementazione delle diverse funzioni API dei plug-in del controllo origine che contribuiscono a un'esperienza integrata per l'utente finale. La sezione di riferimento della documentazione API dei plug-in del controllo origine include informazioni per alcune funzionalità di plug-in del controllo origine avanzate. Per sfruttare queste funzionalità, il plug-in del controllo del codice sorgente deve dichiarare le funzionalità avanzate per l'IDE durante l'inizializzazione e deve implementare le funzioni avanzate specifiche per ogni funzionalità.  
  
## <a name="see-also"></a>Vedere anche  
 [Plug-in controllo codice sorgente](../../extensibility/source-control-plug-ins.md)   
 [Glossario](../../extensibility/source-control-plug-in-glossary.md)   
 [Creazione di un plug-in del controllo del codice sorgente](../../extensibility/internals/creating-a-source-control-plug-in.md)

