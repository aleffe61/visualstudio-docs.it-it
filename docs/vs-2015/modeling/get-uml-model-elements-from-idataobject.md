---
title: Ottenere gli elementi del modello UML da IDataObject | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- UML API, copy and paste
ms.assetid: e0b9cec8-3b93-4a24-8bd3-3e086501d387
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: a560ce5116c52b8c2e83ce9b28252f060e2485f1
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51782076"
---
# <a name="get-uml-model-elements-from-idataobject"></a>Ottenere elementi di modelli UML da IDataObject
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Quando l'utente trascina elementi da qualsiasi origine in un diagramma, gli elementi trascinati vengono codificati in un oggetto `System.Windows.Forms.IDataObject`. La codifica dipende dal tipo di oggetto di origine. Nel frammento seguente viene illustrato come recuperare gli elementi quando l'origine è un diagramma UML.  
  
> [!NOTE]
>  La maggior parte delle operazioni che è necessario eseguire per i modelli UML può essere eseguita usando i tipi in definiti negli assembly **VisualStudio. ArchitectureTools** e  **Microsoft**. Tuttavia, a tale scopo, è necessario usare alcune classi che fanno parte dell'implementazione di strumenti di modellazione UML. Ad esempio, `ShapeElement` in questo frammento non equivale a `IShape` UML. Per ridurre il rischio di collocare il modello UML e diagrammi in uno stato incoerente, è preferibile evitare di usare i metodi su queste classi di implementazione, a eccezione dei casi in cui non è disponibile alcuna alternativa.  
  
## <a name="code-sample"></a>Esempio di codice  
 Il progetto deve fare riferimento a quanto segue [!INCLUDE[TLA2#tla_net](../includes/tla2sharptla-net-md.md)] assembly:  
  
 **Microsoft.VisualStudio.Modeling.Sdk. [versione]**  
  
 **Microsoft.VisualStudio.Modeling.Sdk.Diagrams. [versione]**  
  
 **Forms**  
  
```  
using Microsoft.VisualStudio.Modeling;    
  // for ElementGroupPrototype  
using Microsoft.VisualStudio.Modeling.Diagrams;    
  // for ShapeElement, DiagramDragEventArgs, DiagramPointEventArgs  
…   
  /// <summary>  
  /// Retrieves UML IElements from drag arguments.  
  /// Works for drags from UML diagrams.  
  /// </summary>  
  private IEnumerable<IElement> GetModelElementsFromDragEvent  
                  (DiagramDragEventArgs dragEvent)  
  {  
     //ElementGroupPrototype is the container for  
     //dragged and copied elements and toolbox items.  
     ElementGroupPrototype prototype =  
        dragEvent.Data.  
        GetData(typeof(ElementGroupPrototype))  
                     as ElementGroupPrototype;  
     // Locate the originals in the implementation store.  
     IElementDirectory implementationDirectory =   
        dragEvent.DiagramClientView.Diagram.Store.ElementDirectory;  
  
     return  prototype.ProtoElements.Select(  
       prototypeElement =>   
       {  
          ModelElement element = implementationDirectory  
                .FindElement(prototypeElement.ElementId);  
          ShapeElement shapeElement = element as ShapeElement;  
          if (shapeElement != null)  
          {   
            // Dragged from a diagram.  
            return shapeElement.ModelElement as IElement;  
          }  
          else  
          {   
            // Dragged from UML Model Explorer.  
            return element as IElement;  
          }  
        });  
    }  
```  
  
 Per altre informazioni sulle `ElementGroupPrototype` e il `Store` in cui vengono implementati gli strumenti di modellazione UML, vedere [Modeling SDK per Visual Studio - Domain-Specific Language](../modeling/modeling-sdk-for-visual-studio-domain-specific-languages.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Programmazione con l'API UML](../modeling/programming-with-the-uml-api.md)   
 [Definire un comando di menu in un diagramma di modellazione](../modeling/define-a-menu-command-on-a-modeling-diagram.md)



