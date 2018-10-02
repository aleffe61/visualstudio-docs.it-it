---
title: Chiave di interfacce dell'analizzatore di espressioni | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], expression evaluation
- expression evaluation, interfaces
ms.assetid: 1cac9aa3-0867-4e12-a16e-1e90abbc0fb6
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c243906346b5b20439729545765ae401e8162200
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47518496"
---
# <a name="key-expression-evaluator-interfaces"></a>Interfacce dell'analizzatore di espressioni chiave
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [interfacce dell'analizzatore di espressioni chiave](https://docs.microsoft.com/visualstudio/extensibility/debugger/key-expression-evaluator-interfaces).  
  
> [!IMPORTANT]
>  In Visual Studio 2015, questa modalità di implementazione analizzatori di espressioni è deprecata. Per informazioni sull'implementazione di analizzatori di espressioni di Common Language Runtime, vedi [analizzatori di espressioni CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) e [gestito esempio analizzatore di espressioni](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Quando si scrive un analizzatore di espressioni (EE), insieme al contesto di valutazione, è necessario avere familiarità con le interfacce seguenti.  
  
## <a name="interface-descriptions"></a>Descrizioni dell'interfaccia  
  
-   [IDebugAddress](../../extensibility/debugger/reference/idebugaddress.md)  
  
     Contiene un solo metodo, [GetAddress](../../extensibility/debugger/reference/idebugaddress-getaddress.md), che ottiene una struttura di data che rappresenta il punto di esecuzione corrente. Questa struttura di dati è uno dei tre argomenti che il motore di debug (DE) passa per la [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) metodo per valutare un'espressione. Questa interfaccia viene in genere implementata dal provider di simboli.  
  
-   [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md)  
  
     Ha il [associare](../../extensibility/debugger/reference/idebugbinder-bind.md) metodo, che ottiene l'area di memoria che contiene il valore corrente di un simbolo. Dato sia il metodo che lo contiene, rappresentato da un [IDebugObject](../../extensibility/debugger/reference/idebugobject.md) oggetto e il simbolo, rappresentato da un [IDebugField](../../extensibility/debugger/reference/idebugfield.md) oggetto `IDebugBinder::Bind` restituisce il valore del simbolo. `IDebugBinder` in genere viene implementata tramite il DE.  
  
-   [IDebugField](../../extensibility/debugger/reference/idebugfield.md)  
  
     Rappresenta un tipo di dati semplici. Per i tipi più complessi, ad esempio matrici e metodi, utilizzare derivato [IDebugArrayField](../../extensibility/debugger/reference/idebugarrayfield.md) e [IDebugMethodField](../../extensibility/debugger/reference/idebugmethodfield.md) interfacce, rispettivamente. [IDebugContainerField](../../extensibility/debugger/reference/idebugcontainerfield.md) è un'altra interfaccia derivata importante che rappresenta i simboli che contiene altri simboli, ad esempio metodi o classi. Il `IDebugField` interfaccia (e i suoi derivati) viene in genere implementate dal provider di simboli.  
  
     Un' `IDebugField` oggetto può essere usata per trovare il nome e tipo di simbolo e, insieme a un [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md) oggetto, può essere utilizzato per trovare il relativo valore.  
  
-   [IDebugObject](../../extensibility/debugger/reference/idebugobject.md)  
  
     Rappresenta i bit del valore in fase di esecuzione di un simbolo effettivi. [Associare](../../extensibility/debugger/reference/idebugbinder-bind.md) accetta un [IDebugField](../../extensibility/debugger/reference/idebugfield.md) oggetto, che rappresenta un simbolo e restituisce un' [IDebugObject](../../extensibility/debugger/reference/idebugobject.md) oggetto. Il [GetValue](../../extensibility/debugger/reference/idebugobject-getvalue.md) metodo restituisce il valore del simbolo in un buffer di memoria. In genere un CRI implementa questa interfaccia per rappresentare il valore di una proprietà in memoria.  
  
-   [IDebugExpressionEvaluator](../../extensibility/debugger/reference/idebugexpressionevaluator.md)  
  
     Questa interfaccia rappresenta l'analizzatore di espressioni se stesso. Il metodo chiave è [analizzare](../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md), che restituisce un' [IDebugParsedExpression](../../extensibility/debugger/reference/idebugparsedexpression.md) interfaccia.  
  
-   [IDebugParsedExpression](../../extensibility/debugger/reference/idebugparsedexpression.md)  
  
     Questa interfaccia rappresenta un'espressione analizzata pronta per essere valutata. Il metodo chiave è [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) che restituisce un IDebugProperty2 che rappresenta il valore e il tipo dell'espressione.  
  
-   [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md)  
  
     Questa interfaccia rappresenta un valore e il relativo tipo ed è il risultato della valutazione di un'espressione.  
  
## <a name="see-also"></a>Vedere anche  
 [Contesto di valutazione](../../extensibility/debugger/evaluation-context.md)
