---
title: IDebugFunctionObject2::CreateObject | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IDebugFunctionObject2::CreateObject
- CreateObject
ms.assetid: 148de615-941e-4b64-ab11-75b692aae465
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 64b6c069abe04f25e7aa82b579cf4d905686dcf4
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51770523"
---
# <a name="idebugfunctionobject2createobject"></a>IDebugFunctionObject2::CreateObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Crea un oggetto che usa un costruttore base impostazioni dei flag di valutazione e un valore di timeout.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT CreateObject (  
   IDebugFunctionObject* pConstructor,  
   DWORD                 dwArgs,  
   IDebugObject*         pArgs[],  
   DWORD                 dwEvalFlags,  
   DWORD                 dwTimeout,  
   IDebugObject**        ppObject  
);  
```  
  
```csharp  
int CreateObject (  
   IDebugFunctionObject pConstructor,  
   uint                 dwArgs,  
   IDebugObject[]       pArgs,  
   uint                 dwEvalFlags,  
   uint                 dwTimeout,  
   out IDebugObject**   ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pConstructor`  
 [in] Un' [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) oggetto che rappresenta il costruttore dell'oggetto da creare.  
  
 `dwArgs`  
 [in] Il numero di parametri in di `pArg` matrice. Rappresenta il numero di parametri passati al costruttore.  
  
 `pArgs`  
 [in] Matrice di [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) gli oggetti che rappresenta i parametri passati al costruttore.  
  
 `dwEvalFlags`  
 [in] Una combinazione di flag dal [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) enumerazione che specificano come deve essere eseguita la valutazione.  
  
 `dwTimeout`  
 [in] Tempo massimo, espresso in millisecondi, di attesa prima della restituzione da questo metodo. Uso **infinito** per un'attesa indefinita.  
  
 `ppObject`  
 [out] Restituisce un **IDebugObject** che rappresenta l'oggetto appena creato.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 Chiamare questo metodo per creare un oggetto che rappresenta un'istanza di una classe o un altro tipo complesso che richiede un costruttore, che è un parametro.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugFunctionObject2](../../../extensibility/debugger/reference/idebugfunctionobject2.md)

