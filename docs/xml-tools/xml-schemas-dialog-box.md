---
title: Finestra di dialogo Schemi XML
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
ms.assetid: 0271fa26-2205-49bd-96e0-ae1441571808
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b1f8f4824d18618b40ad4073dc6be0c81d9aba37
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53835208"
---
# <a name="xml-schemas-dialog-box"></a>Finestra di dialogo schemi XML

Il **schemi XML** nella finestra di dialogo è possibile selezionare quali schemi XML schema definition language (XSD) da associare a un documento XML. È possibile selezionare uno schema dalla cache degli schemi oppure specificare uno schema che non si trova nella cache. Gli schemi selezionati vengono considerati parte di un set di schemi, che viene usato per IntelliSense e per la convalida dei documenti XML.

È possibile accedere la **schemi XML** finestra di dialogo facendo la **schemi** pulsante nella finestra delle proprietà del documento o selezionando **schemi** dal **XML** menu.

## <a name="uielement-list"></a>Elenco UIElement
 **Usare**

 Consente di selezionare la modalità di utilizzo di XML Schema.

-   **Automatica**. Questo schema non è usato dal documento corrente ma è disponibile per l'associazione automatica. Se il documento XML dichiara uno spazio di nomi che corrisponde al `targetNamespace` di questo schema, lo schema viene automaticamente associato e incluso nel set di schemi.

-   **Usare questo schema**. Questo schema è usato dal documento corrente. L'utilizzo di questo schema è stato richiesto in modo esplicito selezionando questa colonna oppure lo schema è stato associato automaticamente in base a un `targetNamespace` corrispondente.

-   **Non usare gli schemi selezionati**. Questo schema non è usato dal documento corrente anche se dispone di un `targetNamespace` corrispondente. Questa impostazione può essere utile per la risoluzione di conflitti nel caso in cui la cache dello schema o la soluzione contengano più versioni dello stesso schema.

**Target Namespace**

Consente di visualizzare lo spazio dei nomi di destinazione associato allo schema XML.

**Nome del file**

Consente di visualizzare il nome del file di XML Schema.

**Aggiungi**

Apre la **Apri Schema XSD** finestra di dialogo che consente di selezionare altri schemi da aggiungere al set di schemi. Quando si aggiunge uno schema allo schema impostato, il **utilizzo** il valore di colonna è impostato su **utilizzano questo schema**.

**Rimuovi**

Consente di rimuovere lo schema attualmente selezionato dal set di schemi. L'operazione rimuove lo schema dalla cache degli schemi in memoria, ma non dal file system.

## <a name="see-also"></a>Vedere anche

- [Componenti dell'Editor XML](../xml-tools/xml-editor-components.md)
- [Procedura: Selezionare gli schemi XML da usare](../xml-tools/how-to-select-the-xml-schemas-to-use.md)
- [Cache degli schemi](../xml-tools/schema-cache.md)