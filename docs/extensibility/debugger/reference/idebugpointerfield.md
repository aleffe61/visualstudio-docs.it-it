---
title: IDebugPointerField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPointerField
helpviewer_keywords:
- IDebugPointerField interface
ms.assetid: d51bd5b2-f18e-4e27-b4fb-e6f652fbf635
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7fc686af78b4ac787abef1c0c52309e82c47376b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947894"
---
# <a name="idebugpointerfield"></a>IDebugPointerField
Questa interfaccia rappresenta un tipo di puntatore.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IDebugPointerField : IDebugContainerField  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Il provider di simboli implementa questa interfaccia per rappresentare un puntatore.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Uso [QueryInterface](/cpp/atl/queryinterface) per ottenere questa interfaccia dalle [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) interfaccia se [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) restituisce `FIELD_TYPE_POINTER`.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Oltre ai metodi nel `IDebugField` e `IDebugContainerField` interfacce, questa interfaccia implementa il metodo seguente:  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[GetDereferencedField](../../../extensibility/debugger/reference/idebugpointerfield-getdereferencedfield.md)|Restituisce un [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) che descrive la destinazione dell'indicatore di misura.|  
  
## <a name="remarks"></a>Note  
 In C/C++, un puntatore può essere un contenitore, se viene usato con la notazione di matrice. Ad esempio, dato `char *pString`, `pString` dispone di un tipo di puntatore a `char`. `pString[3]` ha il tipo di un contenitore che è un puntatore a `char` che fa riferimento il quarto elemento di tale contenitore.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: sh.h  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce del Provider di simboli](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)