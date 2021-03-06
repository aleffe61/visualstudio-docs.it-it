---
title: WinCounter | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ff319ffc-f249-4c3f-9eb2-06e392e3ae80
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 51cb5aa0a41f311ea9c24a4ed512d6df4fe2e10f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53875219"
---
# <a name="wincounter"></a>WinCounter
L'opzione **WinCounter** specifica un contatore delle prestazioni di Windows o di un'applicazione per la raccolta di dati a intervalli prestabiliti durante l'esecuzione della profilatura. I contatori delle prestazioni di Windows e dell'applicazione sono elencati come contrassegni nel file di dati di profilatura. È possibile specificare più contatori delle prestazioni da raccogliere in opzioni separate.  
  
 Per impostazione predefinita, i dati dei contatori vengono raccolti ogni 500 millisecondi. Usare l'opzione **AutoMark** per specificare un intervallo di raccolta diverso.  
  
 È possibile usare una sola opzione **AutoMark**. Se vengono specificate più opzioni **AutoMark**, viene usata l'ultima.  
  
 L'opzione **WinCounter** può essere usata solo con l'opzione **Start**.  
  
## <a name="syntax"></a>Sintassi  
  
```cmd  
VSPerfCmd.exe /Start:Method /Wincounter:Path [/WinCounter:Path] [AutoMark:Milliseconds] [Options]  
```  
  
#### <a name="parameters"></a>Parametri  
 `Path`  
 Contatore delle prestazioni di Windows nel formato del percorso del contatore PDH.  
  
## <a name="required-options"></a>Opzioni obbligatorie  
 L'opzione **WinCounter** può essere usata solo con l'opzione **Start**.  
  
 **Start:** `Method`  
 L'opzione **Start** inizializza il profiler sul metodo di profilatura specificato.  
  
## <a name="exclusive-options"></a>Opzioni esclusive  
 L'opzione **AutoMark** può essere usata solo con l'opzione **WinCounter**.  
  
 **AutoMark:** `Milliseconds`  
 Specifica il numero di millisecondi tra le raccolte di dati dei contatori delle prestazioni di Windows.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente viene impostata la raccolta dei dati di due contatori delle prestazioni di Windows a intervalli di 1000 millisecondi.  
  
```cmd  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /WinCounter:"\Processor(0)\% Processor Time" /WinCounter:"\System\Context Switches/sec" /AutoMark:1000  
```  
  
## <a name="see-also"></a>Vedere anche  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Sottoporre a profilatura applicazioni autonome](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Sottoporre a profilatura applicazioni Web ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Sottoporre a profilatura i servizi](../profiling/command-line-profiling-of-services.md)