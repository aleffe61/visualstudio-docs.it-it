---
title: 'DA0004: Utilizzo elevato del processore | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.rules.DAHighProcessorUsage
- vs.performance.rules.DA0004
- vs.performance.DA0004
- vs.performance.4
ms.assetid: 2c4fb569-929e-4f1d-8c50-b590ee371351
caps.latest.revision: 17
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a942a26bb4cd8ccca94fd442250fe8a239cba4ed
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51764035"
---
# <a name="da0004-high-processor-usage"></a>DA0004: Utilizzo elevato del processore
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Id regola | DA0004 |  
| Categoria | Utilizzo degli strumenti di profilatura |  
| Metodi di profilatura | Campionamento di strumentazione |  
| Messaggio | L'utilizzo del processore è costantemente superiore al 75%. È consigliabile usare la modalità di campionamento per le applicazioni basate sulla CPU. |  
| Tipo di regola | Informazioni |  
  
 Quando si esegue la profilatura tramite i metodi di campionamento, memoria .NET o conflitto di risorse, è necessario raccogliere almeno 10 campioni per attivare questa regola.  
  
## <a name="cause"></a>Causa  
 L'utilizzo del processore (CPU) è significativamente elevato nei dati di profilatura raccolti usando il metodo di strumentazione. Si consiglia di usare il metodo di profilatura del campionamento per profilare applicazioni associate alla CPU.  
  
## <a name="rule-description"></a>Descrizione della regola  
 Durante l'esecuzione della profilatura, il processore o i processori sono stati molto occupati in modo coerente. Un utilizzo della CPU elevato può indicare un'applicazione basata sulla CPU. In genere i profili instrumentati non rappresentano il modo più valido per esaminare gli scenari di utilizzo della CPU. Il campionamento di solito è più efficace quando si profilano applicazioni che per la maggior parte del tempo eseguono istruzioni sul processore.  
  
## <a name="how-to-fix-violations"></a>Come correggere le violazioni  
 Ad eccezione dei casi in cui è necessaria la temporizzazione della funzione o si è più interessati a comprendere l'input/output che i colli di bottiglia del processore, è consigliabile eseguire nuovamente la profilatura dell'applicazione usando il metodo di campionamento anziché il metodo di strumentazione.




