---
title: IDebugPortSupplier2 | Microsoft Docs
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
- IDebugPortSupplier2
helpviewer_keywords:
- IDebugPortSupplier2 interface
ms.assetid: 37067324-2ea6-4a01-8829-a6e9c7a70068
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0a95613477e36dc352b6e393d3d1652a25080452
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519989"
---
# <a name="idebugportsupplier2"></a>IDebugPortSupplier2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [IDebugPortSupplier2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugportsupplier2).  
  
Questa interfaccia fornisce porte al gestore di sessione di debug (SDM).  
  
## <a name="syntax"></a>Sintassi  
  
```  
IDebugPortSupplier2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Un fornitore di porte personalizzato implementa questa interfaccia per rappresentare un fornitore di porte.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Una chiamata a `CoCreateInstance` con un fornitore di porte `GUID` restituisce questa interfaccia (questo è il modo consueto per ottenere questa interfaccia). Ad esempio:  
  
```cpp#  
IDebugPortSupplier2 *GetPortSupplier(GUID *pPortSupplierGuid)  
{  
    IDebugPortSupplier2 *pPS = NULL;  
    if (pPortSupplierGuid != NULL) {  
        CComPtr<IDebugPortSupplier2> spPortSupplier;  
        spPortSupplier.CoCreateInstance(*pPortSupplierGuid);  
        if (spPortSupplier != NULL) {  
            pPS = spPortSupplier.Detach();  
        }  
    }  
    return (pPS);  
}  
```  
  
 Una chiamata a [GetPortSupplier](../../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md) restituisce questa interfaccia, che rappresenta il fornitore della porta corrente usato da [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)].  
  
 [GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md) restituisce questa interfaccia, che rappresenta il fornitore della porta che ha creato la porta.  
  
 [IEnumDebugPortSuppliers2](../../../extensibility/debugger/reference/ienumdebugportsuppliers2.md) rappresenta un elenco di `IDebugPortSupplier` interfacce (il `IEnumDebugPortSuppliers` interfaccia viene ottenuta dal [EnumPortSuppliers](../../../extensibility/debugger/reference/idebugcoreserver2-enumportsuppliers.md), che rappresentano tutti i fornitori di porte registrate con [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)]).  
  
 Un motore di debug in genere non interagisce con un fornitore di porte.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Nella tabella seguente sono illustrati i metodi di `IDebugPortSupplier2`.  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[GetPortSupplierName](../../../extensibility/debugger/reference/idebugportsupplier2-getportsuppliername.md)|Ottiene il nome fornitore della porta.|  
|[GetPortSupplierId](../../../extensibility/debugger/reference/idebugportsupplier2-getportsupplierid.md)|Ottiene l'identificatore fornitore di porte.|  
|[GetPort](../../../extensibility/debugger/reference/idebugportsupplier2-getport.md)|Ottiene una porta da un fornitore di porte.|  
|[EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md)|Enumera le porte già esistenti.|  
|[CanAddPort](../../../extensibility/debugger/reference/idebugportsupplier2-canaddport.md)|Verifica che un fornitore di porte supporta l'aggiunta di nuove porte.|  
|[AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)|Aggiunge una porta.|  
|[RemovePort](../../../extensibility/debugger/reference/idebugportsupplier2-removeport.md)|Rimuove una porta.|  
  
## <a name="remarks"></a>Note  
 Un fornitore di porte può identificarsi per nome e ID, aggiungere e rimuovere le porte ed enumerare tutte le porte che fornisce il fornitore della porta.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce di base](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md)   
 [GetPortSupplier](../../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md)   
 [IEnumDebugPortSuppliers2](../../../extensibility/debugger/reference/ienumdebugportsuppliers2.md)
