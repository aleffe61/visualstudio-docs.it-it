---
title: Creazione di file dei dati di profilatura portabili tramite la riga di comando | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 2ceb63a7-b835-4988-b756-2afc3fcc4808
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: be919183f18efc29ea562b0e4cc60c84febe60c8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49841936"
---
# <a name="create-portable-profiling-data-files-from-the-command-line"></a>Creare file dei dati di profilatura portabili dalla riga di comando
Per semplificare la condivisione dei dati di profilatura, è possibile usare lo strumento da riga di comando [VSPerfReport](../profiling/vsperfreport.md) per incorporare i simboli di un'esecuzione della profilatura nel file con estensione *vsp*.  
  
 È anche possibile creare un file di dati di profilatura preanalizzato (con estensione *vsps*), più piccolo e più rapido da caricare nell'IDE.  
  
> [!NOTE]
>  Verificare che i file di simboli (con estensione *pdb*) siano disponibili per **VSPerfReport**. Per altre informazioni, vedere [Procedura: Specificare percorsi dei file di simboli dalla riga di comando](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md).  
>   
>  Per informazioni sul percorso di **VSReport**, vedere [Specificare il percorso degli strumenti da riga di comando](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  
>   
>  Non è possibile filtrare i dati di profilatura di un file con estensione *vsps*.  
  
### <a name="to-embed-the-symbols-for-a-profiling-run-into-a-profiling-data-vsp-file"></a>Per incorporare i simboli per un'esecuzione della profilatura in un file di dati di profilatura (con estensione *vsp*)  
  
- In una finestra del prompt dei comandi, digitare il comando seguente:  
  
   \<percorso><strong>VSPerfReport \<</strong>file VSP> **/PackSymbols**  
  
   Per impostazione predefinita, il file con estensione *vsps* è denominato con il nome base del file con estensione *vsp*. È possibile specificare un nome alternativo con l'opzione **Output**.  
  
### <a name="to-create-a-summary-profiling-data-file"></a>Per creare un file di riepilogo dati di profilatura  
  
- In una finestra del prompt dei comandi, digitare il comando seguente:  
  
   \<percorso><strong>VSPerfReport \<</strong>file VSP> **/SummaryFile** [**/Output:**\<nome file>]  
  
   Per impostazione predefinita, il file con estensione *vsps* è denominato con il nome base del file con estensione *vsp*. È possibile specificare un nome alternativo con l'opzione **Output**.