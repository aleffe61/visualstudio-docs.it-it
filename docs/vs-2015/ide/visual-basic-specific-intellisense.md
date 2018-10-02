---
title: Funzionalità di IntelliSense specifiche per Visual Basic | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IntelliSense [Visual Basic]
- IntelliSense [Visual Studio], Visual Basic
ms.assetid: 4dec8753-05e5-4f74-b304-5f8c4ed8723b
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 9bae55b10695ba73fec86d7ab63943e3440e3f05
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47532339"
---
# <a name="visual-basic-specific-intellisense"></a>Funzionalità di IntelliSense specifiche per Visual Basic
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [specifiche per Visual Basic IntelliSense](https://docs.microsoft.com/visualstudio/ide/visual-basic-specific-intellisense).  
  
L'editor del codice sorgente di Visual Basic offre le seguenti funzionalità di IntelliSense:  
  
-   Suggerimenti per la sintassi  
  
     I suggerimenti per la sintassi visualizzano la sintassi dell'istruzione che si sta digitando. La funzionalità è utile per istruzioni come [Declare](http://msdn.microsoft.com/library/d3f21fb0-b804-4c99-97ed-583b23894cf1).  
  
## <a name="automatic-completion"></a>Completamento automatico  
  
-   Completamento di diverse parole chiave  
  
     Ad esempio, se si digita `goto` e uno spazio, IntelliSense visualizza un elenco delle etichette definite in un menu a discesa. Altre parole chiave supportate sono `Exit`, `Implements`, `Option` e `Declare`.  
  
-   Completamento per `Enum` e `Boolean`  
  
     Quando un'istruzione fa riferimento a un membro di enumerazione, IntelliSense visualizza un elenco dei membri di `Enum`. Quando un'istruzione fa riferimento a un oggetto `Boolean`, IntelliSense visualizza un menu a discesa di valori true e false.  
  
 Il completamento può essere disattivato per impostazione predefinita deselezionando **Elenco membri automatico** dalla pagina **Generale** delle proprietà nella cartella **Visual Basic**.  
  
 È possibile richiamare manualmente il completamento richiamando Elenca membri, Completa parola o ALT+ FRECCIA DESTRA. Per altre informazioni, vedere [Using IntelliSense](../ide/using-intellisense.md) (Uso di IntelliSense).  
  
## <a name="intellisense-in-zone"></a>IntelliSense sensibile all'area  
 IntelliSense sensibile all'area offre un supporto agli sviluppatori di Visual Basic che devono distribuire applicazioni con [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] e sono vincolati a impostazioni di attendibilità parziale. Questa funzionalità:  
  
-   Consente di scegliere le autorizzazioni con cui verrà eseguita l'applicazione.  
  
-   Visualizza le API dell'area prescelta come disponibili in Elenca membri e le API che richiedono autorizzazioni aggiuntive come non disponibili.  
  
 Per altre informazioni, vedere [Sicurezza dall'accesso di codice per applicazioni ClickOnce](../deployment/code-access-security-for-clickonce-applications.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Utilizzo di IntelliSense](../ide/using-intellisense.md)


