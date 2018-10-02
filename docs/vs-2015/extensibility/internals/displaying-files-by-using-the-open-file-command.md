---
title: Visualizzazione di file usando il comando Apri File | Microsoft Docs
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
- project types, supporting Open File command
- Open File command
- persistence, supporting Open File command
ms.assetid: 4fff0576-b2f3-4f17-9769-930f926f273c
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 139eb83f2260c44a3e0f8c50868d42aca8160694
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47532581"
---
# <a name="displaying-files-by-using-the-open-file-command"></a>Visualizzazione di file tramite il comando Apri file
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [i file di visualizzazione utilizzando il comando File Apri](https://docs.microsoft.com/visualstudio/extensibility/internals/displaying-files-by-using-the-open-file-command).  
  
I passaggi seguenti descrivono come l'IDE gestisce i **Apri File** comando, che è disponibile nel **File** dal menu [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]. I passaggi descrivono anche come i progetti devono rispondere alle chiamate provenienti da questo comando.  
  
 Quando un utente fa clic il **Apri File** comando le **File** dal menu e seleziona un file dal **Apri File** si verifica il processo seguente nella finestra di dialogo.  
  
1.  Usa la tabella documenti in esecuzione, l'IDE determina se il file è già aperto in un progetto.  
  
    -   Se il file è aperto, l'IDE riemerga la finestra.  
  
    -   Se il file non è aperto, l'IDE chiama <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.IsDocumentInProject%2A> per ogni progetto per determinare quale progetto è possibile aprire il file di query.  
  
        > [!NOTE]
        >  Nell'implementazione del progetto di <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.IsDocumentInProject%2A>, fornire un valore di priorità che indica il livello in corrispondenza del quale il progetto verrà aperto il file. Vengono forniti i valori di priorità nei <xref:Microsoft.VisualStudio.Shell.Interop.VSDOCUMENTPRIORITY> enumerazione.  
  
2.  Ogni progetto risponde con un livello di priorità che indica l'importanza viene posizionato sul progetto aprire il file.  
  
3.  L'IDE Usa i criteri seguenti per determinare quale progetto apre il file:  
  
    -   Il file verrà aperto il progetto che risponde con la priorità più alta (DP_Intrinsic). Se più di un progetto risponde con la priorità, il progetto prima di rispondere apre il file.  
  
    -   Se risponde alcun progetto con la priorità più alta (DP_Intrinsic), ma tutti i progetti risponde con la priorità stesso, inferiore, il progetto attivo apre il file. Se nessun progetto è attivo, il progetto prima di rispondere apre il file.  
  
    -   Se nessun progetto attesta la proprietà del file (DP_Unsupported), il progetto file esterni si apre il file.  
  
         Se viene creata un'istanza del progetto file esterni, il progetto è sempre risponde con il valore DP_CanAddAsExternal. Questo valore indica che il progetto può aprire il file. Questo progetto viene utilizzato per ospitare i file aperti che non sono in qualsiasi altro progetto. L'elenco di elementi in questo progetto non è persistente; Questo progetto è visibile nel **Esplora soluzioni** solo quando viene usato per aprire un file.  
  
         Se il progetto file esterni non indica che è possibile aprire il file, un'istanza del progetto non è stata creata. In questo caso, l'IDE crea un'istanza del progetto file esterni e indica al progetto per aprire il file.  
  
4.  Non appena l'IDE determina che il file viene aperto il progetto, chiama il <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.OpenItem%2A> metodo su tale progetto.  
  
5.  Il progetto è quindi possibile aprire il file usando un editor specifico del progetto o un editor standard. Per altre informazioni, vedere [come: Apri editor specifici del progetto](../../extensibility/how-to-open-project-specific-editors.md) e [procedura: aprire gli editor Standard](../../extensibility/how-to-open-standard-editors.md), rispettivamente.  
  
## <a name="see-also"></a>Vedere anche  
 [Visualizzazione di file tramite l'apertura con il comando](../../extensibility/internals/displaying-files-by-using-the-open-with-command.md)   
 [Apertura e salvataggio di elementi di progetto](../../extensibility/internals/opening-and-saving-project-items.md)   
 [Procedura: aprire gli editor specifici del progetto](../../extensibility/how-to-open-project-specific-editors.md)   
 [Procedura: Aprire gli editor standard](../../extensibility/how-to-open-standard-editors.md)
