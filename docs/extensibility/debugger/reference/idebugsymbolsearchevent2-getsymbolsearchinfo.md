---
title: IDebugSymbolSearchEvent2::GetSymbolSearchInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
helpviewer_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
ms.assetid: ae9eb72b-f2aa-43b8-87ca-da19d2e78d17
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f02eba47963dc39e7fa1fc426a762ff9f30a664d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53888699"
---
# <a name="idebugsymbolsearchevent2getsymbolsearchinfo"></a>IDebugSymbolSearchEvent2::GetSymbolSearchInfo
Chiamato da un gestore eventi per recuperare i risultati relativi a un processo di caricamento di simboli.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
HRESULT GetSymbolSearchInfo(  
   IDebugModule3**    pModule,  
   BSTR*              pbstrDebugMessage,  
   MODULE_INFO_FLAGS* pdwModuleInfoFlags  
);  
```  
  
```csharp  
int GetSymbolSearchInfo(  
   IDebugModule3              pModule,   
   ref string                 pbstrDebugMessage,   
   out enum_MODULE_INFO_FLAGS pdwModuleInfoFlags  
);  
  
```  
  
#### <a name="parameters"></a>Parametri  
 `pModule`  
 [out] Oggetto IDebugModule3 che rappresenta il modulo per il quale sono stati caricati i simboli.  
  
 `pbstrDebugMessage`  
 [in, out] Restituisce una stringa contenente eventuali messaggi di errore del modulo. Se non si verificano errori, quindi questa stringa conterrà solo il nome del modulo, ma non è mai vuota.  
  
> [!NOTE]
>  [C++] `pbstrDebugMessage` non può essere `NULL` e deve essere liberata mediante `SysFreeString`.  
  
 `pdwModuleInfoFlags`  
 [out] Una combinazione di flag dal [MODULE_INFO_FLAGS](../../../extensibility/debugger/reference/module-info-flags.md) enumerazione che indica se i simboli sono stati caricati.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 Quando un gestore riceve la [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md) evento dopo che viene effettuato un tentativo di caricare i simboli di debug per un modulo, il gestore può chiamare questo metodo per determinare i risultati di tale carico.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugModule3](../../../extensibility/debugger/reference/idebugmodule3.md)   
 [MODULE_INFO_FLAGS](../../../extensibility/debugger/reference/module-info-flags.md)   
 [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md)