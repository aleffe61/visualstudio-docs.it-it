---
title: Versioni di debug delle funzioni di allocazione Heap | Microsoft Docs
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
- vs.debug.crt
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- _CRTDBG_MAP_ALLOC macro
- debugging [CRT], heap allocation functions
- debugging memory leaks, CRT debug library functions
- malloc function
- memory leaks, CRT debug library functions
- heap allocation, debug
- _malloc_dbg function
ms.assetid: 91748bdc-f4cd-4d8b-ab98-0493dab7ed0d
caps.latest.revision: 20
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f7a649d8afd3ae7bf7d6d9abff98734ac96e05cd
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51802100"
---
# <a name="debug-versions-of-heap-allocation-functions"></a>Versioni di debug di funzioni di allocazione heap
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La libreria di runtime del linguaggio C contiene speciali versioni di debug delle funzioni di allocazione heap. Queste funzioni presentano lo stesso nome delle corrispondenti versioni di rilascio, con l'unica differenza del suffisso _dbg. Questo argomento illustra le differenze tra la versione di rilascio di una funzione CRT e la versione _dbg, utilizzando `malloc` e `_malloc_dbg` come esempi.  
  
 Quando [debug](http://msdn.microsoft.com/library/a9901568-4846-4731-a404-399d947e2e7a) è definito, CRT associa tutte [malloc](http://msdn.microsoft.com/library/144fcee2-be34-4a03-bb7e-ed6d4b99eea0) le chiamate a [malloc_dbg](http://msdn.microsoft.com/library/c97eca51-140b-4461-8bd2-28965b49ecdb). Pertanto non è necessario riscrivere il codice utilizzando `_malloc_dbg` anziché `malloc` per sfruttarne i vantaggi durante il debug.  
  
 È tuttavia possibile chiamare `_malloc_dbg` esplicitamente. La chiamata esplicita di `_malloc_dbg` presenta alcuni vantaggi supplementari:  
  
- Registrazione delle allocazioni del tipo `_CLIENT_BLOCK`.  
  
- Memorizzazione del file sorgente e del numero di riga nel punto in cui ha avuto luogo la richiesta di allocazione.  
  
  Se non si desidera convertire le `malloc` le chiamate a `_malloc_dbg`, è possibile ottenere le informazioni sul file di origine definendo [CRTDBG_MAP_ALLOC](http://msdn.microsoft.com/library/435242b8-caea-4063-b765-4a608200312b), in modo che il preprocessore associa direttamente tutte le chiamate a `malloc` a `_malloc_dbg` anziché basarsi su un wrapper `malloc`.  
  
  Per registrare i tipi separati di allocazioni in blocchi client, è necessario chiamare `_malloc_dbg` direttamente e impostare il parametro `blockType` su `_CLIENT_BLOCK`.  
  
  Quando debug non è definito, le chiamate a `malloc` non vengono disturbate, le chiamate a `_malloc_dbg` vengono risolte `malloc`, la definizione di [CRTDBG_MAP_ALLOC](http://msdn.microsoft.com/library/435242b8-caea-4063-b765-4a608200312b) viene ignorato e che riguardano le informazioni di file di origine di richiesta di allocazione non è disponibile. Dal momento che `malloc` non presenta alcun parametro di tipo di blocco, le richieste di tipi `_CLIENT_BLOCK` vengono gestite come allocazioni standard.  
  
## <a name="see-also"></a>Vedere anche  
 [Tecniche di debug CRT](../debugger/crt-debugging-techniques.md)



