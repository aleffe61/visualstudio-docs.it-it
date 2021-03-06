---
title: Creare modelli di progetto
ms.date: 01/02/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- VS.ExportTemplateWizard
helpviewer_keywords:
- project templates [Visual Studio], creating
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: d0d15d4f3836ca1ccfdc800ad4805ed7691e4454
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53990227"
---
# <a name="how-to-create-project-templates"></a>Procedura: Creare modelli di progetto

Questo argomento spiega come creare un modello usando l'**Esportazione guidata modelli**, che consente di creare un pacchetto del modello in un file con estensione *zip*.

## <a name="to-create-a-user-project-template-by-using-the-export-template-wizard"></a>Per creare un modello di progetto utente usando l'Esportazione guidata modelli

1. Creare un progetto.

    > [!NOTE]
    > Quando si assegna il nome a un progetto che fungerà da origine per un modello, usare solo caratteri di identificatore validi. In caso contrario, possono verificarsi errori di compilazione nei progetti creati dal modello. Per altre informazioni sui caratteri di identificatore valido, vedere [Nomi di elementi dichiarati (Visual Basic)](/dotnet/visual-basic/programming-guide/language-features/declared-elements/declared-element-names) o [Identificatori (C++)](/cpp/cpp/identifiers-cpp). In alternativa, è possibile usare [parametri di modello](../ide/template-parameters.md) per specificare nomi "sicuri" per le classi e gli spazi dei nomi.

2. Modificare il progetto finché non è pronto per l'esportazione come modello. Ad esempio, può essere necessario modificare i file del codice per indicare dove deve essere applicata la sostituzione dei parametri. Vedere [Procedura: Sostituire i parametri di un modello](../ide/how-to-substitute-parameters-in-a-template.md).

3. Nel menu **Progetto** scegliere**Esporta modello**.

   Viene aperta l'**Esportazione guidata modelli**.

4. Nella pagina **Scegliere il tipo di modello** selezionare **Modello di progetto**. Selezionare il progetto che si vuole esportare in un modello e quindi scegliere **Avanti**.

5. Nella pagina **Selezionare le opzioni del modello** immettere il nome e una descrizione, un'icona e un'immagine di anteprima facoltative per il modello. Questi elementi verranno visualizzati nella finestra di dialogo **Nuovo progetto**. Scegliere **Fine**.

   Il progetto viene esportato in un file con estensione *zip*, inserito nel percorso di output specificato e, se questa azione è stata selezionata, importato in Visual Studio.

>[!NOTE]
> Per trovare il modello nella finestra di dialogo **Nuovo progetto**, espandere **Installato** e quindi espandere la categoria che corrisponde all'elemento `ProjectType` nel file con estensione *vstemplate*. Ad esempio, un file con estensione *vstemplate* che contiene `<ProjectType>CSharp</ProjectType>` appare in **Installato** > **Visual C#** per impostazione predefinita. È possibile organizzare il modello in una sottodirectory del tipo di progetto semplicemente creando una cartella in quella directory e inserendo il file con estensione *zip* del modello nella cartella. Per altre informazioni, vedere [Procedura: Individuare e organizzare modelli](../ide/how-to-locate-and-organize-project-and-item-templates.md).

## <a name="other-ways-to-create-project-templates"></a>Altri modi per creare modelli di progetti

È possibile creare manualmente modelli di progetti raccogliendo i file che costituiscono il progetto in una cartella e quindi creando un file XML con estensione *vstemplate* con i metadati appropriati. Per altre informazioni, vedere [Procedura: Creare manualmente modelli Web](../ide/how-to-manually-create-web-templates.md).

Se Visual Studio SDK è installato, è possibile eseguire il wrapping del modello finito in un file VSIX per la distribuzione con il modello **Progetto VSIX**. Per altre informazioni, vedere [Introduzione al modello di progetto VSIX](../extensibility/getting-started-with-the-vsix-project-template.md).

## <a name="see-also"></a>Vedere anche

- [Creare modelli di progetto e di elementi](../ide/creating-project-and-item-templates.md)
- [Procedura: Creare modelli di elementi](../ide/how-to-create-item-templates.md)
- [Introduzione al modello di progetto VSIX](../extensibility/getting-started-with-the-vsix-project-template.md)