---
title: IDebugMemoryBytes2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugMemoryBytes2
helpviewer_keywords:
- IDebugMemoryBytes2 interface
ms.assetid: d7647575-0e06-4190-88f5-ca40b82209a4
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8a738ecb042fa423cf165a42a9d472e06f23648d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53887185"
---
# <a name="idebugmemorybytes2"></a>IDebugMemoryBytes2
Questa interfaccia rappresenta i byte di memoria.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IDebugMemoryBytes2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Il motore di debug (DE) implementa questa interfaccia per rappresentare i byte nella memoria.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugprogram2-getmemorybytes.md) restituisce questa interfaccia per fornire l'accesso alla memoria di sistema. [GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md) e [GetMemoryBytes](../../../extensibility/debugger/reference/idebugreference2-getmemorybytes.md) restituire questa interfaccia per fornire l'accesso a byte di un oggetto.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Nella tabella seguente sono illustrati i metodi di `IDebugMemoryBytes2`.  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[ReadAt](../../../extensibility/debugger/reference/idebugmemorybytes2-readat.md)|Legge una sequenza di byte, a partire da una posizione specificata.|  
|[WriteAt](../../../extensibility/debugger/reference/idebugmemorybytes2-writeat.md)|Scrive `dwCount` byte a partire `pStartContext`.|  
|[GetSize](../../../extensibility/debugger/reference/idebugmemorybytes2-getsize.md)|Ottiene la dimensione, espressa in byte, della memoria rappresentata da questa interfaccia.|  
  
## <a name="remarks"></a>Note  
 Per le proprietà, un [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) interfaccia che rappresenta una matrice fornisce un `IDebugMemoryBytes2` interfaccia per accedere ai valori della matrice.  
  
 Visual Studio **visualizzazione per la memoria** chiamate [GetMemoryBytes](../../../extensibility/debugger/reference/idebugprogram2-getmemorybytes.md) per recuperare un `IDebugMemoryBytes2` interfaccia per l'accesso a memoria di sistema. L'indirizzo a cui accedere viene ottenuto l'analisi dell'espressione immessa come indirizzo nella visualizzazione della memoria e quindi valutando l'espressione analizzata usando [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) per ottenere un `IDebugProperty2` interfaccia. Una chiamata a [GetMemoryContext](../../../extensibility/debugger/reference/idebugproperty2-getmemorycontext.md) restituisce il [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) che descrive l'indirizzo di memoria. In questo contesto in memoria viene quindi passato a [ReadAt](../../../extensibility/debugger/reference/idebugmemorybytes2-readat.md) e [WriteAt](../../../extensibility/debugger/reference/idebugmemorybytes2-writeat.md).  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.h  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce di base](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugprogram2-getmemorybytes.md)   
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md)   
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugreference2-getmemorybytes.md)   
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)