---
title: Esplorare relazioni con l'API UML | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- UML API
ms.assetid: a4d11d45-b8c0-40f9-a597-363f07659610
caps.latest.revision: 15
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: 3ae6da2980c55df6eb58686fcdb2c364b9147779
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47525343"
---
# <a name="navigate-relationships-with-the-uml-api"></a>Esplorare relazioni con l'API UML
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [esplorare relazioni con l'API UML](https://docs.microsoft.com/visualstudio/modeling/navigate-relationships-with-the-uml-api).  
  
Un modello è costituito da elementi collegati da tipi diversi di relazioni. In questo argomento viene descritto come esplorare il modello nel codice programma.  
  
## <a name="traversing-relationships"></a>Attraversamento di relazioni  
  
### <a name="any-relationship"></a>Qualsiasi relazione  
 Usare `GetRelatedElements<T>()` per cercare tutti gli elementi collegati a un elemento specificato. Impostare `T` su `IRelationship` per attraversare le relazioni di tutti i tipi o usare un tipo più specifico come `IAssociation` per attraversare solo tale tipo.  
  
```  
IElement anElement;  
// Select all elements related to anElement.  
Context.CurrentDiagram.SelectShapes (  
   anElement.GetRelatedElements<IRelationship>()  
    .SelectMany(e=>e.Shapes()).ToArray());  
  
```  
  
 Usare `GetRelatedLinks<T>()` per individuare tutte le relazioni collegate a un elemento.  
  
```  
// Process all relationships connected to an element.  
foreach (IRelationship relationship in   
   anElement.GetRelatedLinks<IRelationship>())  
{  
  Debug.Assert(relationship.SourceElement == anElement  
      || relationship.TargetElement == anElement);  
}  
  
```  
  
### <a name="association"></a>Associazione  
 Un'associazione è una relazione tra due proprietà, ognuna delle quali appartiene a un classificatore.  
  
```  
IClassifier classifier; // class, interface, component, actor, ...  
// Get all the associations sourced from this classifier  
foreach (IProperty p in classifier.GetOutgoingAssociationEnds())  
{  
  // p represents the end further end of an association.  
  IType oppositeElement = p.Type;   
    // The type to which this association connects classifier  
  
  IProperty oppositeProperty = p.Opposite;  
    // The nearer end of the association.  
  Debug.Assert(oppositeProperty.Type == classifier);  
  IAssociation association = p.Association;  
  Debug.Assert(association.MemberEnds.Contains(p)  
     && association.MemberEnds.Contains(oppositeProperty));  
}  
```  
  
### <a name="generalization-and-realization"></a>Generalizzazione e realizzazione  
 Accedere alle estremità opposte della generalizzazione:  
  
```  
foreach (IClassifier supertype in classifier.Generals) {…}  
foreach (IClassifier subtype in classifier.GetSpecifics()) {…}  
Access the relationship itself:  
foreach (IGeneralization gen in classifier.Generalizations)   
{ Debug.Assert(classifier == gen.Specific); }  
```  
  
```  
  
/// InterfaceRealization:  
IEnumerable<IInterface> GetRealizedInterfaces  
    (this IBehavioredClassifier classifier);  
IEnumerable<IBehavioredClassifier> GetRealizingClassifiers  
    (this IInterface interface);  
  
```  
  
### <a name="dependency"></a>Dipendenza  
  
```  
/// Returns the elements depending on this element  
IEnumerable<INamedElement> GetDependencyClients(this INamedElement element);   
/// Returns the elements this element depends on  
IEnumerable<INamedElement> INamedElement GetDependencySuppliers(this INamedElement element);  
  
```  
  
### <a name="activity-edge"></a>Activity Edge  
  
```  
/// Returns the nodes targeted by edges outgoing from this one  
IEnumerable<IActivityNode> GetActivityEdgeTargets(this IActivityNode node);  
/// Returns the nodes sourcing edges incoming to this one  
IEnumerable<IActivityNode> GetActivityEdgeSources(this IActivityNode node);  
  
```  
  
### <a name="connector-assembly-and-delegation"></a>Connettore (assembly e delega)  
  
```  
/// Returns the elements connected via assembly   
/// or delegation to this one  
IEnumerable<IConnectableElement> GetConnectedElements(this IConnectableElement element);  
  
```  
  
### <a name="messages-and-lifelines"></a>Messaggi e linee di vita  
  
```  
IEnumerable<IMessage> GetAllOutgoingMessages(this ILifeline  lifeline);   
// both from lifeline and execution occurrences  
IEnumerable<IMessage> GetAllIncomingMessages(this ILifeline  lifeline);  
ILifeline GetSourceLifeline(this IMessage message);   
    // may return null for found messages  
ILifeline GetTargetLifeline(this IMessage message);    
    // may return null for lost messages  
  
```  
  
### <a name="package-import"></a>Importazione pacchetto  
  
```  
IEnumerable<IPackage>GetImportedPackages(this INamespace namespace);  
IEnumerable<INamespace> GetImportingNamespaces(this IPackage package);  
  
```  
  
### <a name="use-case-extend-and-include"></a>Caso di utilizzo di inclusione ed estensione  
  
```  
IEnumerable<IUseCase>GetExtendedCases(this IUseCase usecase);  
IEnumerable<IUseCase>GetExtendingCases(this IUseCase usecase);  
IEnumerable<IUseCase>GetIncludedCases(this IUseCase usecase);  
IEnumerable<IUseCase>GetIncludingCases(this IUseCase usecase);  
```  
  
## <a name="enumerating-relationships"></a>Enumerazione delle relazioni  
 Tutte le proprietà del modello UML che restituiscono più valori sono conformi all'interfaccia IEnumerable <>. Ciò significa che è possibile usare [espressioni di Query Linq](http://go.microsoft.com/fwlink/?LinkId=168834) e i metodi di estensione definiti nel **System. Linq** dello spazio dei nomi.  
  
 Ad esempio:  
  
```  
from shape in     Context.CurrentDiagram.GetSelectedShapes<IClassifier>()  
where shape.Color == System.Drawing.Color.Red  
select shape.Element  
  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Estendere modelli e diagrammi UML](../modeling/extend-uml-models-and-diagrams.md)   
 [Esplorare il modello UML](../modeling/navigate-the-uml-model.md)


