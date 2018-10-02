---
title: RemoveFromCollection&lt;T&gt; ActivityDesigner | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.RemoveFromCollection`1.UI
ms.assetid: 6617ba26-c8bc-4aed-b746-112bf490d288
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 9cb791c64909cf8c494b5c5b3dc481f106dc8cf1
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47529412"
---
# <a name="removefromcollectionlttgt-activity-designer"></a>RemoveFromCollection&lt;T&gt; ActivityDesigner
Il **RemoveFromCollection\<T >** ActivityDesigner viene utilizzato per creare e configurare un <xref:System.Activities.Statements.RemoveFromCollection%601> attività.  
  
## <a name="the-removefromcollectiont-activity"></a>RemoveFromCollection\<T > attività  
 L'attività <xref:System.Activities.Statements.RemoveFromCollection%601> rimuove un determinato elemento da una raccolta specifica.  
  
### <a name="using-the-removefromcollectiont-activity-designer"></a>Usando RemoveFromCollection\<T > ActivityDesigner  
 Il **RemoveFromCollection\<T >** ActivityDesigner è reperibile nella **raccolta** categoria del **casella degli strumenti**, accessibile facendo clic la **Casella degli strumenti** scheda [!INCLUDE[wfd2](../includes/wfd2-md.md)] (in alternativa, selezionare **sulla barra degli strumenti** dal **visualizzazione** menu oppure premere CTRL + ALT + X.)  
  
 Il **RemoveFromCollection\<T >** ActivityDesigner può essere trascinato dal **casella degli strumenti** e rilasciarlo al [!INCLUDE[wfd2](../includes/wfd2-md.md)] superficie ovunque posizionate le attività vengono in genere, ad esempio all'interno di un <xref:System.Activities.Statements.Sequence>. Ciò consente di creare un <xref:System.Activities.Statements.RemoveFromCollection%601> attività con un valore predefinito <xref:System.Activities.Activity.DisplayName%2A> removefromcollection\<Int32 >. Il <xref:System.Activities.Activity.DisplayName%2A> possibile modificare il valore nell'intestazione del **RemoveFromCollection\<T >** ActivityDesigner o nel **DisplayName** finestra della griglia delle proprietà. Le altre proprietà devono essere modificate nella griglia delle proprietà.  
  
### <a name="the-removefromcollectiont-properties"></a>RemoveFromCollection\<T > proprietà  
 Nella tabella seguente sono elencate le proprietà di <xref:System.Activities.Statements.RemoveFromCollection%601> e ne viene descritta la modalità di utilizzo nella finestra di progettazione.  
  
|Nome proprietà|Obbligatorio|Utilizzo|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Nome descrittivo facoltativo dell'attività <xref:System.Activities.Statements.RemoveFromCollection%601>. Il valore predefinito è RemoveFromCollection\<Int32 >.<br /><br /> Sebbene la proprietà <xref:System.Activities.Activity.DisplayName%2A> non sia obbligatoria, se ne consiglia l'uso.|  
|<xref:System.Activities.Statements.RemoveFromCollection%601.Item%2A>|True|L'elemento da aggiungere per il **Collection\<T >**. Questo elemento è di tipo *T*, che è di tipo *TypeArgument*. Per specificare l'elemento, digitare un'espressione Visual Basic nella griglia delle proprietà.|  
|<xref:System.Activities.Statements.RemoveFromCollection%601.Collection%2A>|True|Raccolta alla quale aggiungere l'elemento. Questa raccolta è di tipo **ICollection\<TypeArgument >.** Per specificare la raccolta, digitare un'espressione Visual Basic nella griglia delle proprietà.|  
|*TypeArgument*|True|Tipo T degli elementi contenuti in <xref:System.Collections.Generic.ICollection%601>. Per impostazione predefinita, ciò *TypeArgument* è impostato su **Int32**. Per modificare il tipo, modificare il valore della *TypeArgument* nella casella combinata nella griglia delle proprietà.|  
|<xref:System.Activities.Activity%601.Result%2A>|False|Valore che indica se l'elemento specificato è stato rimosso dalla raccolta. Per specificare una variabile da associare al risultato, digitare una variabile Visual Basic nella griglia delle proprietà.|  
  
## <a name="see-also"></a>Vedere anche  
 [Raccolta](../workflow-designer/collection-activity-designers.md)   
 [AddToCollection\<T >](../workflow-designer/addtocollection-t-activity-designer.md)   
 [ClearCollection\<T >](../workflow-designer/clearcollection-t-activity-designer.md)   
 [ExistsInCollection\<T>](../workflow-designer/existsincollection-t-activity-designer.md)