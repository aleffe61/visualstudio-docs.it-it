---
title: La cartella di lavoro utilizzata per creare il progetto contiene controlli ActiveX non caricabili nella finestra di progettazione
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.SelectDocWizard.ContainsActiveXControls
dev_langs:
- VB
- CSharp
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 6a48cff6b3d2e2b4a090ee5ec5cd879b272593cd
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53876432"
---
# <a name="the-workbook-used-to-create-this-project-contains-activex-controls-that-the-designer-cannot-load"></a>La cartella di lavoro utilizzata per creare il progetto contiene controlli ActiveX non caricabili nella finestra di progettazione
  Questo errore viene visualizzato quando si aggiunge a livello di codice un controllo a un documento di Word o a un foglio di lavoro di Excel, si salva il documento o la cartella di lavoro e si crea quindi una nuova soluzione a livello di documento basata sul documento o sulla cartella di lavoro.  
  
 Le informazioni relative alla descrizione del tipo gestito del controllo non vengono salvate insieme al documento o alla cartella di lavoro. Quando si crea una nuova soluzione basata su tale documento o cartella di lavoro, in Visual Studio non sono disponibili informazioni sufficienti per caricare il controllo nella finestra di progettazione dell'elemento host.  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Aprire il documento o la cartella di lavoro.  
  
2.  Rimuovere i controlli che sono stati aggiunti in fase di esecuzione. Tale scopo, è possibile selezionarli nel documento o cartella di lavoro e premere il **eliminare** chiave.  
  
3.  Creare una soluzione a livello di documento basata sul documento o sulla cartella di lavoro.  
  
## <a name="see-also"></a>Vedere anche  
 [Procedura: Creare progetti di Office in Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [Aggiungere controlli ai documenti di Office in fase di esecuzione](../vsto/adding-controls-to-office-documents-at-run-time.md)  
