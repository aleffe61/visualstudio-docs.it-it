---
title: IDebugField::GetKind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugField::GetKind
helpviewer_keywords:
- IDebugField::GetKind method
ms.assetid: e7c9c60a-8e55-4ecc-aa63-0c814a1e92cc
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 06c830656aca630e3dec11d59e7a553668cbed8b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53950894"
---
# <a name="idebugfieldgetkind"></a>IDebugField::GetKind
Questo metodo ottiene il tipo di campo.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
HRESULT GetKind(   
   FIELD_KIND* pdwKind  
);  
```  
  
```csharp  
int GetKind(  
   out enum_FIELD_KIND pdwKind  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pdwKind`  
 [out] Restituisce il tipo del campo come una combinazione di [FIELD_KIND](../../../extensibility/debugger/reference/field-kind.md) costanti.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [FIELD_KIND](../../../extensibility/debugger/reference/field-kind.md)