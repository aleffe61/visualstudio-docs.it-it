---
title: "Procedura: Spostarsi tra le visualizzazioni e l'editor XML"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: cb69fbbd-d99c-439e-9498-5df9050f8df0
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 09ad752dc87ea322396d6e6513593d71a7554b98
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53936243"
---
# <a name="how-to-switch-between-views-and-the-xml-editor"></a>Procedura: Passare dalle visualizzazioni all'Editor XML

In questo argomento viene illustrato come passare dalle visualizzazioni di Progettazione XML Schema (Progettazione XSD) all'editor XML. Questo esempio Usa la [schema di ordine di acquisto](../xml-tools/sample-xsd-file-simple-schema.md).

## <a name="to-switch-between-the-views-and-the-xml-editor"></a>Per passare dalle visualizzazioni all'editor XML

1.  Per creare e modificare un nuovo file di schema XML, seguire i passaggi in [come: Creare e modificare un file di schema XSD](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).

2.  Per passare a Progettazione XML Schema dall'Editor XML, fare doppio clic su un punto qualsiasi dell'Editor XML e selezionare **Progettazione viste**.

3.  Per passare alla visualizzazione grafico tramite la filigrana, scegliere il **usare la visualizzazione grafico per visualizzare la relazione tra i nodi** collegamento nella visualizzazione iniziale.

4.  Trascinare il `USAddress` nodo il **XML Schema Explorer** alla visualizzazione grafico. Fare doppio clic il `USAddress` nodo nella visualizzazione grafico e selezionare **Mostra nella visualizzazione modello di contenuto** nel menu di scelta rapida.

     Viene aperta la visualizzazione modello di contenuto con i dettagli del nodo `USAddress`.

5.  Per passare alla visualizzazione iniziale dalla visualizzazione modello di contenuto usando la barra degli strumenti, scegliere il **visualizzazione iniziale** pulsante sulla barra degli strumenti XSD.

6.  Per spostarsi tra le visualizzazioni usando i tasti di scelta, premere **Ctrl**+**1** per la visualizzazione iniziale, **Ctrl**+**2** per la visualizzazione grafico e **Ctrl**+**3** per la visualizzazione modello di contenuto.

7.  Per passare all'Editor XML dalla visualizzazione modello di contenuto, il pulsante destro del nodo e selezionare **Visualizza codice** nel menu di scelta rapida.