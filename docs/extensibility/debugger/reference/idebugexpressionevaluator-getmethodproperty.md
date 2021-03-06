---
title: IDebugExpressionEvaluator::GetMethodProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugExpressionEvaluator::GetMethodProperty
helpviewer_keywords:
- IDebugExpressionEvaluator::GetMethodProperty method
ms.assetid: c394fe4d-eeb6-4feb-828c-098d84a6f1ba
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a0569c3e6a3d79279533c1c1c6717e8e5c3ce059
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53820774"
---
# <a name="idebugexpressionevaluatorgetmethodproperty"></a>IDebugExpressionEvaluator::GetMethodProperty
Questo metodo ottiene un oggetto di proprietà che contiene le variabili locali, argomenti e altre proprietà di un metodo.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
HRESULT GetMethodProperty(   
   IDebugSymbolProvider* pSymbolProvider,  
   IDebugAddress*        pAddress,  
   IDebugBinder*         pBinder,  
   BOOL                  fIncludeHiddenLocals,  
   IDebugProperty2**     ppProperty  
);  
```  
  
```csharp  
int GetMethodProperty(  
   IDebugSymbolProvider pSymbolProvider,   
   IDebugAddress        pAddress,   
   IDebugBinder         pBinder,   
   int                  fIncludeHiddenLocals,   
   out IDebugProperty2  ppProperty  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pSymbolProvider`  
 [in] Il provider di simboli da utilizzare, espresse come una [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) oggetto.  
  
 `pAddress`  
 [in] L'indirizzo nel codice, espresso come un [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) oggetto, che deve essere risolta nel più vicino che contiene funzioni.  
  
 `pBinder`  
 [in] Lo strumento di associazione da utilizzare, espresse come una [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) oggetto.  
  
 `fIncludeHiddenLocals`  
 [in] Diverso da zero (`TRUE`) significa che includere variabili locali nascosti; zero (`FALSE`) significa che non inserire nascosti variabili locali  
  
 `ppProperty`  
 [out] Restituisce un [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) oggetto che rappresenta il metodo.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 Variabili locali nascosti sono in genere le variabili che vengono generate dal compilatore.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)   
 [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)   
 [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)