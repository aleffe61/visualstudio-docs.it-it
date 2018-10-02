---
title: 'Procedura: cercare un thread nella visualizzazione messaggi | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Message Search dialog box
- Messages view
- messages, searching for
ms.assetid: 732b7ccc-54ea-41db-823b-2b96e3e4083e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 984c3f0dc9b61059b53a7caf5a859d3413c99e62
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47529119"
---
# <a name="how-to-search-for-a-message-in-messages-view"></a>Procedura: cercare un thread nella visualizzazione messaggi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [procedura: cercare un thread nella visualizzazione messaggi](https://docs.microsoft.com/visualstudio/debugger/how-to-search-for-a-message-in-messages-view).  
  
È possibile cercare un messaggio specifico nella visualizzazione dei messaggi tramite relativo handle, tipo o ID del messaggio come criterio di ricerca. Una di queste, o una combinazione, ovvero saranno i criteri di ricerca valida. La direzione iniziale della ricerca può anche essere specificata. I campi nella finestra di dialogo sono precaricati con gli attributi del messaggio attualmente selezionato.  
  
### <a name="to-search-for-a-message-in-messages-view"></a>Per cercare un messaggio nella visualizzazione messaggi  
  
1.  Disporre le finestre in modo tale Spy + + e un oggetto attivo [visualizzazione messaggi](../debugger/messages-view.md) finestra sono visibili.  
  
2.  Dal **ricerca** menu, scegliere **Trova messaggio**.  
  
     Il [finestra di dialogo Ricerca messaggi](../debugger/message-search-dialog-box.md) apre.  
  
3.  Trascinare il **strumento di ricerca** rispetto alla finestra desiderata. Quando si trascina lo strumento, il **ricerca messaggi** nella finestra di dialogo vengono visualizzati i dettagli sulla finestra selezionata.  
  
     - oppure -  
  
     Se hai l'handle della finestra di cui si desidera esaminare i messaggi, digitarla nella **gestire** casella di testo.  
  
     - oppure -  
  
     Se si conosce il tipo di messaggio e/o ID del messaggio desiderati, selezionarli dal **tipo** e **messaggio** menu a discesa e deselezionare il **gestire** casella di testo.  
  
4.  Deselezionare tutti i campi per cui non si desidera specificare i valori.  
  
    > [!TIP]
    >  Per ridurre il disordine schermata, selezionare la **Nascondi Spy + +** opzione. Questa opzione consente di nascondere la finestra principale di Spy + + e di mantenere solo le **Trova finestra** nella finestra di dialogo visibile nella parte superiore alle altre applicazioni. La finestra principale di Spy + + è ripristinata quando si fa clic **OK** oppure **Cancel**, o quando si cancella il **Nascondi Spy + +** opzione.  
  
5.  Scegli **iscrizione** oppure **verso il basso** per la direzione iniziale della ricerca.  
  
6.  Fare clic su **OK**.  
  
 Se viene trovato un messaggio corrisponda, evidenziarlo nella finestra di visualizzazione dei messaggi. Visualizzare [la visualizzazione messaggi](../debugger/messages-view.md).


