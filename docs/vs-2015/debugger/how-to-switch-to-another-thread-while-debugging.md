---
title: 'Procedura: passare a un altro Thread durante il debug | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- threads, switching [debugging]
ms.assetid: 5cd76c52-76fa-4fcc-b37e-e9f0ecac0e9e
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ad13c81afc82ac69055ae117c862a1cf73b51478
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51737705"
---
# <a name="how-to-switch-to-another-thread-while-debugging"></a>Procedura: passare a un altro thread durante il debug
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Quando si esegue il debug di un'applicazione multithreading, è possibile utilizzare diversi metodi per cambiare contesto passando dal thread utilizzato a un altro thread.  
  
### <a name="to-switch-to-any-thread-that-appears-in-the-threads-window"></a>Per passare a un thread visualizzato nella finestra Thread  
  
-   Fare doppio clic sul thread.  
  
### <a name="to-switch-to-a-thread-in-a-source-window"></a>Per passare a un thread in una finestra di origine  
  
-   Nella barra di navigazione a sinistra, fare doppio clic su un indicatore del thread, scegliere **passare a**, quindi fare clic sul nome del thread al quale si desidera passare. Nel menu di scelta rapida vengono visualizzati solo i thread presenti in quella determinata posizione.  
  
     Se viene visualizzato alcun indicatore, fare doppio clic nella **thread** finestra e verificare che **Mostra thread nell'origine** sia selezionata.  
  
### <a name="to-switch-to-a-thread-in-the-debug-location-toolbar"></a>Per passare a un thread nella barra degli strumenti Posizione di debug  
  
1.  Nel **posizione di Debug** sulla barra degli strumenti, fare clic sui **Thread** casella.  
  
2.  Nell'elenco, fare clic sul thread al quale si desidera passare.  
  
## <a name="see-also"></a>Vedere anche  
 [Eseguire il debug di applicazioni multithreading](../debugger/debug-multithreaded-applications-in-visual-studio.md)



