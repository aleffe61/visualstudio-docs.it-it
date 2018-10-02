---
title: Funzioni Hook del blocco client | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.hooks
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- client blocks, validating and reporting data
- debugging [C++], hook functions
- _CrtSetDumpClient function
- client blocks, hook functions
- hooks, client block
ms.assetid: f21c197e-565d-4e3f-9b27-4c018c9b87fc
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 29bbfb24566a59047e47090f92a040c3c2fe8a12
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47526292"
---
# <a name="client-block-hook-functions"></a>Funzioni hook del blocco client
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [funzioni Hook del blocco Client](https://docs.microsoft.com/visualstudio/debugger/client-block-hook-functions).  
  
Se si desidera convalidare o inserire in report il contenuto dei dati memorizzati in blocchi `_CLIENT_BLOCK`, sarà possibile scrivere una funzione specificamente per tale scopo. Tale funzione dovrà avere un prototipo analogo al seguente, come definito in CRTDBG.H:  
  
```  
void YourClientDump(void *, size_t)  
  
```  
  
 In altre parole, la funzione di hook dovrà accettare un **void** puntatore all'inizio del blocco di allocazione, insieme a un **size_t** tipo valore che indica la dimensione dell'allocazione e restituire `void`. Non esistono altre limitazioni al contenuto.  
  
 Dopo aver installato la funzione hook mediante [CrtSetDumpClient](http://msdn.microsoft.com/library/f3dd06d0-c331-4a12-b68d-25378d112033), verrà chiamato ogni volta che un `_CLIENT_BLOCK` dump di blocco. È quindi possibile usare [CrtReportBlockType](http://msdn.microsoft.com/library/0f4b9da7-bebb-4956-9541-b2581640ec6b) per ottenere informazioni sul tipo o sul sottotipo dei blocchi di dump;.  
  
 Il puntatore alla funzione che viene passato a `_CrtSetDumpClient` JE typu **CRT_DUMP_CLIENT**, come definito in CRTDBG. H:  
  
```  
typedef void (__cdecl *_CRT_DUMP_CLIENT)  
   (void *, size_t);  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Scrittura di funzioni Hook di debug](../debugger/debug-hook-function-writing.md)   
 [Esempio crt_dbg2](http://msdn.microsoft.com/en-us/21e1346a-6a17-4f57-b275-c76813089167)   
 [_CrtReportBlockType](http://msdn.microsoft.com/library/0f4b9da7-bebb-4956-9541-b2581640ec6b)


