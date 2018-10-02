---
title: Modifica e continuazione (Visual Basic) | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
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
- VB
helpviewer_keywords:
- Edit and Continue, 64-bit
- Edit and Continue [Visual Basic]
- debugging [Visual Basic], Edit and Continue
- Visual Basic, Edit and Continue
- 64-bit Edit and Continue
ms.assetid: 7e90f34f-e699-45ab-a4c9-a4b527c498c8
caps.latest.revision: 43
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 825eac4ab53e95904e85a794b665ce6f6b11f873
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519909"
---
# <a name="edit-and-continue-visual-basic"></a>Modifica e continuazione (Visual Basic)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [modifica e continuazione (Visual Basic)](https://docs.microsoft.com/visualstudio/debugger/edit-and-continue-visual-basic).  
  
Modifica e continuazione è una funzionalità per il debug di [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] che consente di apportare modifiche al codice mentre viene eseguito in modalità di interruzione. Dopo aver applicato le modifiche al codice, è possibile riprendere l'esecuzione del codice con le nuove modifiche già inserite e verificarne l'effetto.  
  
 La funzionalità Modifica e continuazione può essere utilizzata ogni volta che si attiva la modalità di interruzione. In modalità di interruzione il puntatore all'istruzione, ovvero la freccia gialla nella finestra del codice sorgente, punta alla riga che verrà eseguita successivamente ed è posizionato in un'istruzione eseguibile all'interno del corpo di un metodo o una proprietà. In questa modalità è possibile apportare alle istruzioni eseguibili quasi tutti i tipi di modifiche, le quali verranno incorporate nel progetto sottostante. In modalità di interruzione, tuttavia, non è in genere consentito apportare modifiche a istruzioni di dichiarazione, quali i metodi pubblici, i campi pubblici o le dichiarazioni di classe.  
  
 Quando si apporta una modifica non autorizzata, la modifica viene contrassegnata con una sottolineatura ondulata di colore viola e nell'Elenco attività viene visualizzata un'attività. Per poter continuare a utilizzare Modifica e continuazione, è necessario annullare la modifica non autorizzata. Alcune modifiche non autorizzate sono consentite se effettuate all'esterno di Modifica e continuazione. Se si desidera mantenere i risultati di tale modifica non autorizzata, è necessario interrompere il debug e riavviare l'applicazione.  
  
 La modalità Modifica e continuazione è supportata per i progetti a 64 bit destinati a .NET Framework 4.5.1.  
  
 Modifica e continuazione non è supportato quando si avvia il debug usando **Connetti a processo**. La funzionalità Modifica e continuazione non è supportata per il codice ottimizzato, il codice nativo e gestito misto o i progetti Compact Framework (Smart Device).  
  
 Negli argomenti di questa sezione vengono fornite informazioni dettagliate sull'utilizzo di questa funzionalità e sui tipi di modifiche non consentiti.  
  
## <a name="in-this-section"></a>In questa sezione  
 [Procedura: Applicare modifiche in modalità di interruzione con Modifica e continuazione](../debugger/how-to-apply-edits-in-break-mode-with-edit-and-continue.md)  
 Viene descritto come applicare modifiche al codice in modalità di interruzione.  
  
 [Modifiche non supportate in Modifica e continuazione di Visual Basic](../debugger/unsupported-edits-in-visual-basic-edit-and-continue.md)  
 Descrive i tipi di modifiche che non è possibile eseguire in Modifica e continuazione di [!INCLUDE[vb_current_short](../includes/vb-current-short-md.md)].  
  
## <a name="related-sections"></a>Sezioni correlate  
 [Modifica e continuazione](../debugger/edit-and-continue.md)  
 È disponibile un elenco di argomenti su Modifica e continuazione.


