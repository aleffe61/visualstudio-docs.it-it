---
title: IDebugEngineProgram2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugEngineProgram2
helpviewer_keywords:
- IDebugEngineProgram2 interface
ms.assetid: 151003a9-2e4d-4acf-9f4d-365dfa6b9596
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 33f1d88eaa7fe6cce34f4b386998ecc68cfe4953
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53934479"
---
# <a name="idebugengineprogram2"></a>IDebugEngineProgram2
Questa interfaccia fornisce supporto per il debug multithreading.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IDebugEngineProgram2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Un motore di debug implementa questa interfaccia per supportare il debug simultaneo di più thread. Questa interfaccia viene implementata nello stesso oggetto che implementa il [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) interfaccia.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Uso [QueryInterface](/cpp/atl/queryinterface) per ottenere questa interfaccia da un `IDebugProgram2` interfaccia.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Nella tabella seguente sono illustrati i metodi di `IDebugEngineProgram2`.  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[Stop](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md)|Arresta tutti i thread in esecuzione in questo programma.|  
|[WatchForThreadStep](../../../extensibility/debugger/reference/idebugengineprogram2-watchforthreadstep.md)|Verifica la presenza di esecuzione (o arresto la visione per l'esecuzione) venga eseguita il thread specificato.|  
|[WatchForExpressionEvaluationOnThread](../../../extensibility/debugger/reference/idebugengineprogram2-watchforexpressionevaluationonthread.md)|Consente o non consente la valutazione dell'espressione si verifica sul thread specificato, anche se il programma viene arrestato.|  
  
## <a name="remarks"></a>Note  
 Visual Studio chiama questa interfaccia in risposta a un [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md) eventi e impostare gli stati "Watch per passaggio Thread" e "Watch per espressione di valutazione nel Thread" del programma. [Arrestare](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md) viene chiamato ogni volta che è necessario arrestare il programma; questo metodo consente il programma di terminare tutti i thread.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.h  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)