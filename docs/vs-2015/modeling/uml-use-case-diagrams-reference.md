---
title: 'Diagrammi caso di utilizzo UML: Riferimento | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.teamarch.usecasediagram.toolbox
- vs.teamarch.usecasediagram.diagram
- vs.teamarch.UMLModelExplorer.usecasediagram
helpviewer_keywords:
- diagrams - modeling, use case
- UML, use case diagrams
- diagrams - modeling, UML use case
- use case diagrams
- UML diagrams, use case
ms.assetid: aa15772b-eb67-4366-b145-b559112817df
caps.latest.revision: 35
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 64eece28fc46fce799eff01e7ed1e7302e939dbc
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51791762"
---
# <a name="uml-use-case-diagrams-reference"></a>Diagrammi casi d'uso UML: riferimento
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

In Visual Studio, un *diagramma caso di utilizzo* riepiloga gli utenti che utilizzano l'applicazione o il sistema e ciò che è possibile eseguire. Per creare un diagramma caso di utilizzo UML nel **Architecture** menu, fare clic su **nuovo diagramma livello o UML**.  
  
 Un diagramma caso di utilizzo è incentrato sulla descrizione dei requisiti dell'utente. Illustra le relazioni tra requisiti, utenti e componenti principali. Non descrive però i requisiti in dettaglio, i quali vengono illustrati in diagrammi o documenti separati da poter collegare a ogni caso di utilizzo. Per informazioni su come diagrammi casi d'uso consentono di comprendere, illustrare e comunicare le esigenze degli utenti, vedere [modellare i requisiti utente](../modeling/model-user-requirements.md).  
  
 Per individuare le versioni di Visual Studio che supportano questa funzionalità, vedere [Supporto delle versioni per gli strumenti di architettura e modellazione](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).  
  
> [!NOTE]
>  In questo argomento vengono illustrati gli elementi disponibili in diagrammi caso di utilizzo. Per altre informazioni su come creare diagrammi casi d'uso, vedere [diagrammi caso di utilizzo UML: linee guida](../modeling/uml-use-case-diagrams-guidelines.md). Per altre informazioni su come creare e disegnare diagrammi di modellazione, vedere [modelli e diagrammi UML modifica](../modeling/edit-uml-models-and-diagrams.md).  
  
## <a name="reading-use-case-diagrams"></a>Lettura di diagrammi caso di utilizzo  
 Le tabelle nelle sezioni seguenti descrivono gli elementi disponibili in un diagramma caso di utilizzo oltre alle relative proprietà principali. Per un elenco completo delle proprietà, vedere [diagrammi caso d'usano delle proprietà degli elementi su UML](../modeling/properties-of-elements-on-uml-use-case-diagrams.md).  
  
### <a name="actors-use-cases-and-subsystems"></a>Attori, casi di utilizzo e sottosistemi  
 ![Gli elementi in un diagramma caso di utilizzo](../modeling/media/uml-ucovactor.png "UML_UCOvActor")  
  
|**Forma**|**Elemento**|**Descrizione e proprietà principali**|  
|---------------|-----------------|-----------------------------------------|  
|1|**attore**|Rappresenta un utente, un'organizzazione o un sistema esterno che interagisce con l'applicazione o il sistema. Un attore è un tipo di elemento.<br /><br /> -   **Image Path** -il percorso del file di immagine che deve essere usato invece l'icona predefinita dell'attore. L'icona deve essere un file di risorse all'interno del progetto di Visual Studio.|  
|2|**Caso d'uso**|Rappresenta le azioni eseguite da uno o più attori per il perseguimento di un obiettivo specifico. Un caso di utilizzo è un tipo di elemento.<br /><br /> -   **Argomenti** -il sottosistema in cui viene visualizzato il caso d'uso.|  
|3|**Associazione**|Indica che un attore partecipa a un caso di utilizzo.|  
|4|**Sottosistema o componente**|L'applicazione o il sistema in cui si sta lavorando o una parte di esso. Può essere una rete di grandi dimensioni o una singola classe di un'applicazione.<br /><br /> I casi di utilizzo supportati da un sistema o un componente vengono visualizzati all'interno del rettangolo. Può essere utile illustrare alcuni casi di utilizzo all'esterno del rettangolo per chiarire l'ambito del sistema.<br /><br /> Un sottosistema in un diagramma caso di utilizzo ha fondamentalmente lo stesso tipo di un componente in un diagramma dei componenti.<br /><br /> -   **È Indirectly Instantiated** : se false, il sistema in esecuzione contiene uno o più oggetti che corrispondono direttamente a questo sottosistema. Se true, il sottosistema è un costrutto nella progettazione visualizzato nel sistema in esecuzione solo tramite la creazione di istanze delle relative parti costituenti.|  
  
### <a name="structuring-use-cases"></a>Strutturazione dei casi di utilizzo  
 ![Casi d'uso con Includi, Estendi e generalizzazione](../modeling/media/uml-ucovstructure.png "UML_UCOvStructure")  
  
|Forma|**Elemento**|Descrizione|  
|-----------|-----------------|-----------------|  
|5|**includere**|Un caso di utilizzo di inclusione chiama il caso di utilizzo incluso. L'inclusione viene usata per mostrare come un caso di utilizzo venga suddiviso in passaggi più piccoli. Il caso di utilizzo incluso viene inserito all'estremità della freccia.<br /><br /> Si noti che il diagramma non mostra l'ordine dei passaggi. È possibile usare un diagramma di attività, un diagramma di sequenza o un altro documento per descrivere questi dettagli.|  
|6|**Estendere**|Un caso di utilizzo di estensione aggiunge gli obiettivi e passaggi per il caso di utilizzo esteso. Le estensioni possono essere usate solo in determinate condizioni. Il caso di utilizzo esteso viene inserito all'estremità della freccia.<br /><br /> Si noti che il diagramma non mostra le circostanze esatte in cui viene applicata l'estensione. È possibile registrare tali dettagli in un commento o un altro documento.|  
|7|**Ereditarietà**|Mette in correlazione un elemento specializzato e un elemento generalizzato. L'elemento generalizzato viene inserito all'estremità della freccia.<br /><br /> Un caso di utilizzo specializzato eredita gli obiettivi e gli attori della relativa generalizzazione e può aggiungere obiettivi più specifici e i passaggi per raggiungerli.<br /><br /> Un attore specializzato eredita i casi di utilizzo, gli attributi e le associazioni della relativa generalizzazione e può aggiungerne altri.|  
|8|**dipendenza**|Indica che la progettazione dell'origine dipende dalla progettazione della destinazione.|  
|9|**Commentoo**|Usato per aggiungere note generali al diagramma.|  
|10|**Artefatto**|Un elemento fornisce un collegamento a un altro diagramma o documento. È possibile crearlo trascinando un file da Esplora soluzioni. Può essere collegato con una dipendenza a qualsiasi altro elemento del diagramma. Un elemento viene in genere usato per collegare un caso di utilizzo a un diagramma di sequenza, una pagina di OneNote, un documento di Word o una presentazione di PowerPoint che ne descrive i dettagli. Il documento può essere un elemento della soluzione [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] o un documento in una posizione condiviso, ad esempio un sito di SharePoint.<br /><br /> -   **Collegamento ipertestuale**. L'URL o il percorso del file del diagramma o del documento.<br /><br /> Fare doppio clic su un elemento per aprire il file o una pagina Web a cui è collegato.|  
|11 (non mostrato)|**Pacchetti**|I casi di utilizzo, gli attori e i sottosistemi possono essere contenuti all'interno di pacchetti. Forme di pacchetto non vengono visualizzati nel diagramma, ma è possibile impostare il **LinkedPackage** proprietà del diagramma. Elementi creati successivamente nel diagramma vengono posizionati all'interno del pacchetto. Per altre informazioni, vedere [definire pacchetti e spazi dei nomi](../modeling/define-packages-and-namespaces.md).|  
  
## <a name="see-also"></a>Vedere anche  
 [Diagrammi caso di utilizzo UML: linee guida](../modeling/uml-use-case-diagrams-guidelines.md)   
 [Modificare modelli e diagrammi UML](../modeling/edit-uml-models-and-diagrams.md)   
 [Diagrammi di sequenza UML: riferimento](../modeling/uml-sequence-diagrams-reference.md)   
 [Diagrammi classi UML: riferimento](../modeling/uml-class-diagrams-reference.md)   
 [Diagrammi dei componenti UML: riferimento](../modeling/uml-component-diagrams-reference.md)   
 [Diagrammi dei componenti UML: riferimento](../modeling/uml-component-diagrams-reference.md)



