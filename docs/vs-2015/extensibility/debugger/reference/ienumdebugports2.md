---
title: IEnumDebugPorts2 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IEnumDebugPorts2
helpviewer_keywords:
- IEnumDebugPorts2
ms.assetid: 1754eef3-cf62-42e0-b218-1911acba77d4
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 678784d8ee9a15099e4c46554e2c1451936611d8
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51750608"
---
# <a name="ienumdebugports2"></a>IEnumDebugPorts2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Questa interfaccia consente di enumerare le porte di un fornitore di computer o la porta.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IEnumDebugPorts2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Un fornitore di porte personalizzato implementa questa interfaccia per rappresentare un elenco delle porte create dal fornitore. Visual Studio implementa questa interfaccia per supportare il proprio fornitore della porta.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Chiamare [EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md) per ottenere questa interfaccia che rappresenta un elenco delle porte create dal fornitore della porta. Chiamare [EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md) per ottenere questa interfaccia che rappresenta un elenco di porte che sono stati salvati su disco.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Nella tabella seguente sono illustrati i metodi di `IEnumDebugPorts2`.  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[avanti](../../../extensibility/debugger/reference/ienumdebugports2-next.md)|Recupera un determinato numero di porte in una sequenza di enumerazione.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugports2-skip.md)|Ignora un determinato numero di porte in una sequenza di enumerazione.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugports2-reset.md)|Reimposta una sequenza di enumerazione all'inizio.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugports2-clone.md)|Crea un enumeratore che contiene lo stesso stato di enumerazione dell'enumeratore corrente.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugports2-getcount.md)|Ottiene il numero di porte in un enumeratore.|  
  
## <a name="remarks"></a>Note  
 Visual Studio Usa questa interfaccia per consentire di popolare un elenco di porte usate per la connessione a processi.  
  
 Un motore di debug non usa in genere questa interfaccia.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce di base](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumPorts](../../../extensibility/debugger/reference/idebugcoreserver2-enumports.md)   
 [EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md)

