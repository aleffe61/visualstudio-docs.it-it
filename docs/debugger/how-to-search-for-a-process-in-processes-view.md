---
title: 'Procedura: cercare un processo nella visualizzazione processi | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Processes view
- processes, searching for
ms.assetid: 7cb97b37-4a95-4f1b-9eee-4910aa9c115b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8129516476977e526cde9c3eb3dbe546bdbe3876
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49822917"
---
# <a name="how-to-search-for-a-process-in-processes-view"></a>Procedura: cercare un processo nella visualizzazione processi
È possibile cercare un processo specifico nella visualizzazione processi usando la relativa stringa di ID o un modulo di processo come criterio di ricerca. È anche possibile specificare la direzione iniziale della ricerca. I campi nella finestra di dialogo mostrerà gli attributi del processo selezionato nell'albero del processo.  
  
### <a name="to-search-for-a-process-in-processes-view"></a>Per cercare un processo nella visualizzazione processi  
  
1. Disporre le finestre in modo tale Spy + + e un oggetto attivo [visualizzazione processi](../debugger/processes-view.md) finestra sono visibili.  
  
2. Dal **ricerca** menu, scegliere **Trova processo**  
  
    Il [dialogo Ricerca processi](../debugger/process-search-dialog-box.md) apre.  
  
3. Digitare l'ID del processo o una stringa del modulo come criterio di ricerca.  
  
4. Deselezionare tutti i campi per cui non si desidera specificare i valori.  
  
   > [!TIP]
   >  Per trovare tutti i processi appartenenti a un modulo, cancellare il **processo** e digitare il nome del modulo nel **modulo** casella. Quindi usare **Trova successivo** per continuare la ricerca dei processi.  
  
5. Scegli **iscrizione** oppure **verso il basso** per la direzione iniziale della ricerca.  
  
6. Fare clic su **OK**.  
  
   Se viene trovato un processo di corrispondenza, è evidenziato nel **visualizzazione processo** finestra.