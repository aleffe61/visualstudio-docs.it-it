---
title: LineOff | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 76082063-20ef-47ae-ad64-81b43b654865
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5fc5ad3e2256b32e32e02814d41168663e3539ff
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53926122"
---
# <a name="lineoff"></a>LineOff
Per impostazione predefinita, il profiler raccoglie i dati dei numeri di riga del codice sorgente e i dati di offset dei numeri di riga quando si usa il metodo di campionamento per la profilatura. L'opzione **LineOff** di VSPerfCmd disabilita la raccolta dei dati dei numeri di riga quando VSPerfCmd viene usato per avviare l'applicazione. I dati di profilatura vengono raccolti a livello di funzione quando si specifica l'opzione **LineOff**.  
  
 È possibile usare **LineOff** solo con l'opzione **Launch** e solo quando il profiler è stato inizializzato per eseguire il campionamento tramite l'opzione **Start**:**Sample**.  
  
## <a name="syntax"></a>Sintassi  
  
```cmd  
VSPerfCmd.exe /Launch:AppName /LineOff [Options]  
```  
  
#### <a name="parameters"></a>Parametri  
 nessuno  
  
## <a name="required-options"></a>Opzioni obbligatorie  
 L'opzione **LineOff** può essere usata solo su una riga di comando che contiene l'opzione **Launch**.  
  
 **Launch:** `AppName`  
 Avvia l'applicazione specificata e inizia la profilatura con il metodo di campionamento.  
  
## <a name="example"></a>Esempio  
 Questo esempio illustra come avviare l'applicazione e il profiler e quindi disabilitare il campionamento a livello di riga.  
  
```cmd  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe /LineOff  
```  
  
## <a name="see-also"></a>Vedere anche  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Sottoporre a profilatura applicazioni autonome](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Sottoporre a profilatura applicazioni Web ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Sottoporre a profilatura i servizi](../profiling/command-line-profiling-of-services.md)