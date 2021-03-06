---
title: "Procedura: attivare l'avvio automatico per le installazioni da CD | Microsoft Docs"
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, AutoStart
- ClickOnce deployment, installation on CD or DVD
- deploying applications [ClickOnce], installation on CD or DVD
ms.assetid: caaec619-900c-4790-90e3-8c91f5347635
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 2fde610731ca5ec315b94d2e46f58edb2a7b56fa
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49273143"
---
# <a name="how-to-enable-autostart-for-cd-installations"></a>Procedura: attivare l'avvio automatico per le installazioni da CD
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Quando si distribuisce un [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] dell'applicazione mediante supporti rimovibili, ad esempio CD-ROM o DVD-ROM di avvio, è possibile abilitare `AutoStart` in modo che il [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] applicazione viene avviata automaticamente dopo l'inserimento del supporto.  
  
 `AutoStart` può essere abilitata per il **Publish** pagina della **creazione progetti**.  
  
### <a name="to-enable-autostart"></a>Abilitare l'avvio automatico  
  
1.  Con un progetto selezionato in **Esplora soluzioni**, scegliere **Proprietà** dal menu **Progetto**.  
  
2.  Scegliere il **pubblica** scheda.  
  
3.  Scegliere il **opzioni** pulsante.  
  
     Il **Publish Options** verrà visualizzata la finestra di dialogo.  
  
4.  Fare clic su **distribuzione**.  
  
5.  Selezionare il **per installazioni da CD, avvia automaticamente l'installazione all'inserimento del CD** casella di controllo.  
  
     Un file Autorun verrà copiato nel percorso di pubblicazione è pubblicata l'applicazione.  
  
## <a name="see-also"></a>Vedere anche  
 [Pubblicazione di applicazioni ClickOnce](../deployment/publishing-clickonce-applications.md)   
 [Procedura: Pubblicare un'applicazione ClickOnce mediante la Pubblicazione guidata](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)



