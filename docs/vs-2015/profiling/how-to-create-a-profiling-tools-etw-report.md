---
title: 'Procedura: Creare un report ETW degli strumenti di profilatura | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: bf5547b3-f6c7-4989-9d47-2fe4f1261444
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1901cf0800483ee4ce8ba0bce26fe3cf7ac073e6
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MTE95
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51761607"
---
# <a name="how-to-create-a-profiling-tools-etw-report"></a>Procedura: creare un rapporto ETW degli strumenti di profilatura
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Il report ETW (Event Tracing for Windows) elenca gli eventi ETW registrati in una sessione di prestazioni degli strumenti di profilatura di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. I dati ETW vengono raccolti in un file binario con estensione etl. Per altre informazioni sul report, vedere [Report ETW (Event Tracing for Windows)](../profiling/event-tracing-for-windows-etw-report.md).  
  
> [!NOTE]
>  Non è possibile visualizzare i report ETW nell'interfaccia di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
- Per informazioni su come raccogliere dati ETW usando l'interfaccia di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], vedere [Procedura: Raccogliere dati ETW (Event Tracing for Windows)](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md).  
  
- Per informazioni su come raccogliere dati ETW da un prompt dei comandi, vedere [VSPerfCmd](../profiling/vsperfcmd.md) ed [Eventi](../profiling/events-vsperfcmd.md).  
  
  Per generare il report ETW, usare il comando **VSReport/summary:etw**. Il file con estensione etl contenente i dati ETW deve trovarsi nella stessa directory del file dei dati di profilatura (con estensione vsp o vsps). Per impostazione predefinita, il report viene generato come file con valori delimitati da virgole (con estensione csv). Per altre informazioni, vedere [VSPerfReport](../profiling/vsperfreport.md).  
  
### <a name="to-generate-an-etw-report"></a>Per generare un report ETW  
  
-   In una finestra del **prompt dei comandi** digitare la riga di comando seguente:  
  
     *ToolsPath* **VSPerfReport** *VSPFile*  **/Summary:ETW [/Xml]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|Percorso dell'utilità degli strumenti di profilatura. Per altre informazioni, vedere [Specifica del percorso degli strumenti da riga di comando](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).|  
    |*VSPFile*|File (con estensione vsp o vsps) dei dati di profilatura. Sono accettati percorsi completi e parziali.|  
    |Xml|Genera un report in formato XML.|



