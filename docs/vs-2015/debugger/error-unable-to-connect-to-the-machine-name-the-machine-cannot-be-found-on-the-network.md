---
title: 'Errore: Impossibile connettersi alla macchina &lt;nome&gt;. Impossibile trovare il computer sulla rete. | Microsoft Docs'
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
- vs.debug.remote.dcom_disabled
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- DCOM, unable to connect error
ms.assetid: b584b5db-ef52-45ed-8561-1314da3cc5b8
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fbd5299c8bd14581a9228b7aa0491af6455b1fda
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47526964"
---
# <a name="error-unable-to-connect-to-the-machine-ltnamegt-the-machine-cannot-be-found-on-the-network"></a>Errore: Impossibile connettersi alla macchina &lt;nome&gt;. Impossibile trovare il computer sulla rete.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [errore: Impossibile connettersi alla macchina &lt;nome&gt;. Impossibile trovare il computer sulla rete. ](https://docs.microsoft.com/visualstudio/debugger/error-unable-to-connect-to-the-machine-name-the-machine-cannot-be-found-on-the-network).  
  
Questo messaggio di errore viene visualizzato quando si verifica una delle seguenti condizioni:  
  
-   La connessione stabilita al computer remoto è stata interrotta.  
  
-   L'account utente utilizzato per la connessione al computer remoto è stato disabilitato.  
  
-   La password utilizzata per la connessione al computer remoto è scaduta.  
  
### <a name="to-resolve-this-behavior"></a>Per risolvere questo comportamento  
  
-   Assicurarsi che il computer locale e il computer remoto si trovino nella stessa rete. A tale scopo, utilizzare Esplora risorse o Esplora file per tentare di accedere al computer remoto.  
  
     - e -  
  
-   Assicurarsi che l'account utente utilizzato per la connessione al computer remoto sia attivato.  
  
     - e -  
  
-   Assicurarsi che la password utilizzata per la connessione al computer remoto sia valida e non scaduta.  
  
## <a name="see-also"></a>Vedere anche  
 [Impostare Remote Tools sul dispositivo](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c)   
 [Impostazioni di debug e preparazione](../debugger/debugger-settings-and-preparation.md)


