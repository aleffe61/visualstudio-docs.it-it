---
title: IDebugObject2 | Microsoft Docs
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
- IDebugObject2
helpviewer_keywords:
- IDebugObject2 interface
ms.assetid: ef640967-8adb-4793-994d-ae1736510891
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: fd5ecc632675e13a6e0c4a6dd3ffaa3680408e3a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47540583"
---
# <a name="idebugobject2"></a>IDebugObject2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [IDebugObject2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugobject2).  
  
> [!IMPORTANT]
>  In Visual Studio 2015, questa modalità di implementazione analizzatori di espressioni è deprecata. Per informazioni sull'implementazione di analizzatori di espressioni di Common Language Runtime, vedi [analizzatori di espressioni CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) e [gestito esempio analizzatore di espressioni](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Questa interfaccia fornisce informazioni aggiuntive su un oggetto.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IDebugObject2 : IDebugObject  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 L'analizzatore di espressioni implementa questa interfaccia per offre il supporto per gli alias e l'accesso alle informazioni sull'oggetto.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Un' [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) interfaccia può ottenere questa interfaccia tramite [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3). È inoltre [GetObject](../../../extensibility/debugger/reference/idebugalias-getobject.md) restituisce questa interfaccia.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
 Oltre ai metodi nel [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) interfaccia, il `IDebugObject2` interfaccia implementa quanto segue:  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[GetBackingFieldForProperty](../../../extensibility/debugger/reference/idebugobject2-getbackingfieldforproperty.md)|Ottiene il campo o una variabile (se presente) che può essere supporta la proprietà rappresentata da questo oggetto.|  
|[GetICorDebugValue](../../../extensibility/debugger/reference/idebugobject2-geticordebugvalue.md)|Ottiene l'oggetto di codice gestito che rappresenta il valore di questo oggetto.|  
|[CreateAlias](../../../extensibility/debugger/reference/idebugobject2-createalias.md)|Restituisce un alias esistente o crea un ID univoco per questo oggetto.|  
|[GetAlias](../../../extensibility/debugger/reference/idebugobject2-getalias.md)|Ottiene l'alias associato all'oggetto, se presente.|  
|[GetField](../../../extensibility/debugger/reference/idebugobject2-getfield.md)|Ottiene il tipo di questo oggetto.|  
|[IsUserData](../../../extensibility/debugger/reference/idebugobject2-isuserdata.md)|Determina se questo oggetto rappresenta i dati dell'utente.|  
|[IsEncOutdated](../../../extensibility/debugger/reference/idebugobject2-isencoutdated.md)|Determina se lo stato di modifica e continuazione non è più valido.<br /><br /> Un analizzatore di espressioni personalizzato può neimplementuje metodu questo metodo (l'app deve sempre restituire `E_NOTIMPL`).|  
  
## <a name="remarks"></a>Note  
 Visualizzare [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md) per una discussione sugli alias.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce di valutazione di espressioni](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)   
 [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)   
 [GetObject](../../../extensibility/debugger/reference/idebugalias-getobject.md)
