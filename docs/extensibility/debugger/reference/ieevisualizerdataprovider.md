---
title: IEEVisualizerDataProvider | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEEVisualizerDataProvider
helpviewer_keywords:
- IEEVisualizerDataProvider interface
ms.assetid: 5fdfe6e3-b94e-4edb-acc5-41d8773d8ca5
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1ee69cf02bb91623e10359ea68e88cd106116ef2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53962033"
---
# <a name="ieevisualizerdataprovider"></a>IEEVisualizerDataProvider
> [!IMPORTANT]
>  In Visual Studio 2015, questa modalità di implementazione analizzatori di espressioni è deprecata. Per informazioni sull'implementazione di analizzatori di espressioni di Common Language Runtime, vedi [analizzatori di espressioni CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) e [gestito esempio analizzatore di espressioni](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Questa interfaccia offre la possibilità di modificare il valore di un oggetto tramite un visualizzatore di tipi.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IEEVisualizerDataProvider : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 L'analizzatore di espressioni implementa questa interfaccia per supportare la modifica dei dati in un oggetto di proprietà tramite un visualizzatore di tipi.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 Questa interfaccia viene utilizzata nella creazione di [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md) oggetto tramite una chiamata a [CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md). Visualizzare [visualizzazione di dati e visualizzare](../../../extensibility/debugger/visualizing-and-viewing-data.md) per altri dettagli.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[CanSetObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-cansetobjectforvisualizer.md)|Determina se è possibile aggiornare l'oggetto (e, successivamente, il relativo valore) che rappresenta questo visualizzatore.|  
|[GetNewObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-getnewobjectforvisualizer.md)|Forza una nuova valutazione dell'oggetto per questo visualizzatore.|  
|[GetObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-getobjectforvisualizer.md)|Ottiene un oggetto esistente per questo visualizzatore (non viene eseguita alcuna valutazione).|  
|[SetObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-setobjectforvisualizer.md)|Aggiorna l'oggetto per questo visualizzatore, cambiando il valore che viene visualizzato il visualizzatore.|  
  
## <a name="remarks"></a>Note  
 Il servizio Visualizzatore (come rappresentata dal [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md) l'interfaccia e restituito da [CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)) mantiene un riferimento all'oggetto che implementa il `IEEVisualizerDataProvider` interfaccia . Di conseguenza, il `IEEVisualizerDataProvider` interfaccia non deve essere implementata nello stesso oggetto che implementa le [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) se quell'oggetto mantiene un riferimento al `IEEVisualizerService` oggetto: i risultati di un riferimento circolare e un un deadlock si verifica quando gli oggetti vengono eliminati definitivamente. L'approccio consigliato consiste nell'implementare `IEEVisualizerDataProvider` in un oggetto separato a cui il `IDebugProperty2` delegati senza chiamare il metodo dell'oggetto `IUnknown::AddRef` su di esso.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: ee.h  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce di valutazione di espressioni](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)   
 [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)   
 [Visualizzazione di tipi e dati](../../../extensibility/debugger/visualizing-and-viewing-data.md)