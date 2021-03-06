---
title: IDebugObject::IsEqual | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugObject::IsEqual
helpviewer_keywords:
- IDebugObject::IsEqual method
ms.assetid: 4b76e663-ef2e-41ff-9be1-bf26d666a34a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c5f928d2fc845f6dbab99504d0967e11e7a51142
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53878153"
---
# <a name="idebugobjectisequal"></a>IDebugObject::IsEqual
Confronta un oggetto con questo oggetto.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
HRESULT IsEqual(   
   IDebugObject* pObject,  
   BOOL*         pfIsEqual  
);  
```  
  
```csharp  
int IsEqual(  
   IDebugObject pObject,  
   out int      pfIsEqual  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pObject`  
 [in] Un' [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) che rappresenta l'oggetto da confrontare con l'oggetto.  
  
 `pfIsEqual`  
 [out] Restituisce diverso da zero (`TRUE`) se i valori degli oggetti sono uguali; in caso contrario, restituisce zero (`FALSE`).  
  
## <a name="return-value"></a>Valore restituito  
 Se l'operazione riesce, restituisce S_OK; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 In genere, questo metodo può confrontare gli indirizzi dei valori rappresentati dal `pObject` parametro e ciò [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) oggetto; se gli indirizzi sono uguali, quindi gli oggetti possono essere considerati uguali.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)