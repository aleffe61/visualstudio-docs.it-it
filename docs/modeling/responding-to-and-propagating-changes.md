---
title: Risposta alle modifiche e propagazione delle modifiche
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, events
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: ace1873c45ba8437ba929ec10ef75db3d0d50bf2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53905202"
---
# <a name="responding-to-and-propagating-changes"></a>Risposta alle modifiche e propagazione delle modifiche
Quando un elemento viene creato, eliminato o aggiornato, è possibile scrivere codice che propaga le modifiche ad altre parti del modello o a risorse esterne, ad esempio file, database o altri componenti.

## <a name="in-this-section"></a>In questa sezione
 Come indicazione generale, prendere in considerazione queste tecniche nell'ordine seguente:

|Tecnica|Scenari|Per altre informazioni|
|-|-|-|
|Definire una valore calcolato della proprietà di dominio.|Una proprietà di dominio il cui valore viene calcolato da altre proprietà nel modello. Ad esempio, un prezzo che rappresenta la somma dei prezzi degli elementi correlati.|[Proprietà di archiviazione calcolate e personalizzate](../modeling/calculated-and-custom-storage-properties.md)|
|Definire una proprietà di dominio di archiviazione personalizzati.|Una proprietà di dominio archiviata in altre parti del modello o esternamente. È ad esempio, è stato possibile analizzare una stringa di espressione in una struttura ad albero del modello.|[Proprietà di archiviazione calcolate e personalizzate](../modeling/calculated-and-custom-storage-properties.md)|
|Eseguire l'override di gestori di modifica, ad esempio OnDeleting e OnValueChanging|Mantenere sincronizzati i vari elementi e mantenere i valori esterni sincronizzato con il modello.<br /><br /> Vincolare i valori per gli intervalli definiti.<br /><br /> Chiamato immediatamente prima e dopo il valore della proprietà e altre modifiche. È possibile terminare la modifica generando un'eccezione.|[Gestori di modifica del valore delle proprietà del dominio](../modeling/domain-property-value-change-handlers.md)|
|Regole|È possibile definire regole che vengono accodate per l'esecuzione subito prima della fine di una transazione in cui si è verificata una modifica. Questi non vengono eseguiti su annullamento o ripristino. Usarli per mantenere sincronizzati con l'altro una parte dell'archivio.|[Le regole propagano le modifiche all'interno del modello](../modeling/rules-propagate-changes-within-the-model.md)|
|Eventi di Store|L'archivio di modellazione fornisce notifiche degli eventi, ad esempio aggiungendo o eliminando un elemento o un collegamento o la modifica del valore di una proprietà. L'evento viene anche eseguita in annullamento e ripristino. Usare gli eventi di archiviazione per aggiornare i valori che non sono presenti nell'archivio.|[I gestori eventi propagano le modifiche al di fuori del modello](../modeling/event-handlers-propagate-changes-outside-the-model.md)|
|Eventi .NET|Le forme dispongono di gestori di eventi che rispondono al clic del mouse e altri movimenti. È necessario registrarsi per questi eventi per ogni oggetto. La registrazione avviene in genere di una sostituzione di InitializeInstanceResources e deve essere eseguita per ogni elemento.<br /><br /> Questi eventi si verificano in genere all'esterno di una transazione.|[Procedura: Intercettare un clic su una forma o un elemento Decorator](../modeling/how-to-intercept-a-click-on-a-shape-or-decorator.md)|
|Regole dei limiti|Regola bounds viene utilizzata in particolare per vincolare i limiti della forma.|[Le regole associate (BoundsRules) vincolano posizione e dimensione delle forme](../modeling/boundsrules-constrain-shape-location-and-size.md)|
|Regole di selezione|Le regole di selezione in modo specifico vincolano ciò che l'utente può selezionare.|[Procedura: Accedere e vincolare la selezione corrente](../modeling/how-to-access-and-constrain-the-current-selection.md)|
|OnAssocatedPropertyChanged|Indicare gli stati degli elementi del modello usando le funzionalità di forme e connettori, ad esempio shadow, frecce, colore e larghezza della linea e stile.|[Aggiornamento di forme e di connettori per riflettere il modello](../modeling/updating-shapes-and-connectors-to-reflect-the-model.md)|

## <a name="comparing-rules-and-store-events"></a>**Le regole di confrontare e gli eventi di Store**
 Modifica notificanti, regole e gli eventi vengono eseguiti quando vengono apportate in un modello.

 Le regole vengono in genere applicate alla transazione end in cui si è verificata la modifica e gli eventi vengono applicati dopo il commit delle modifiche in una transazione.

 Usare gli eventi di archiviazione per sincronizzare il modello con gli oggetti di fuori di Store e le regole per mantenere la coerenza all'interno di Store.

-   **Creazione di regole personalizzate** è creare una regola personalizzata come una classe derivata da una regola astratta. È anche necessario segnalare al framework relativa alla regola personalizzata. Per altre informazioni, vedere [le regole propagano le modifiche all'interno di the Model](../modeling/rules-propagate-changes-within-the-model.md).

-   **Sottoscrizione di eventi** prima di richiedere a un evento, creare un gestore dell'evento e delegato. Usare quindi il <xref:Microsoft.VisualStudio.Modeling.Store.EventManagerDirectory%2A>proprietà per sottoscrivere l'evento. Per altre informazioni, vedere [gestori di propagare le modifiche di fuori il modello di eventi](../modeling/event-handlers-propagate-changes-outside-the-model.md).

-   **Annullamento delle modifiche** quando si annulla una transazione, gli eventi vengono generati, ma non vengono applicate le regole. Se una regola viene modificato un valore e si annulla la modifica, il valore viene reimpostato sul valore originale durante l'operazione di annullamento. Quando viene generato un evento, è necessario modificare manualmente il valore relativo valore originale. Per altre informazioni su transactons e di annullamento, vedere [come: Utilizzare le transazioni per aggiornare il modello](../modeling/how-to-use-transactions-to-update-the-model.md).

-   **Il passaggio di argomenti dell'evento a regole ed eventi** entrambi gli eventi e le regole vengono passate un `EventArgs` parametro che contiene informazioni su come il modello modificato.

## <a name="see-also"></a>Vedere anche

- [Procedura: Intercettare un clic su una forma o un elemento Decorator](../modeling/how-to-intercept-a-click-on-a-shape-or-decorator.md)
- [Scrittura di codice per personalizzare un linguaggio specifico di dominio](../modeling/writing-code-to-customise-a-domain-specific-language.md)