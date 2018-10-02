---
title: Implementazione della gestione dei comandi per annidati progetti | Microsoft Docs
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
- nested projects, implementing command handling
ms.assetid: 48a9d66e-d51c-4376-a95a-15796643a9f2
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ea27ea6f1b1ef49174b555fb9b1aae0d4c54dd23
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47540700"
---
# <a name="implementing-command-handling-for-nested-projects"></a>Implementazione della gestione dei comandi per i progetti annidati
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [implementazione di gestione di comando per i progetti annidati](https://docs.microsoft.com/visualstudio/extensibility/internals/implementing-command-handling-for-nested-projects).  
  
L'IDE può passare i comandi che vengono passati tramite il <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> e il <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> interfacce per i progetti annidati o i progetti padre è possono filtrare o ignorare i comandi.  
  
> [!NOTE]
>  È possibile filtrare solo i comandi in genere gestiti dal progetto padre. Comandi, ad esempio **compilare** e **Distribuisci** che vengono gestiti dagli IDE non può essere filtrato.  
  
 I passaggi seguenti descrivono il processo per implementare la gestione dei comandi.  
  
## <a name="procedures"></a>Procedure  
  
#### <a name="to-implement-command-handling"></a>Per implementare la gestione dei comandi  
  
1.  Quando l'utente seleziona un nodo o un progetto annidato in un progetto annidato:  
  
    1.  Le chiamate dell'IDE di <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> (metodo).  
  
     oppure  
  
    1.  Se il comando ha avuto origine in una finestra della gerarchia, ad esempio un comando di menu di scelta rapida in Esplora soluzioni nell'IDE chiama il <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand%2A> metodo sull'elemento padre del progetto.  
  
2.  Il progetto padre è possibile esaminare i parametri da passare al `QueryStatus`, ad esempio `pguidCmdGroup` e `prgCmds`, per determinare se il progetto padre deve filtrare i comandi. Se il progetto principale viene implementato per filtrare i comandi, è necessario impostare:  
  
    ```  
    prgCmds[0].cmdf = OLECMDF_SUPPORTED;  
    // make sure it is disabled  
    prgCmds[0].cmdf &= ~MSOCMDF_ENABLED;  
    ```  
  
     Il progetto padre deve restituire `S_OK`.  
  
     Se il progetto principale non filtra il comando, deve semplicemente restituire `S_OK`. In questo caso, l'IDE indirizza automaticamente il comando al progetto figlio.  
  
     Il progetto padre non è disponibile eseguire il comando al progetto figlio. L'IDE esegue questa attività...  
  
## <a name="see-also"></a>Vedere anche  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy>   
 [I comandi, menu e barre degli strumenti](../../extensibility/internals/commands-menus-and-toolbars.md)   
 [Annidamento dei progetti](../../extensibility/internals/nesting-projects.md)
