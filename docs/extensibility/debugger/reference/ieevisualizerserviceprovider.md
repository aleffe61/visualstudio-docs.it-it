---
title: IEEVisualizerServiceProvider | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEEVisualizerServiceProvider
helpviewer_keywords:
- IEEVisualizerServiceProvider interface
ms.assetid: 859d1a51-1c65-4c8b-ae74-3b74b181ebcd
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ed17748a2c635de5b4a4b715d4061ee3841f18ac
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53990438"
---
# <a name="ieevisualizerserviceprovider"></a>IEEVisualizerServiceProvider
> [!IMPORTANT]
>  In Visual Studio 2015, questa modalità di implementazione analizzatori di espressioni è deprecata. Per informazioni sull'implementazione di analizzatori di espressioni di Common Language Runtime, vedi [analizzatori di espressioni CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) e [gestito esempio analizzatore di espressioni](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Questa interfaccia consente di accedere a un metodo che consente di creare un servizio del visualizzatore, che consente di gestire le attività del Visualizzatore di tipo per l'IDE.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IEEVisualizerServiceProvider : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Note per gli implementatori  
 Visual Studio implementa questa interfaccia per creare un oggetto servizio del visualizzatore, che a sua volta viene utilizzato per fornire gli ID di classe (`CLSID`s) di visualizzatori di tipi per l'IDE di Visual Studio.  
  
## <a name="notes-for-callers"></a>Note per i chiamanti  
 L'analizzatore di espressioni (EE) chiama [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md) per ottenere questa interfaccia.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)|Crea il servizio Visualizzatore|  
  
## <a name="remarks"></a>Note  
 Il `IEEVisualizerServiceProvider` ottenuta durante l'implementazione dell'interfaccia [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md). Il servizio visualizzatore che consente di creare questa interfaccia viene usato per fornire funzionalità a un' [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) interfaccia, che l'analizzatore di Espressioni è responsabile dell'implementazione. L'analizzatore di Espressioni è inoltre responsabile dell'implementazione un' [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md) interfaccia che consente i visualizzatori di tipo visualizzare e modificare un valore della proprietà.  
  
 Visualizzare [visualizzazione di dati e visualizzare](../../../extensibility/debugger/visualizing-and-viewing-data.md) per informazioni dettagliate sull'interagiscono di queste interfacce.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: ee.h  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Interfacce di valutazione di espressioni](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)   
 [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)   
 [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md)   
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [Visualizzazione di tipi e dati](../../../extensibility/debugger/visualizing-and-viewing-data.md)