---
title: 'Procedura: modificare il computer di riproduzione di diagnostica della grafica | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 1b9aa3ea-29a0-4e21-bc57-936f33537b5c
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a2d5d56d37bbed4180d1231cac54da6beff3418d
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51737597"
---
# <a name="how-to-change-the-graphics-diagnostics-playback-machine"></a>Procedura: modificare il computer di riproduzione della diagnostica della grafica
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

È possibile riprodurre informazioni grafiche con computer locale o utilizzando un computer o dispositivo remoto.  
  
## <a name="choosing-a-playback-machine"></a>Scelta di un computer di riproduzione  
 Il computer di riproduzione è un computer o dispositivo che viene usato per riprodurre gli eventi di grafica da un log di grafica. In genere, il computer locale è l'opzione più semplice, ma un problema di rendering non potrebbe riprodursi in un computer con hardware diverse o versioni di driver al computer in cui è stato acquisito; In questo caso, è possibile scegliere un computer riproduzione remoto che riproduce meglio il problema e utilizzare comunque il computer di sviluppo per diagnosticarlo.  
  
#### <a name="to-use-the-local-machine-to-play-back-graphics-information"></a>Usare il computer locale per riprodurre informazioni grafiche  
  
1.  Nella finestra del documento di Log di grafica scegliere il **computer di riproduzione** collegamento. Il **connessioni Debugger remoto** verrà visualizzata la finestra di dialogo.  
  
2.  Sotto **Manual Configuration**, nella **indirizzo** proprietà, immettere `localhost`.  
  
3.  Impostare il **modalità di autenticazione** proprietà **None**.  
  
4.  Scegliere il **seleziona** pulsante.  
  
#### <a name="to-use-a-remote-machine-to-play-back-graphics-information"></a>Usare un computer remoto per riprodurre informazioni grafiche  
  
1.  Nella finestra del documento di Log di grafica scegliere il **computer di riproduzione** collegamento. Il **connessioni Debugger remoto** verrà visualizzata la finestra di dialogo.  
  
2.  Sotto **Manual Configuration**, nella **indirizzo** proprietà, immettere il nome di dominio Windows o l'indirizzo IP della macchina o del dispositivo che si desidera utilizzare per riprodurre informazioni grafiche.  
  
3.  Specificare il tipo di autorizzazione che si desidera usare per proteggere la connessione al computer di riproduzione.  
  
    -   Per l'autenticazione di Windows, impostare il **modalità di autenticazione** proprietà **Windows**.  
  
    -   Nessuna autenticazione, impostare il **modalità di autenticazione** proprietà **None**.  
  
4.  Scegliere il **seleziona** pulsante.  
  
> [!NOTE]
>  Il **connessioni Debugger remoto** nella finestra di dialogo può inoltre essere visualizzate le destinazioni di debug remote che sono direttamente connessi al computer di sviluppo o che sono nella stessa subnet. È possibile usare una di queste destinazioni di debug remote come computer di riproduzione della diagnostica della grafica senza configurarlo manualmente. Nel **le connessioni Remote Debugger** finestra di dialogo, selezionare la destinazione desiderata, quindi scegliere il **selezionare** pulsante.  
  
## <a name="see-also"></a>Vedere anche  
 [Documento di log della grafica](../debugger/graphics-log-document.md)



