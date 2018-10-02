---
title: Ridenominazione di nodi della gerarchia del progetto (C++) | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- HierUtil7 sample [Visual Studio SDK], renaming project nodes
- project nodes, renaming in HierUtil7 sample
ms.assetid: cea5968e-e9f8-41a5-b068-622df542247c
caps.latest.revision: 12
manager: douge
ms.openlocfilehash: 57e647f2926452fe32b4d3975b0cd151d0fc9823
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47528575"
---
# <a name="renaming-project-hierarchy-nodes-c"></a>Ridenominazione dei nodi della gerarchia del progetto (C++)
È possibile rinominare un nodo di gerarchia di cartelle di progetto usando il framework del progetto HierUtil7 per C++ non gestito. Per altre informazioni, vedere [esempio HierUtil7](http://msdn.microsoft.com/en-us/29c15184-a70c-4813-86c2-fb1d47442d11).  
  
## <a name="expanding-the-hierarchy-node"></a>Espandere il nodo della gerarchia  
  
#### <a name="to-expand-the-hierarchy-node-and-rename-the-folder"></a>Per espandere il nodo della gerarchia e rinominare la cartella  
  
1.  Selezionare il nodo della gerarchia utilizzando il metodo seguente:  
  
    ```  
    IfFailGo(pNode->ExtExpand(EXPF_SelectItem, GUID_MacroExplorer));  
    ```  
  
     `pNode` è il contenitore di gerarchia corrispondente alla cartella e `EXPF_SelectItem` proviene il <xref:Microsoft.VisualStudio.Shell.Interop.EXPANDFLAGS> enumerazione. Il `GUID_MacroExplorer` è una costante GUID definita in vsshell. idl e viene riportato un esempio per `rguidPersistenceSlot` nella firma della funzione di `ExtExpand`, definita in Hu_node.h.  
  
    ```  
    HRESULT ExtExpand(EXPANDFLAGS expandflags, REFGUID rguidPersistenceSlot = GUID_SolutionExplorer) const;  
    ```  
  
     È possibile trovare il file Hu_node.h nella cartella \<radice di installazione > \Program Files\VSIP 8.0\EnvSDK\common\hierutil7:  
  
2.  Rinominare la cartella inserendo il comando Rinomina con <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.PostExecCommand%2A>  
  
    ```  
    IfFailGo(srpVsUIShell->PostExecCommand(&guidVSStd97, cmdidRename, 0, NULL));  
    ```  
  
     `srpVsUIShell` è un <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell> puntatore: `<IVsUIShell>``srpVsUIShell`. `guiVSStd97` è un identificatore univoco del gruppo di comandi a cui il comando `cmdidRename` appartiene, definito in Vsshlids.h.  
  
## <a name="see-also"></a>Vedere anche  
 [Creazione di tipi di progetto](../extensibility/internals/creating-project-types.md)   
 [Esempi di VSSDK](../misc/vssdk-samples.md)