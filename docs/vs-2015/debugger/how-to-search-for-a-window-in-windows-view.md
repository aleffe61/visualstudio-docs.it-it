---
title: 'Procedura: cercare una finestra in Windows Vista | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- windows, searching in Windows view
ms.assetid: 30306970-b861-4315-acf8-f86a43d4e73b
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 60eb467a24c85d176dae7727a476cc45dac6c876
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51782973"
---
# <a name="how-to-search-for-a-window-in-windows-view"></a>Procedura: cercare una finestra nella visualizzazione finestre
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

È possibile cercare una specifica finestra nella visualizzazione di Windows usando il relativo handle, didascalie, classe o una combinazione di titolo e classe come criterio di ricerca. È anche possibile specificare la direzione iniziale della ricerca. I campi nella finestra di dialogo mostrerà gli attributi della finestra selezionata nell'albero della finestra.  
  
 Iniziare con la struttura ad albero espansa per il secondo livello (tutte le finestre che sono figli del desktop), in modo che sia possibile identificare a livello di desktop windows tramite il nome della classe e il titolo. Dopo aver scelto una finestra del desktop a livello, è possibile espandere tale livello per trovare una specifica finestra figlio.  
  
### <a name="to-search-for-a-window-in-windows-view"></a>Per cercare una finestra nella visualizzazione di Windows  
  
1.  Disporre le finestre in modo tale Spy + +, il [Windows Vista](../debugger/windows-view.md) finestra e finestra di destinazione sono visibili.  
  
2.  Dal **ricerca** menu, scegliere **Trova finestra**.  
  
     Il [finestra di dialogo ricerca](../debugger/window-search-dialog-box.md) apre.  
  
    > [!TIP]
    >  Per ridurre il disordine schermata, selezionare la **Nascondi Spy + +** opzione. Questa opzione consente di nascondere la finestra principale di Spy + + e rimane solo il **ricerca finestre** nella finestra di dialogo visibile nella parte superiore alle altre applicazioni. La finestra principale di Spy + + è ripristinata quando si fa clic **OK** oppure **Cancel**, o quando si cancella il **Nascondi Spy + +** opzione.  
  
3.  Trascinare il **strumento di ricerca** nell'intervallo di destinazione. Quando si trascina lo strumento, il **ricerca finestre** nella finestra di dialogo vengono visualizzati i dettagli sulla finestra selezionata.  
  
     - oppure -  
  
     Se si conosce l'handle della finestra desiderata (ad esempio, dal debugger), è possibile digitare nel **gestire** casella.  
  
     - oppure -  
  
     Se si conosce il sottotitolo e/o classe della finestra di cui si desidera, è possibile digitarli nel **didascalia** e **classe** caselle di testo e deselezionare il **gestire** casella di testo.  
  
4.  Scegli **iscrizione** oppure **verso il basso** per la direzione iniziale della ricerca.  
  
5.  Fare clic su **OK**.  
  
     Se la finestra corrispondente viene trovata, viene evidenziato nel [Windows Vista](../debugger/windows-view.md) finestra.



