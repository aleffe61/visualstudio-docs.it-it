---
title: Raccolta di statistiche di applicazioni Web ASP.NET usando il metodo di campionamento del profiler tramite la riga di comando | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- profiling tools, sampling method
- sampling profling method
ms.assetid: f8383ab1-eb49-4d3f-8608-d8b4d51a81be
caps.latest.revision: 22
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d4353308ce42ad61fdc53732d1a077f510ed2c1c
ms.sourcegitcommit: 71218ffc33da325cc1b886f69ff2ca50d44f5f33
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/09/2018
ms.locfileid: "48881552"
---
# <a name="collecting-application-statistics-for-aspnet-web-applications-using-the-profiler-sampling-method-from-the-command-line"></a>Raccolta di statistiche di applicazioni Web ASP.NET usando il metodo di campionamento del profiler tramite la riga di comando
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [raccogliere statistiche dell'applicazione per le applicazioni Web ASP.NET usando il metodo di campionamento del Profiler da riga di comando](https://docs.microsoft.com/visualstudio/profiling/collecting-application-statistics-for-aspnet-web-applications-using-the-profiler-sampling-method-from-the-command-line).  
  
Questa sezione descrive le procedure e le opzioni per la raccolta di statistiche sulle prestazioni per un'applicazione Web ASP.NET tramite gli strumenti da riga di comando **VSPerfASPNETCmd** e **VSPerfCmd** e il metodo di profilatura del campionamento.  
  
> [!NOTE]
>  Le funzionalità di sicurezza avanzate di Windows 8 e Windows Server 2012 hanno richiesto modifiche significative riguardo alla modalità di raccolta dei dati su queste piattaforme da parte del profiler di Visual Studio. Le app di Windows Store richiedono nuove tecniche di raccolta. Vedere [Performance Tools on Windows 8 and Windows Server 2012 applications](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md) (Strumenti per le prestazioni nelle applicazioni Windows 8 e Windows Server 2012).  
  
> [!NOTE]
>  Anche se lo strumento **VSPerfCmd** consente l'accesso completo alle funzionalità degli strumenti di profilatura che consentono la sospensione e la ripresa della profilatura e la raccolta di dati aggiuntivi dal processore e dai contatori delle prestazioni di Windows, quando queste funzionalità non sono necessarie è consigliabile usare lo strumento da riga di comando **VSPerfASPNETCmd**. Lo strumento da riga di comando **VSPerfASPNETCmd** è il metodo preferito per la profilatura di siti Web ASP.NET tramite il profiler autonomo. Rispetto allo strumento da riga di comando [VSPerfCmd](../profiling/vsperfcmd.md), non è necessario impostare variabili di ambiente né riavviare il computer. Per altre informazioni, vedere [Rapid Web Site Profiling with VSPerfASPNETCmd](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md) (Profilatura rapida di un sito Web con VSPerfASPNETCmd).  
  
## <a name="common-tasks"></a>Attività comuni  
  
|Attività|Contenuto correlato|  
|----------|---------------------|  
|**Connettere il profiler a un'applicazione ASP.NET**|-   [How to: Attach the Profiler to an ASP.NET Web Application to Collect Application Statistics](../profiling/how-to-attach-the-profiler-to-an-aspnet-web-application-to-collect-application-statistics-by-using-the-command-line.md) (Procedura: Connettere il profiler a un'applicazione Web ASP.NET per raccogliere statistiche dell'applicazione)|  
  
## <a name="related-tasks"></a>Attività correlate  
  
### <a name="profiling-aspnet-web-applications"></a>Profilatura di applicazioni Web ASP.NET  
  
|Attività|Contenuto correlato|  
|----------|---------------------|  
|**Sottoporre a profilatura tramite il metodo di strumentazione**|-   [Raccolta di dati di intervallo dettagliati tramite strumentazione](../profiling/collecting-detailed-timing-data-for-an-aspnet-web-application-using-the-profiler-instrumentation-method-from-the-command-line.md)|  
|**Profilatura dell'allocazione di memoria e garbage collection**|-   [Collecting Memory Data](../profiling/collecting-memory-data-from-an-aspnet-web-application-by-using-the-profiler-command-line.md) (Raccolta di dati relativi alla memoria)|  
|**Sottoporre a profilatura i conflitti di risorse e le attività dei thread**|-   [Raccolta di dati di concorrenza](../profiling/collecting-concurrency-data-for-an-aspnet-web-application-using-the-profiler-command-line.md)|  
  
### <a name="sampling-method"></a>Metodo di campionamento  
  
|Attività|Contenuto correlato|  
|----------|---------------------|  
|**Sottoporre a profilatura applicazioni client autonome**|-   [Raccolta di statistiche dell'applicazione tramite campionamento](../profiling/collecting-application-statistics-for-stand-alone-applications-by-using-the-profiler-command-line.md)|  
|-   **Sottoporre a profilatura i servizi**|-   [Raccolta di statistiche dell'applicazione tramite campionamento](../profiling/collecting-application-statistics-for-services-by-using-the-profiler-sampling-method.md)|  
  
### <a name="analyzing-sampling-data-views-and-reports"></a>Analisi di visualizzazioni dati e di report di campionamento  
 [Sampling Method Data Views](../profiling/profiler-sampling-method-data-views.md) (Visualizzazioni dei dati del metodo di campionamento)


