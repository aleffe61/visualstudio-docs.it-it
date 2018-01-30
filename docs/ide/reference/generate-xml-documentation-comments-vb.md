---
title: Generare commenti in formato documentazione XML per Visual Basic | Microsoft Docs
ms.custom: 
ms.date: 11/17/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 2f421553657dfafb265140e44e38a2c7722a7303
ms.sourcegitcommit: f89ed5fc2e5078213e30a6ade4604e34df48181f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/13/2018
---
# <a name="generate-xml-documentation-comments-in-visual-basic"></a>Generare commenti in formato documentazione XML in Visual Basic

**Cosa:** consente di generare immediatamente il codice XML di base richiesto per documentare l'elemento selezionato. 

**Quando:** si vogliono creare commenti in formato documentazione XML per l'elaborazione successiva con uno strumento di documentazione come Sandcastle.

**Perché:** è possibile creare manualmente l'intero blocco di commento, tuttavia questa funzionalità consentirà di risparmiare tempo e ottenere una maggiore accuratezza generando il modello di base e altri elementi. 

**Come:**

1. Posizionare il cursore del testo sopra l'elemento da documentare, ad esempio, un metodo.

   ![Metodo da documentare](media/doc-highlight-vb.png)

1. Digitare quindi **'''** (3 virgolette singole). Verranno creati automaticamente il modello di base e gli eventuali elementi aggiuntivi necessari.  Ad esempio, quando si aggiungono commenti per un metodo, verranno generati i tag **\<summary\>**, oltre a un tag **\<param\>** per ogni parametro passato al metodo e a un tag **\<returns\>** per documentare i valori restituiti dal metodo.

   ![Modello](media/doc-preview-vb.png)

1. Completare i commenti e aggiungere eventuali informazioni aggiuntive che si ritiene necessarie.

   ![Commento completato](media/doc-result-vb.png)

## <a name="see-also"></a>Vedere anche

[Documentazione del codice tramite XML (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/documenting-your-code-with-xml)  
[Generazione codice](../code-generation-in-visual-studio.md)