---
title: Spazio dei nomi diagnostic | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic
helpviewer_keywords:
- Concurrency::diagnostic namespace
ms.assetid: ad786b19-7c4c-46ee-bfb6-c4752b373a09
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d781bbfefa59b2e124cf76c11b8fd7c06cc66dda
ms.sourcegitcommit: 4cd4aef53e7035d23e7d1d0f66f51ac8480622a1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2018
ms.locfileid: "34764670"
---
# <a name="diagnostic-namespace"></a>Spazio dei nomi diagnostic
Lo spazio dei nomi `diagnostics` offre funzionalità per l'emissione di marcatori del visualizzatore di concorrenza.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
namespace diagnostic;  
```  
  
## <a name="members"></a>Membri  
  
### <a name="classes"></a>Classi  
  
|nome|Descrizione|  
|----------|-----------------|  
|[Classe marker_series](../profiling/marker-series-class.md)|Rappresenta un canale seriale di eventi generati da un singolo provider.|  
|[Classe span](../profiling/span-class.md)|Definisce una fase dell'applicazione.|  
  
### <a name="enumerations"></a>Enumerazioni  
  
|nome|Descrizione|  
|----------|-----------------|  
|[Enumerazione marker_importance](../profiling/marker-importance-enumeration.md)|Rappresenta il livello di importanza di un marcatore del visualizzatore di concorrenza.|  
  
## <a name="requirements"></a>Requisiti  
 **Intestazione:** *cvmarkersobj.h*  
  
 **Spazio dei nomi:** Concurrency  
  
## <a name="see-also"></a>Vedere anche  
 [Spazio dei nomi Concurrency (visualizzatore di concorrenza)](../profiling/concurrency-namespace-concurrency-visualizer.md)