---
title: IEnumDebugThreads2 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IEnumDebugThreads2
helpviewer_keywords:
- IEnumDebugThreads2
ms.assetid: 1854f078-3b49-42c2-b65b-33e3b506fd63
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 96a86c322ed2fa1ac750171116a0a11c9b2b4d99
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47520249"
---
# <a name="ienumdebugthreads2"></a>IEnumDebugThreads2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [IEnumDebugThreads2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/ienumdebugthreads2).  
  
Questo Interfacc enumera i thread in esecuzione nella sessione di debug corrente.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IEnumDebugThreads2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Il motore di debug (DE) implementa questa interfaccia per rappresentare un elenco di thread in un programma.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Chiamare [EnumThreads](../../../extensibility/debugger/reference/idebugprocess2-enumthreads.md) per ottenere questa interfaccia che rappresenta un elenco di tutti i thread in tutti i programmi in esecuzione in un processo. Chiamare [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md) per ottenere questa interfaccia che rappresenta un elenco di thread in esecuzione in un programma.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Nella tabella seguente sono illustrati i metodi di `IEnumDebugThreads2`.  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[avanti](../../../extensibility/debugger/reference/ienumdebugthreads2-next.md)|Recupera un determinato numero di thread nella sequenza di enumerazione.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugthreads2-skip.md)|Ignora un determinato numero di thread in una sequenza di enumerazione.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugthreads2-reset.md)|Reimposta una sequenza di enumerazione all'inizio.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugthreads2-clone.md)|Crea un enumeratore che contiene lo stesso stato di enumerazione di quello corrente.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugthreads2-getcount.md)|Ottiene il numero di thread in un enumeratore.|  
  
## <a name="remarks"></a>Note  
 Visual Studio ottiene in genere questa interfaccia per aggiornare il **thread** finestra anche per ottenere il primo thread dell'elenco, per poter chiamare [Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md), [continua](../../../extensibility/debugger/reference/idebugprocess3-continue.md), e [Passaggio](../../../extensibility/debugger/reference/idebugprocess3-step.md).  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce di base](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprocess2-enumthreads.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md)   
 [Passaggio](../../../extensibility/debugger/reference/idebugprocess3-step.md)   
 [Continuare](../../../extensibility/debugger/reference/idebugprocess3-continue.md)   
 [Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)
