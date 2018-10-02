---
title: Modifica e continuazione finestra di messaggio di errore | Microsoft Docs
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
- vs.debug.ENC.SupportedButNotAvaiable
- vs.debug.ENC.CannotEditWhileException
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- Edit and Continue Error Message dialog box
ms.assetid: f98c91c0-447a-4533-85b6-87170a0dc4c3
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d649df9584fc06ee08b7a7d1e846597c12519019
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47525259"
---
# <a name="edit-and-continue-error-message-dialog-box"></a>Finestra di dialogo di errore di Modifica e continuazione
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [modifica e continuazione finestra messaggio di errore](https://docs.microsoft.com/visualstudio/debugger/edit-and-continue-error-message-dialog-box).  
  
Questa finestra di dialogo viene visualizzata quando si esegue il debug in un linguaggio che supporta la modifica e continuazione, ma **modifica e continuazione** non è disponibile per il tipo di sono state apportate modifiche al codice. Nel messaggio di errore sono riportate informazioni più dettagliate. Questa finestra di dialogo può essere visualizzata per uno dei seguenti motivi:  
  
-   Si è tentato di modificare il codice gestito mentre era abilitato il debug di codice non gestito. La funzionalità Modifica e continuazione non è compatibile con il debug in modalità mista.  
  
-   Si è tentato di modificare il codice di SQL Server.  
  
-   Si è tentato di modificare il codice durante il debug di un dump di Dr. Watson.  
  
-   Si è provato a modificare il codice dopo che si è verificata un'eccezione non gestita e l'opzione "**Rimuovi stack di chiamate su eccezioni non gestite**" non è stato selezionato.  
  
-   Si è tentato di modificare il codice durante il debug di un'applicazione di runtime incorporata.  
  
-   Si è provato a modificare il codice in un programma che si era connessi anziché avviandolo dal **Debug** menu.  
  
-   Si è tentato di modificare il codice ottimizzato.  
  
-   Si è tentato di modificare il codice gestito quando la destinazione è un'applicazione a 64 bit. Se si desidera utilizzare Modifica e continuazione, è necessario impostare la destinazione su x86 (*Project* **delle proprietà**, **compilare** scheda **del compilatore avanzate** impostazione.).  
  
-   Si è tentato di modificare il codice in un assembly modificato durante il debug e ricaricato.  
  
-   Si è tentato di modificare il codice in un assembly che non è stato caricato.  
  
-   Si è avviato il debug di una versione precedente dell'applicazione, poiché la nuova versione presenta errori di compilazione.  
  
-   Si è tentato di modificare il codice durante l'esecuzione.  
  
## <a name="uielement-list"></a>Elenco UIElement  
 **OK**  
 Chiudere la finestra di dialogo e annullare il tentativo di modifica immediatamente precedente.  
  
## <a name="see-also"></a>Vedere anche  
 [Modifiche al codice supportate (C++)](../debugger/supported-code-changes-cpp.md)


