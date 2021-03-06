---
title: 'Procedura: cercare un Thread nella visualizzazione thread | Microsoft Docs'
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
- threads, searching
ms.assetid: 5609a9b3-c279-4426-9e2e-dd87896a6d6f
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fb1c3979b0505305fd4f6a600e3352c0d08955de
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51766910"
---
# <a name="how-to-search-for-a-thread-in-threads-view"></a>Procedura: cercare un thread nella visualizzazione thread
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

È possibile cercare un thread specifico nella visualizzazione thread utilizzando la relativa stringa di ID o un modulo di thread come criterio di ricerca. È anche possibile specificare la direzione iniziale della ricerca. I campi nella finestra di dialogo mostrerà gli attributi del thread selezionato nell'albero del thread.  
  
### <a name="to-search-for-a-thread-in-threads-view"></a>Per cercare un thread nella visualizzazione thread  
  
1. Disporre le finestre in modo tale Spy + + e un oggetto attivo [visualizzazione thread](../debugger/threads-view.md) finestra sono visibili.  
  
2. Dal **ricerca** menu, scegliere **trova Thread**.  
  
    Il [finestra di dialogo Ricerca Thread](../debugger/thread-search-dialog-box.md) apre.  
  
3. Digitare l'ID del thread o una stringa del modulo come criterio di ricerca.  
  
4. Deselezionare tutti i campi per cui non si desidera specificare i valori.  
  
   > [!TIP]
   >  Per trovare tutti i thread appartenenti a un modulo, cancellare il **Thread** casella di testo e il tipo di modulo assegnare un nome nel **modulo** casella. Quindi usare **Trova successivo** per continuare la ricerca per i thread.  
  
5. Scegli **iscrizione** oppure **verso il basso** per la direzione iniziale della ricerca.  
  
6. Fare clic su **OK**.  
  
   Se il thread corrispondente viene trovato, evidenziarlo nella finestra Visualizzazione thread.



