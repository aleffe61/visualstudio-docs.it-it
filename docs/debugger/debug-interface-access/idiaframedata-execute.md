---
title: Idiaframedata | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::execute method
ms.assetid: 7a6c7d03-1ff1-4059-bd54-5f407eeebc26
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 66b8f904ac8add69db0c6d1760b5427cb8c802ae
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49918356"
---
# <a name="idiaframedataexecute"></a>IDiaFrameData::execute
Esegue la rimozione dello stack e restituisce i risultati in un'interfaccia di frame dello stack del percorso.  
  
## <a name="syntax"></a>Sintassi  
  
```C++  
HRESULT execute (   
   IDiaStackWalkFrame* frame  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `frame`  
 [in] Un' [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md) oggetto che contiene lo stato dei registri di frame.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore. Nella tabella seguente mostra i valori restituiti possibili per questo metodo.  
  
|Valore|Descrizione|  
|-----------|-----------------|  
|E_DIA_INPROLOG|Non è possibile eseguire uno stack frame nel codice di prologo.|  
|E_DIA_SYNTAX|Analizzare l'errore nel programma di frame.|  
|E_DIA_FRAME_ACCESS|Non è possibile registri di accesso o la memoria.|  
|E_DIA_VALUE|Errore nel calcolo di un valore (ad esempio, la divisione per zero).|  
  
## <a name="remarks"></a>Note  
 Questo metodo viene chiamato durante il debug di rimozione dello stack. Il [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md) oggetto viene implementato dall'applicazione client per ricevere gli aggiornamenti per i registri e fornire i metodi utilizzati dal `execute` (metodo).  
  
## <a name="see-also"></a>Vedere anche  
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)   
 [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md)