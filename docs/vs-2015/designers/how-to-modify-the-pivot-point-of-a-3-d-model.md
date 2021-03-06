---
title: 'Procedura: Modificare il punto di perno di un modello 3D | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c20b4ec8-29f5-4ca5-bc39-d4548ca6f573
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: beba04bab85b3fd09aafb195039ad6e34106e293
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49850529"
---
# <a name="how-to-modify-the-pivot-point-of-a-3-d-model"></a>Procedura: Modificare il punto pivot di un modello tridimensionale
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Questo documento illustra come usare l'editor dei modelli per modificare il *punto di perno* di un modello 3D. Il punto di perno è il punto nello spazio che definisce il centro matematico dell'oggetto per la rotazione e il ridimensionamento.  
  
 Questo documento illustra questa attività:  
  
-   Modifica del punto di perno di un oggetto  
  
## <a name="modifying-the-pivot-point-of-a-3-d-model"></a>Modifica del punto di perno di un modello 3D  
 È possibile ridefinire l'origine di un modello 3D modificandone il punto di perno.  
  
 Assicurarsi che siano visualizzate la finestra **Proprietà** e la **casella degli strumenti**.  
  
#### <a name="to-modify-the-pivot-point-of-a-3-d-model"></a>Per modificare il punto perno di un modello 3D  
  
1. Iniziare con un modello 3D esistente, come quello descritto in [Procedura: Creare un modello 3D di base](../designers/how-to-create-a-basic-3-d-model.md).  
  
2. Passare alla modalità perno. Nella barra degli strumenti disponibile in modalità **Editor dei modelli** scegliere il pulsante **Modalità perno** per attivare la modalità perno. Viene visualizzata una casella intorno al pulsante **Modalità perno** per indicare che l'editor dei modelli è ora in modalità perno. In modalità perno, operazioni come la traslazione agiscono sul punto di perno dell'oggetto anziché sulla struttura dell'oggetto nello spazio globale.  
  
3. Modificare il punto di perno dell'oggetto. In modalità **Seleziona** selezionare l'oggetto e nella barra degli strumenti del **visualizzatore modelli** scegliere lo strumento **Trasla**. Nell'area di progettazione viene visualizzata una casella che rappresenta il punto di perno. Spostare la casella per modificare il punto di perno dell'oggetto.  
  
    Spostando la casella è possibile spostare il punto di perno in tutte le tre dimensioni. Per traslare il punto di perno lungo un asse, spostare la freccia corrispondente all'asse. La casella e le frecce vengono visualizzate in giallo per indicare l'asse interessata dalla traslazione.  
  
    È possibile specificare il punto di perno anche tramite la proprietà **Traslazione perno** della finestra **Proprietà**.  
  
   > [!TIP]
   >  È possibile visualizzare l'effetto del nuovo punto di perno ruotando l'oggetto. Per ruotarlo, usare lo strumento **Ruota** o modificare la proprietà **Rotazione**.  
  
   Di seguito è riportato un modello con un punto di perno modificato:  
  
   ![Modello di casa con punto di perno modificato](../designers/media/digit-modified-model.png "Digit-Modified-Model")  
  
## <a name="see-also"></a>Vedere anche  
 [Procedura: Creare un modello 3D di base](../designers/how-to-create-a-basic-3-d-model.md)   
 [Editor dei modelli](../designers/model-editor.md)



