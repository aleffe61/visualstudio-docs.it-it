---
title: 'Procedura: collegare visualizzazioni ai dati documento | Microsoft Docs'
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
- editors [Visual Studio SDK], custom - attach views to document data
ms.assetid: f92c0838-45be-42b8-9c55-713e9bb8df07
caps.latest.revision: 23
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 423634a98b09af8d549442cb8f24964228496227
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47528066"
---
# <a name="how-to-attach-views-to-document-data"></a>Procedura: collegare visualizzazioni ai dati documento
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [procedura: collegare visualizzazioni ai dati documento](https://docs.microsoft.com/visualstudio/extensibility/how-to-attach-views-to-document-data).  
  
Se si dispone di una nuova visualizzazione del documento, è possibile aggiungerlo a un oggetto dati del documento esistente.  
  
### <a name="to-determine-if-you-can-attach-a-view-to-an-existing-document-data-object"></a>Per determinare se è possibile collegare una visualizzazione a un oggetto dati del documento esistente  
  
1.  Implementare <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A>.  
  
2.  Nell'implementazione di `IVsEditorFactory::CreateEditorInstance`, chiamare `QueryInterface` sull'oggetto di dati documento esistente quando si chiama l'IDE di `CreateEditorInstance` implementazione.  
  
     La chiamata `QueryInterface` consente di esaminare l'oggetto dati documento esistente, specificato nella `punkDocDataExisting` parametro.  
  
     Le interfacce esatte è necessario eseguire una query, dipende tuttavia, l'editor che viene aperto il documento, come descritto nel passaggio 4.  
  
3.  Se non si trova le interfacce appropriate nell'oggetto dati documento esistente, quindi restituire un codice di errore in un editor che indica che l'oggetto dati del documento non è compatibile con l'editor.  
  
     Nell'implementazione dell'IDE di <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A>, una finestra di messaggio che informa che il documento è aperto in un altro editor e chiede se si desidera chiuderlo.  
  
4.  Se si chiude in questo documento, Visual Studio chiama quindi la factory dell'editor per la seconda volta. In questa chiamata, il `DocDataExisting` parametro è uguale a NULL. L'implementazione della factory dell'editor può aprire quindi l'oggetto dati del documento in un editor personalizzato.  
  
    > [!NOTE]
    >  Per determinare se è possibile lavorare con un oggetto dati del documento esistente, è inoltre possibile utilizzare le informazioni private dell'implementazione dell'interfaccia eseguendo il cast di un puntatore all'effettiva [!INCLUDE[vcprvc](../includes/vcprvc-md.md)] classe dell'implementazione privata. Ad esempio, tutti gli editor standard implementano `IVsPersistFileFormat`, che eredita da <xref:Microsoft.VisualStudio.OLE.Interop.IPersist>. Di conseguenza, è possibile chiamare `QueryInterface` per <xref:Microsoft.VisualStudio.OLE.Interop.IPersist.GetClassID%2A>, e se l'ID classe oggetto dati del documento esistente corrisponde dell'implementazione di ID di classe, quindi è possibile lavorare con l'oggetto dati del documento.  
  
## <a name="robust-programming"></a>Programmazione efficiente  
 Quando Visual Studio chiama l'implementazione del <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> metodo passa nuovamente un puntatore all'oggetto dati documento esistente nel `punkDocDataExisting` parametro, se presente. Esaminare l'oggetto dati del documento restituito nella `punkDocDataExisting` per determinare se l'oggetto dati del documento è appropriato per l'editor come descritto nella nota nel passaggio 4 della procedura in questo argomento. Se è appropriato, quindi la factory dell'editor deve fornire una seconda vista per i dati come descritto nel [Supporting Multiple Document Views](../extensibility/supporting-multiple-document-views.md). In caso contrario, quindi viene visualizzato un messaggio di errore appropriato.  
  
## <a name="see-also"></a>Vedere anche  
 [Supporto di più visualizzazioni documento](../extensibility/supporting-multiple-document-views.md)   
 [Dati documento e visualizzazione documento negli editor personalizzati](../extensibility/document-data-and-document-view-in-custom-editors.md)
