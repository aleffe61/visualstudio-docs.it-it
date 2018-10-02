---
title: 'Diagrammi dei componenti UML: Riferimento | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.teamarch.componentdiagram.diagram
- vs.teamarch.componentdiagram.toolbox
- vs.teamarch.UMLModelExplorer.componentdiagram
helpviewer_keywords:
- UML diagrams, component
- diagrams - modeling, component
- diagrams - modeling, UML component
- UML, component diagrams
- component diagrams
ms.assetid: 5eddff6a-892a-4c3c-9278-687ac1eccc50
caps.latest.revision: 38
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: f628ebfa84246c6d991543352f4de36a51cc7fbf
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47531888"
---
# <a name="uml-component-diagrams-reference"></a>Diagrammi dei componenti UML: riferimento
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [diagrammi dei componenti UML: riferimento](https://docs.microsoft.com/visualstudio/modeling/uml-component-diagrams-reference).  
  
In Visual Studio, un *diagramma dei componenti* vengono illustrate le parti di una progettazione di un sistema software. Un diagramma dei componenti consente di visualizzare la struttura generale del sistema e il comportamento del servizio che tali parti forniscono e utilizzano tramite le interfacce. Per creare un diagramma dei componenti UML, nelle **Architecture** menu, fare clic su **nuovo diagramma livello o UML**.  
  
 Per individuare le versioni di Visual Studio che supportano questa funzionalità, vedere [Supporto delle versioni per gli strumenti di architettura e modellazione](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).  
  
 È possibile usare un diagramma dei componenti per descrivere una progettazione implementata in qualsiasi linguaggio o stile. È necessario solo identificare le parti della progettazione che interagiscono con le altre parti della progettazione tramite un set di input e output limitato. I componenti possono essere di qualsiasi dimensione e possono essere interconnessi in qualsiasi modo.  
  
 Per altre informazioni su come usare i diagrammi dei componenti nel processo di progettazione, vedere [modellare l'architettura dell'applicazione](../modeling/model-your-app-s-architecture.md).  
  
> [!NOTE]
>  Questo argomento illustra gli elementi che è possibile usare nei diagrammi dei componenti. Per altre informazioni su come creare diagrammi dei componenti, vedere [diagrammi dei componenti UML: linee guida](../modeling/uml-component-diagrams-guidelines.md). Per altre informazioni su come creare diagrammi di modellazione in generale, vedere [modelli e diagrammi UML modifica](../modeling/edit-uml-models-and-diagrams.md).  
  
## <a name="reading-component-diagrams"></a>Lettura dei diagrammi dei componenti  
 La tabella seguente descrive gli elementi che è possibile usare in un diagramma dei componenti, insieme alle relative proprietà principali. Per un elenco completo delle proprietà degli elementi, vedere [delle proprietà degli elementi nei diagrammi dei componenti UML](../modeling/properties-of-elements-on-uml-component-diagrams.md).  
  
 ![Elementi usati nei diagrammi dei componenti](../modeling/media/uml-compovreading.png "UML_CompOvReading")  
  
|**Forma**|**Elemento**|**Descrizione e proprietà principali**|  
|---------------|-----------------|-----------------------------------------|  
|1|**Componente**|Una parte riutilizzabile della funzionalità del sistema. Un componente fornisce e utilizza il comportamento tramite le interfacce e può usare altri componenti.<br /><br /> È possibile nascondere o mostrare le parti interne di un componente usando il controllo di espansione/compressione (9).<br /><br /> Un componente è un tipo di classe.<br /><br /> -   **Is Indirectly Instantiated**. Se true (impostazione predefinita), il componente esiste solo come elemento della progettazione. In fase di esecuzione esistono solo le relative parti.|  
|2|**Porta interfaccia fornita**|Rappresenta un gruppo di messaggi o di chiamate che un componente implementa e che gli altri componenti o sistemi esterni possono usare. Una porta è una proprietà di un componente che ha un'interfaccia come tipo.|  
|3|**Porta interfaccia richiesta**|Rappresenta un gruppo di messaggi o di chiamate che il componente invia ad altri componenti o sistemi esterni. Il componente è progettato per essere associato a componenti che forniscono almeno tali operazioni. La porta ha un'interfaccia come tipo.|  
|4|**dipendenza**|Può essere usato per indicare che un'interfaccia richiesta di un componente può essere soddisfatta da un'interfaccia fornita di un altro componente.<br /><br /> Le dipendenze possono essere inoltre usate più generalmente tra gli elementi del modello, per illustrare che la progettazione di un elemento dipende dalla progettazione dell'altro.|  
|5|**Parte**|Un attributo di un componente il cui tipo è in genere un altro componente. Una parte viene usata nella progettazione interna del relativo componente padre. Le parti vengono illustrate graficamente, annidate all'interno del componente padre.<br /><br /> Per creare una parte di un tipo di componente esistente, trascinare il componente da Esplora modelli UML nel componente proprietario.<br /><br /> Per creare una parte di un nuovo tipo, scegliere il **componente** dello strumento e quindi fare clic sul componente proprietario.<br /><br /> Ad esempio, un componente `Car` contiene le parti `engine:CarEngine`, `backLeft:Wheel`, `frontRight:Wheel` e così via.<br /><br /> Più parti possono avere lo stesso tipo e componenti diversi possono avere parti dello stesso tipo.<br /><br /> -   **Tipo**. Il tipo della parte, definito in altri punti del modello. In genere, il tipo è un altro componente.<br />-   **Molteplicità**. Il valore predefinito è 1. È possibile impostarla su **0..1** per indicare che la parte può avere il valore **null**, **\*** per indicare che la parte è una raccolta di istanze del tipo specificato, o per qualsiasi espressione che può essere valutata in un intervallo di numeri.|  
|6|**Assembly parti**|Una connessione tra le porte dell'interfaccia richiesta di una parte e le porte dell'interfaccia fornita di un'altra parte. L'implementazione di un assembly delle parti può variare da un componente all'altro. Le parti connesse devono avere lo stesso componente padre.|  
|7|**Delega**|Collega una porta a un'interfaccia di una delle parti del componente. Indica che i messaggi inviati al componente vengono gestiti dalla parte o che i messaggi inviati dalla parte vengono inviati dal componente padre.|  
|(non mostrato)|**Generalizzazione**|Indica che un componente eredita da un altro componente. Le parti e le interfacce vengono ereditate.|  
|9|Controllo di compressione/espansione |Usare questo elemento per nascondere o mostrare le parti interne di un componente.|  
|(non mostrato)|**Commentoo**|Per note aggiuntive. È possibile collegare un commento a qualsiasi numero di elementi nel diagramma usando il **connettore** dello strumento.|  
  
## <a name="see-also"></a>Vedere anche  
 [Modificare modelli e diagrammi UML](../modeling/edit-uml-models-and-diagrams.md)   
 [Diagrammi dei componenti UML: linee guida](../modeling/uml-component-diagrams-guidelines.md)   
 [Convalidare il sistema durante lo sviluppo](../modeling/validate-your-system-during-development.md)   
 [Diagrammi caso di utilizzo UML: riferimento](../modeling/uml-use-case-diagrams-reference.md)   
 [Diagrammi classi UML: riferimento](../modeling/uml-class-diagrams-reference.md)   
 [Diagrammi di attività UML: riferimento](../modeling/uml-activity-diagrams-reference.md)   
 [Diagrammi di sequenza UML: riferimenti](../modeling/uml-sequence-diagrams-reference.md)


