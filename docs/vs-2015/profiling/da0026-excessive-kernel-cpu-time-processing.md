---
title: 'DA0026: Tempo di elaborazione CPU kernel eccessivo | Microsoft Docs'
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
- vs.performance.rules.DA0026
- vs.performance.DA0026
- vs.performance.26
ms.assetid: 4cfc8a29-b29b-4a72-b386-03d8856fdf8a
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e2dbf52ab216a2272cb3b6094126a34987588704
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51749663"
---
# <a name="da0026-excessive-kernel-cpu-time-processing"></a>DA0026: Tempo di elaborazione CPU kernel eccessivo
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Id regola | TODO |  
| Categoria | Utilizzo degli strumenti di profilatura |  
| Metodo di profilatura | Campionamento |  
| Messaggio | È stata misurata relativamente elevata quantità di tempo di CPU in modalità kernel. Provare ad analizzare l'origine campionamento SysCall. |  
| Tipo di regola | Informazioni |  
  
 Quando si esegue la profilatura tramite i metodi di campionamento, memoria .NET o conflitto di risorse, è necessario raccogliere almeno 10 campioni per attivare questa regola.  
  
## <a name="cause"></a>Causa  
 Il tempo CPU proporzionale eseguito in modalità kernel ha superato la quantità di tempo trascorso in modalità utente. Per determinare la causa degli elevati tempi di esecuzione in modalità kernel, eseguire di nuovo la profilatura e abilitare il campionamento del numero di chiamate di sistema (syscalls).  
  
## <a name="rule-description"></a>Descrizione della regola  
 La percentuale relativamente elevata del tempo impiegato dall'applicazione in modalità kernel può giustificare l'esecuzione di ulteriori analisi. Un'applicazione in modalità utente passa alla modalità kernel per eseguire operazioni di I/O, per attendere primitive di sincronizzazione di thread o processi o per eseguire chiamate di sistema. È possibile analizzare i tipi di chiamate di sistema effettuati dall'applicazione e le funzioni responsabili di tali chiamate selezionando l'opzione per raccogliere stack di chiamate campione in base alle chiamate di sistema.  
  
## <a name="how-to-fix-violations"></a>Come correggere le violazioni  
 Per analizzare i tipi di chiamate di sistema effettuati dall'applicazione, eseguire nuovamente il profilo e selezionare l'opzione per raccogliere campioni in base alle chiamate al sistema. Se si eseguono gli strumenti di profilatura nell'IDE, vedere [Procedura: Scegliere eventi di campionamento](../profiling/how-to-choose-sampling-events.md) per altre informazioni. Se si eseguono gli strumenti di profilatura dalla riga di comando, vedere la sezione **Sampling Interval Options** (Opzioni di intervallo di campionamento) dell'argomento [VSPerfCmd](../profiling/vsperfcmd.md) nel riferimento agli strumenti di profilatura della riga di comando.



