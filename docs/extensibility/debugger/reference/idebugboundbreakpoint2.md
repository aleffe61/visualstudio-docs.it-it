---
title: IDebugBoundBreakpoint2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBoundBreakpoint2
helpviewer_keywords:
- IDebugBoundBreakpoint2 interface
ms.assetid: df33c52e-ded2-48a0-951d-1f36c8fc922e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9d745bfb4682f92995145cc28967e416baaec35a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53950843"
---
# <a name="idebugboundbreakpoint2"></a>IDebugBoundBreakpoint2
Questa interfaccia rappresenta un punto di interruzione che è associato a un percorso di codice.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IDebugBoundBreakpoint2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Il motore di debug (DE) implementa questa interfaccia come parte del supporto per i punti di interruzione.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Una chiamata a [associare](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) crea questa interfaccia. Le chiamate a [GetBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getbreakpoint.md) e [successivo](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-next.md) anche possibile ottenere questa interfaccia.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Nella tabella seguente sono illustrati i metodi di `IDebugBoundBreakpoint2`.  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getpendingbreakpoint.md)|Ottiene il punto di interruzione in sospeso da cui è stato creato il punto di interruzione associato specificato.|  
|[GetState](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getstate.md)|Ottiene lo stato del punto di interruzione associato.|  
|[GetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-gethitcount.md)|Ottiene il numero di passaggi corrente per questo punto di interruzione associato.|  
|[GetBreakpointResolution](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getbreakpointresolution.md)|Ottiene la risoluzione di punto di interruzione che descrive il punto di interruzione.|  
|[Enable](../../../extensibility/debugger/reference/idebugboundbreakpoint2-enable.md)|Abilita o disabilita il punto di interruzione.|  
|[SetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-sethitcount.md)|Imposta il numero di passaggi per questo punto di interruzione associato.|  
|[SetCondition](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setcondition.md)|Imposta o modifica la condizione associata a questo punto di interruzione associato.|  
|[SetPassCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setpasscount.md)|Imposta o modifica il numero di sessione associato a questo punto di interruzione associato.|  
|[Eliminazione](../../../extensibility/debugger/reference/idebugboundbreakpoint2-delete.md)|Elimina il punto di interruzione.|  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.h  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [GetBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getbreakpoint.md)   
 [Avanti](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-next.md)   
 [Bind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)