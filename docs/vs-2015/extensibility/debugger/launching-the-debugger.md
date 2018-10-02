---
title: L'avvio del Debugger | Microsoft Docs
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
- debugging [Debugging SDK], launching the debugger
- debugger [Debugging SDK], launching
ms.assetid: f24da1a1-f923-48b4-989f-18a22b581d1b
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f2a427825fdc10811fccc10ddc71438b406ebd5b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47518796"
---
# <a name="launching-the-debugger"></a>Avvio del debugger
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [l'avvio del Debugger](https://docs.microsoft.com/visualstudio/extensibility/debugger/launching-the-debugger).  
  
L'avvio del debugger richiede l'invio di sequenza corretta di metodi ed eventi con i relativi attributi appropriati.  
  
## <a name="sequences-of-methods-and-events"></a>Sequenze di metodi ed eventi  
  
1.  Gestore di sessione di debug (SDM) viene chiamato, scegliendo la **eseguire il Debug** menu e quindi selezionando **avviare**. Visualizzare [avviando un programma](../../extensibility/debugger/launching-a-program.md) per altre informazioni.  
  
2.  Le chiamate SDM [OnAttach](../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md) (metodo).  
  
3.  In base al modello di processo (DE) del motore di debug, il `IDebugProgramNodeAttach2::OnAttach` metodo restituisce uno dei metodi seguenti, che determina ciò che accade.  
  
     Se `S_FALSE` viene restituito, il motore di debug (DE) deve essere caricato in fase di macchina virtuale.  
  
     oppure  
  
     Se `S_OK` viene restituito, è la Germania da caricare in-process del messaggio SDM. Il modello SDM esegue quindi le attività seguenti:  
  
    1.  Le chiamate [GetEngineInfo](../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md) per ottenere le informazioni del motore della DE.  
  
    2.  CO-crea il DE.  
  
    3.  Le chiamate [collegare](../../extensibility/debugger/reference/idebugengine2-attach.md).  
  
4.  L'invio di DE un' [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) per il modello SDM con un `EVENT_SYNC` attributo.  
  
5.  L'invio di DE un' [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) per il modello SDM con un `EVENT_SYNC` attributo.  
  
6.  L'invio di DE un' [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) per il modello SDM con un `EVENT_SYNC` attributo.  
  
7.  L'invio di DE un' [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) per il modello SDM con un `EVENT_SYNC` attributo.  
  
8.  L'invio di DE un' [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) per il modello SDM con un `EVENT_SYNC` attributo.  
  
## <a name="see-also"></a>Vedere anche  
 [Chiamare gli eventi del Debugger](../../extensibility/debugger/calling-debugger-events.md)   
 [Avvio di un programma](../../extensibility/debugger/launching-a-program.md)
