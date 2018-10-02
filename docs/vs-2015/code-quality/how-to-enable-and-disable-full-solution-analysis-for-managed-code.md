---
title: "Procedura: abilitare e disabilitare l'analisi della soluzione completa per il codice gestito | Microsoft Docs"
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- full solution analysis
ms.assetid: 04315147-5792-47f0-8b5f-9ac8413c6a57
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 4815963966c54d7c237737d85c2e573e886bc9ba
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47526834"
---
# <a name="how-to-enable-and-disable-full-solution-analysis-for-managed-code"></a>Procedura: abilitare e disabilitare l'analisi della soluzione completa per il codice gestito
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [procedura: abilitare e disabilitare analisi della soluzione completa per codice gestito](https://docs.microsoft.com/visualstudio/code-quality/how-to-enable-and-disable-full-solution-analysis-for-managed-code).  
  
NOTA]
>  Questo argomento si applica solo a Visual Studio 2015 Update 3 RC e versioni successive.  
  
 *Analisi della soluzione completa* è una funzionalità di Visual Studio che consente di scegliere se vengono visualizzati i problemi di analisi codice solo in Visual c# o Visual Basic file aperti nella soluzione o nel file Visual c# o Visual Basic sia aperti e chiusi nella soluzione.  
  
 Benché sia utile la possibilità di vedere tutti i problemi in tutti i file, può essere fonte di distrazione e rallentano anche a Visual Studio se la soluzione è molto grande o contiene una grande quantità di file.  Per limitare il numero di problemi visualizzati e migliorare le prestazioni di Visual Studio, è possibile disabilitare l'analisi della soluzione completa. Se si desidera, è possibile riabilitare facilmente questa funzionalità.  
  
#### <a name="to-toggle-full-solution-analysis"></a>Per attivare o disattivare analisi della soluzione completa  
  
1.  Nel menu principale in Visual Studio, scegliere **degli strumenti** &#124; **opzioni** per visualizzare il **opzioni** nella finestra di dialogo.  
  
2.  Nel **le opzioni** finestra di dialogo, scegliere **Editor di testo** &#124; **c#** o **Basic** &#124; **avanzate**.  
  
3.  Selezionare il **Abilita analisi della soluzione completa** casella di controllo per abilitare l'analisi della soluzione completa o deselezionare la casella per disabilitarla. Scegliere il **OK** pulsante al termine.  
  
     ![Abilitare la casella di controllo analysis soluzione completa. ](../code-quality/media/fsa-toolsoptions.png "FSA_ToolsOptions")  
  
## <a name="results-of-enabling-and-disabling-full-solution-analysis"></a>Risultati di abilitazione e disabilitazione di analisi della soluzione completa  
 Nello screenshot seguente, è possibile visualizzare i risultati quando sono abilitata l'analisi della soluzione completa. Tutti gli errori e problemi di analisi del codice nel *tutti* dei file nella soluzione viene visualizzata, indipendentemente dal fatto che i file sono aperti.  
  
 ![Analisi della soluzione completa abilitata. ](../code-quality/media/fsa-enabled.png "FSA_Enabled")  
  
 Lo screenshot seguente mostra i risultati dalla stessa soluzione dopo la disabilitazione di analisi della soluzione completa. Solo gli errori e problemi di analisi del codice in aprono Esplora file vengono visualizzati nell'elenco errori.  
  
 ![Analisi della soluzione completa disabilitato. ](../code-quality/media/fsa-disabled.png "FSA_Disabled")  
  
## <a name="automatically-disabling-full-solution-analysis"></a>Automaticamente la disabilitazione di analisi della soluzione completa  
 Se Visual Studio rileva che 200MB o inferiore di memoria di sistema è disponibile a esso, viene disabilitata automaticamente analisi della soluzione completa (nonché alcune altre funzionalità) se è abilitato. In questo caso, viene visualizzato un avviso per informare l'utente di questo oggetto. Un pulsante consente di abilitare nuovamente l'analisi della soluzione completa se si desidera eseguire questa operazione.  
  
 ![Testo dell'avviso la sospensione di analisi della soluzione completa](../code-quality/media/fsa-alert.png "FSA_Alert")  
  
## <a name="additional-details"></a>Dettagli aggiuntivi  
 Per impostazione predefinita, analisi della soluzione completa sono abilitato per Visual Basic e disabilitato per Visual c#.  
  
 Visual Studio Update 3 RC include un motore di diagnostica v2 analizzatore ottimizzato del codice che riduce l'utilizzo di memoria in modo significativo e riduce il tempo di CPU per inattività, anche se sono abilitata l'analisi della soluzione completa.


