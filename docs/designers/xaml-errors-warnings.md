---
title: Errori e avvisi XAML
ms.date: 03/06/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 34eac8a0-7ec5-4c40-b97a-0126ed367931
author: karann-msft
ms.author: karann
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a7e0a5b4bde839e90bcf852273fa0872b1a5c76f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53922612"
---
# <a name="xaml-errors-and-warnings"></a>Errori e avvisi XAML

Durante la creazione di codice XAML, Visual Studio analizza il codice mentre lo si digita. Quando viene rilevato un errore in una riga di codice, viene visualizzata una sottolineatura ondulata. Se si porta il cursore del mouse sulla sottolineatura, vengono visualizzate informazioni sull'errore o sull'avviso. Per alcuni errori e avvisi viene visualizzata una lampadina di azione e la combinazione di tasti **CTRL**+**.** consente di visualizzare le opzioni per la risoluzione del problema.

## <a name="error-types"></a>Tipi di errore

Vari strumenti analizzano il codice XAML in background. Gli errori XAML sono suddivisi nei tre tipi seguenti, a seconda dello strumento che ha rilevato l'errore:

|**Errore rilevato da**|**Formato codice di errore**|
| - |-----------------|
|Servizio di linguaggio XAML (Editor XAML)|XLSxxxx|
|Finestra di progettazione XAML|XDGxxxx|
|Modifica e continuazione XAML|XECxxxx|

> [!Note]
> Non tutti gli errori o avvisi hanno un codice corrispondente. Gli errori senza codice sono in genere errori della finestra di progettazione XAML.


## <a name="suppress-xaml-designer-errors"></a>Eliminare gli errori della finestra di progettazione XAML

Aprire la finestra di dialogo **Opzioni** selezionando **Strumenti > Opzioni** e selezionare **Editor di testo > XAML > Varie**.

Deselezionare la casella di controllo **Show errors detected by the XAML designer** (Visualizza errori rilevati dalla finestra di progettazione XAML).

![Eliminare gli errori della finestra di progettazione XAML](../designers/media/suppress_xaml_designer_errors.png)
