---
title: Priorità di progetto | Microsoft Docs
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
- projects [Visual Studio SDK], opening items
ms.assetid: 9f707592-2fb6-4f75-9269-f6d4700a998e
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 57698e78c9228177e7f078cd725c1d4571e36d76
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47532366"
---
# <a name="project-priority"></a>Priorità di progetto
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [priorità del progetto](https://docs.microsoft.com/visualstudio/extensibility/internals/project-priority).  
  
In genere, un elemento del progetto è un membro di un solo progetto nella soluzione. Di conseguenza, l'IDE di può facilmente determinare quale progetto viene utilizzato per aprire l'elemento. Tuttavia, se un elemento è un membro di più di un progetto, l'IDE usa uno schema di priorità per determinare il migliore progetto per aprire l'elemento.  
  
 Nell'elenco seguente viene illustrato lo schema di priorità di progetto:  
  
-   Le chiamate dell'IDE di <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject2.IsDocumentInProject%2A> metodo per ogni progetto nella soluzione per determinare se il documento è un membro di tale progetto.  
  
-   Se il documento è un membro del progetto, il progetto risponde con una priorità di progetto viene assegnata in base alla relativa funzionalità di gestione di tale documento. Ad esempio, un progetto in linguaggio risponde con una priorità assoluta per i file di origine della lingua ma risponde con una priorità più bassa per un tipo di file non riconosciuto che non viene usato come parte del processo di compilazione.  
  
-   I progetti che forniscono gli editor personalizzati, specifico del progetto o le finestre di progettazione per un documento ricevono anche una priorità alta.  
  
-   Il <xref:Microsoft.VisualStudio.Shell.Interop.VSDOCUMENTPRIORITY> enumerazione fornisce valori di priorità dei documenti.  
  
-   Il progetto che specifica la priorità più elevata viene fornito il contesto per aprire il documento. Se due progetti di restituiscono i valori di uguale priorità, il progetto attivo è preferito. Se nessun progetto nella soluzione risponde che è possibile aprire il documento, l'IDE inserisce il documento nel progetto file esterni. Per altre informazioni, vedere [progetto di file esterni](../../extensibility/internals/miscellaneous-files-project.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Progetto file esterni](../../extensibility/internals/miscellaneous-files-project.md)   
 [Procedura: aprire gli editor di documenti aperti](../../extensibility/how-to-open-editors-for-open-documents.md)   
 [Aggiunta di modelli di progetto e di elemento di progetto](../../extensibility/internals/adding-project-and-project-item-templates.md)
