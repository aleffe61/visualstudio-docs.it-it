---
title: Sicurezza dei modelli di testo | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- text templates, security
ms.assetid: 567a2383-7d43-4acc-af4a-cd70b7a0151e
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 65b4b6616921dae0abb0bb54316d8b8262d1f652
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49214682"
---
# <a name="security-of-text-templates"></a>Sicurezza dei modelli di testo
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

I modelli di testo presentano i problemi di sicurezza seguenti:  
  
-   Modelli di testo sono vulnerabili a operazioni di inserimento di codice arbitrario.  
  
-   Se il meccanismo usato dall'host per trovare un processore di direttiva non è protetto, è possibile eseguire un processore di direttiva dannoso.  
  
## <a name="arbitrary-code"></a>Esecuzione di codice arbitrario  
 Quando si scrive un modello, è possibile inserire il codice all'interno di \<# # > tag. In questo modo arbitraria di codice essere eseguito in un modello di testo.  
  
 Assicurarsi di ottenere modelli da fonti attendibili. Assicurarsi che avvisare gli utenti finali dell'applicazione non vengano eseguite modelli che non provengono da origini attendibili.  
  
## <a name="malicious-directive-processor"></a>Processore di direttiva dannosi  
 Il motore del modello testo interagisce con un host di trasformazione e uno o più processori di direttive per trasformare il testo del modello in un file di output. Per altre informazioni, vedere [il processo di trasformazione del modello di testo](../modeling/the-text-template-transformation-process.md).  
  
 Se il meccanismo usato dall'host per trovare un processore di direttiva non è protetto, viene eseguito il rischio di eseguire un processore di direttiva dannoso. Il processore di direttiva dannoso potrebbe fornire codice che viene eseguito in `FullTrust` modalità quando si esegue il modello. Se si crea un host di trasformazione del modello testo personalizzato, è necessario usare un meccanismo protetto, ad esempio il Registro di sistema per il motore individuare i processori di direttiva.



