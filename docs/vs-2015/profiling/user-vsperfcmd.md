---
title: User (VSPerfCmd) | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ee1a478e-374d-4f30-ae28-d260b9d4723a
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b6c201253fe6952bed0657d54f8cc91eb60fbba6
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51760029"
---
# <a name="user-vsperfcmd"></a>User (VSPerfCmd)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

L'opzione **User** specifica il dominio e il nome utente dell'account proprietario del processo profilato. Questa opzione è obbligatoria solo se il processo è in esecuzione come utente diverso dall'utente connesso. Il proprietario del processo è elencato nella colonna Nome utente nella scheda Processi di Gestione attività di Windows.  
  
 Il **utente** opzione può essere specificata solo in una riga di comando che contiene anche le **avviare** opzione.  
  
## <a name="syntax"></a>Sintassi  
  
```  
VSPerfCmd.exe /Start:Method /Output:FileName /User:[Domain\]UserName [Options]  
```  
  
#### <a name="parameters"></a>Parametri  
 `Domain`  
 Nome del dominio dell'utente.  
  
 `UserName`  
 Nome dell'utente.  
  
## <a name="required-options"></a>Opzioni obbligatorie  
 L'opzione **User** può essere usata solo con l'opzione **Start**.  
  
 **Start:** `Method`  
 Inizializza il profiler sul metodo di profilatura specificato.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente illustra l'uso dell'opzione **User**.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /User:SYSTEM  
```  
  
## <a name="see-also"></a>Vedere anche  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profilatura di applicazioni autonome](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profilatura di applicazioni Web ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profilatura di servizi](../profiling/command-line-profiling-of-services.md)



