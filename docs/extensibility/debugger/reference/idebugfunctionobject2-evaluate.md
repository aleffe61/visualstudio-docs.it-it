---
title: IDebugFunctionObject2::Evaluate | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugFunctionObject2::Evaluate
ms.assetid: bc54c652-904b-4297-a6db-faa329684881
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f785e698e0c73146e4b80838d815c300bffa7abc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53991217"
---
# <a name="idebugfunctionobject2evaluate"></a>IDebugFunctionObject2::Evaluate
Chiama la funzione e restituisce il valore risultante come oggetto.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
HRESULT Evaluate (  
   IDebugObject** ppParams,  
   DWORD          dwParams,  
   DWORD          dwEvalFlags,  
   DWORD          dwTimeout,  
   IDebugObject** ppResult  
);  
```  
  
```csharp  
int Evaluate (  
   IDebugObject     ppParams,  
   uint             dwParams,  
   uint             dwEvalFlags,  
   uint             dwTimeout,  
   out IDebugObject ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `ppParams`  
 [in] Matrice di [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) gli oggetti che rappresentano i parametri di input. Ognuno di questi parametri è stato creato utilizzando uno dei metodi Create in questa interfaccia.  
  
 `dwParams`  
 [in] Il numero di parametri in di `ppParams` matrice.  
  
 `dwEvalFlags`  
 [in] Una combinazione di flag dal [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) enumerazione che specificano come deve essere eseguita la valutazione.  
  
 `dwTimeout`  
 [in] Specifica il tempo massimo, espresso in millisecondi, di attesa prima della restituzione da questo metodo. Uso **infinito** per un'attesa indefinita.  
  
 `ppResult`  
 [out] Restituisce un **IDebugObject** che rappresenta il valore della funzione sotto forma di oggetto.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugFunctionObject2](../../../extensibility/debugger/reference/idebugfunctionobject2.md)