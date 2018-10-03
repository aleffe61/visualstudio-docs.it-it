---
title: 'Procedura: usare la finestra moduli | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.modules
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Modules window
- Modules window
- executable files, displaying while debugging
- debugging [Visual Studio], displaying modules
- DLLs, displaying while debugging
- modules, displaying
ms.assetid: d840fdca-b035-4452-b652-72580c831896
caps.latest.revision: 41
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4f7a5c71a95c0e4c366b7001a3adf86d5bacc9c8
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47525569"
---
# <a name="how-to-use-the-modules-window"></a>Procedura: utilizzare la finestra Moduli
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [visualizzare i moduli, le DLL e file eseguibili nel Debugger](https://docs.microsoft.com/visualstudio/debugger/how-to-use-the-modules-window).  
  
NOTA]
>  Questa funzionalità non è disponibile per il debug di script o SQL.  
  
 Il **moduli** finestra sono elencate le DLL ed EXE che vengono utilizzati dal programma e Visualizza informazioni rilevanti per ognuno.  
  
### <a name="to-display-the-modules-window-in-break-mode-or-in-run-mode"></a>Per visualizzare la finestra Moduli in modalità di interruzione o di esecuzione  
  
-   Nel **Debug** menu, scegliere **Windows**e quindi fare clic su **moduli**.  
  
     Per impostazione predefinita, il **moduli** finestra sono ordinati in base all'ordine di caricamento. È tuttavia possibile ordinare i moduli in base a qualsiasi colonna.  
  
### <a name="to-sort-by-any-column"></a>Per eseguire l'ordinamento in base a una colonna  
  
-   Fare clic sul pulsante nella parte superiore della colonna.  
  
     È possibile caricare i simboli o specificare un percorso simboli dal **moduli** finestra usando il menu di scelta rapida.  
  
## <a name="loading-symbols"></a>Caricamento dei simboli  
 Nel **moduli** finestra, è possibile vedere quali moduli sono caricati i simboli di debug. Queste informazioni sono visualizzate le **stato simboli** colonna. Se lo stato è indicato **Skipped loadingCannot trovare o aprire il file PDB**, o **caricamento disabilitato dall'impostazione include/exclude**, è possibile usare il debugger per scaricare i simboli dai simboli pubblici Microsoft i server o per caricare i simboli da una directory di simboli nel computer. Per altre informazioni, vedere [specifica simboli (PDB) e i file di origine](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)  
  
#### <a name="to-load-symbols-manually"></a>Per caricare i simboli manualmente  
  
1.  Nel **moduli** finestra, pulsante destro del mouse un modulo per il quale non sono stati caricati i simboli.  
  
2.  Puntare **Carica simboli da** e quindi fare clic su **server dei simboli Microsoft** oppure **percorso dei simboli**.  
  
#### <a name="to-change-symbol-load-settings"></a>Per modificare le impostazioni di caricamento dei simboli  
  
1.  Nel **moduli** finestra, fare doppio clic su qualsiasi modulo MSIL.  
  
2.  Fare clic su **delle impostazioni dei simboli**.  
  
     È ora possibile modificare le impostazioni di caricamento di simboli, come descritto in [specificare i percorsi dei simboli e il comportamento di caricamento](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md#BKMK_Specify_symbol_locations_and_loading_behavior). Riavviare la sessione di debug per rendere effettive le modifiche.  
  
#### <a name="to-change-symbol-load-behavior-for-a-specific-module"></a>Per modificare il comportamento di caricamento dei simboli per un modulo specifico  
  
1.  Nel **moduli** finestra, fare clic sul modulo.  
  
2.  Puntare **impostazioni caricamento automatico simboli** e quindi fare clic su **Carica sempre manualmente** oppure **predefinito**. Riavviare la sessione di debug per rendere effettive le modifiche.  
  
## <a name="see-also"></a>Vedere anche  
 [Interruzione dell'esecuzione](http://msdn.microsoft.com/en-us/30fc4643-f337-4651-b1ff-f2de2c098d40)   
 [Visualizzazione dei dati nel Debugger](../debugger/viewing-data-in-the-debugger.md)   
 [Specificare file di simboli (PDB) e di origine](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)




