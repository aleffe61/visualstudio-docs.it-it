---
title: CV_call_e | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- CV_call_e enumeration
ms.assetid: f230560b-4243-432d-8f19-46df112043b9
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8d4d001b1c6c2df10b8263fa9b0c5f5be360c9e9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519015"
---
# <a name="cvcalle"></a>CV_call_e
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [CV_call_e](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/cv-call-e).  
  
Specifica la convenzione di chiamata per una funzione.  
  
> [!NOTE]
>  Solo i valori di enumerazione più comuni sono documentati qui. L'enumerazione completo è disponibile nel file di intestazione cvconst.h.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
typedef enum CV_call_e {   
   CV_CALL_NEAR_C    = 0x00,  
   CV_CALL_NEAR_FAST = 0x04,  
   CV_CALL_NEAR_STD  = 0x07,  
   CV_CALL_NEAR_SYS  = 0x09,  
   CV_CALL_THISCALL  = 0x0b,  
   CV_CALL_CLRCALL   = 0x16  
} CV_call_e;  
```  
  
## <a name="elements"></a>Elementi  
 CV_CALL_NEAR_C  
 Specifica una convenzione di chiamata di funzioni con un push quasi di destra a sinistra. La funzione chiamante Cancella lo stack.  
  
 CV_CALL_NEAR_FAST  
 Specifica una convenzione di chiamata di funzioni con un push da sinistra a destra quasi registri. La funzione chiamata viene utilizzata la somma dei byte di parametro per cancellare lo stack.  
  
 CV_CALL_NEAR_STD  
 Specifica una convenzione di chiamata di funzione tramite una chiamata standard quasi (right-to-left push).  
  
 CV_CALL_NEAR_SYS  
 Specifica una convenzione di chiamata di funzione tramite una chiamata di sistema quasi.  
  
 CV_CALL_THISCALL  
 Specifica una convenzione di chiamata di funzioni usando `this` chiamare (`this` puntatore passati nel registro).  
  
 CV_CALL_CLRCALL  
 Specifica una convenzione di chiamata di funzioni usata da Common Language Runtime (CLR) (noto anche come un codice gestito convenzione di chiamata).  
  
## <a name="remarks"></a>Note  
 I valori di questa enumerazione vengono restituiti da una chiamata per il [Get_callingconvention](../../debugger/debug-interface-access/idiasymbol-get-callingconvention.md) (metodo).  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: cvconst.h  
  
## <a name="see-also"></a>Vedere anche  
 [Enumerazioni e strutture](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaSymbol::get_callingConvention](../../debugger/debug-interface-access/idiasymbol-get-callingconvention.md)


