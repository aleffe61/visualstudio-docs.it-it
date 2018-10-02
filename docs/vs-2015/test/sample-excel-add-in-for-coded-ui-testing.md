---
title: Componente aggiuntivo di Excel di esempio per i test codificati dell'interfaccia utente | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- coded UI tests, Excel Add-in sample
ms.assetid: 2cd52d1a-4c35-43ca-8a84-9c79dabd907f
caps.latest.revision: 18
ms.author: gewarren
manager: douge
ms.openlocfilehash: 0f0b4211b51940564041fab5777d6594168e1329
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47529479"
---
# <a name="sample-excel-add-in-for-coded-ui-testing"></a>Componente aggiuntivo di Excel di esempio per i test codificati dell'interfaccia utente
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [esempio di componente aggiuntivo per Excel per il test codificato dell'interfaccia utente](https://docs.microsoft.com/visualstudio/test/sample-excel-add-in-for-coded-ui-testing).  
  
Questo componente aggiuntivo di esempio per [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)] è specificamente progettato per supportare i test codificati dell'interfaccia utente dei fogli di lavoro di Excel registrati ed eseguiti in Visual Studio Enterprise. Per creare il componente aggiuntivo, si usa Visual Studio Tools per Office.  
  
 Per altre informazioni su come creare un componente aggiuntivo di Excel, vedere [Procedura dettagliata: Creazione del primo componente aggiuntivo VSTO per Excel](http://msdn.microsoft.com/library/a855e2be-3ecf-4112-a7f5-ec0f7fad3b5f) o cercare "componente aggiuntivo Excel" in MSDN.  
  
 Anche se il componente aggiuntivo per Excel non è l'argomento principale di questi documenti sull'estensione dei test codificati dell'interfaccia utente per Excel, alcuni commenti possono essere utili.  
  
 Parti importanti di questo componente aggiuntivo:  
  
-   Classe `ThisAddIn`: gestisce il canale Servizi remoti .NET tra `ExcelUICommunicator` e l'[estensione di esempio per i test codificati dell'interfaccia utente per Excel](../test/sample-coded-ui-test-extension-for-excel.md).  
  
-   `ExcelCodedUIAddinHelper_TemporaryKey.pfx`: certificato di sicurezza per il test del componente aggiuntivo.  
  
-   Classe `ExcelUICommunicator`: questa classe implementa l'interfaccia `IExcelUICommunication`.  
  
## <a name="thisaddin-class"></a>Classe ThisAddIn  
 La maggior parte degli elementi di questa classe viene effettivamente generata da Visual Studio Tools per Office nel file `ThisAddIn.Designer.cs` quando si crea il progetto Componente aggiuntivo di Excel.  
  
 I membri che è necessario implementare sono i gestori eventi: `ThisAddIn_Startup()` e `ThisAddIn_Shutdown()`, il cui scopo è inizializzare o chiudere il canale Servizi remoti .NET usato da `ExcelUICommunicator`.  
  
## <a name="excelcodeduiaddinhelpertemporarykeypfx"></a>ExcelCodedUIAddinHelper_TemporaryKey.pfx  
 Questo file contiene un certificato di sicurezza temporaneo che viene generato da Visual Studio Tools per Office e concede all'assembly del componente aggiuntivo l'autorizzazione per operare nel processo di Excel per il test del componente aggiuntivo e dell'estensione. È consigliabile eliminare questo certificato e crearne uno nuovo nella scheda **Firma** della finestra **Proprietà** del progetto. In alternativa, associare il proprio certificato di test.  
  
## <a name="exceluicommunicator-class"></a>Classe ExcelUICommunicator  
 Questa classe implementa l'interfaccia `IExcelUITestCommunication` e ottiene dal modello a oggetti di Excel le informazioni dell'interfaccia utente richieste. Per altre informazioni, vedere [Interfaccia Excel Communicator di esempio](../test/sample-excel-communicator-interface.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Estensione di test codificati dell'interfaccia utente e registrazioni delle azioni per supportare Microsoft Excel](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)   
 [Procedura dettagliata: Creazione del primo componente aggiuntivo VSTO per Excel](http://msdn.microsoft.com/library/a855e2be-3ecf-4112-a7f5-ec0f7fad3b5f)   
 [Sviluppo di Office e SharePoint](http://msdn.microsoft.com/library/2ddec047-263a-4901-a54c-a15fc8472329)


