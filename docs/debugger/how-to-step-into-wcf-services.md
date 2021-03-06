---
title: 'Procedura: passaggio nei servizi WCF | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging, WCF
- WCF, debugging
ms.assetid: 9893ad01-54af-499f-85a6-9d1cfe6eb640
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cad65b893867a18133bbf9492a1c1786b24a81ed
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49912163"
---
# <a name="how-to-step-into-wcf-services"></a>Procedura: eseguire istruzioni nei servizi WCF
In [!INCLUDE[vs_dev11_long](../data-tools/includes/vs_dev11_long_md.md)], è possibile eseguire istruzioni in un servizio WCF. Se il servizio WCF si trova nella stessa soluzione [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] del client, è possibile raggiungere punti di interruzione nel servizio WCF.  
  
 Per consentire il funzionamento, è necessario avere attivato il debug nel file app.config o web.config. Per informazioni su come abilitare il debug e per le limitazioni sull'esecuzione dei servizi WCF, vedere [limitazioni del debug di WCF](../debugger/limitations-on-wcf-debugging.md).  
  
### <a name="to-step-into-a-wcf-service"></a>Per eseguire istruzioni in un servizio WCF  
  
1. Creare una soluzione [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] contenente entrambi i progetti client WCF e servizio WCF.  
  
2. In Esplora soluzioni, fare clic sul progetto Client WCF e quindi fare clic su **imposta come progetto di avvio**.  
  
3. Attivare il debug nel file app.config o web.config. Per altre informazioni, vedere [limitazioni del debug di WCF](../debugger/limitations-on-wcf-debugging.md).  
  
4. Impostare un punto di interruzione nel percorso all'interno del progetto client in cui si desidera iniziare a eseguire le istruzioni. In genere, si troverà poco prima della chiamata del servizio WCF.  
  
5. Eseguire il debug nel punto d'interruzione, quindi iniziare a eseguire le istruzioni. Il debugger eseguirà automaticamente le istruzioni nel servizio.  
  
## <a name="see-also"></a>Vedere anche  
 [Debug dei servizi WCF](../debugger/debugging-wcf-services.md)   
 [Limitazioni del debug di WCF](../debugger/limitations-on-wcf-debugging.md)   
 [Procedura: Eseguire il debug di un servizio WCF indipendente](../debugger/how-to-debug-a-self-hosted-wcf-service.md)