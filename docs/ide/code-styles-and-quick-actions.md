---
title: Preferenze di stile per il codice
ms.date: 03/10/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.CSharp.Code_Style.General
- VS.ToolsOptionsPages.Text_Editor.Basic.Code_Style.General
ms.workload:
- multiple
ms.openlocfilehash: e1875099fa73fc994643b137807d1b0e1ed485c9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53949946"
---
# <a name="code-style-preferences"></a>Preferenze di stile per il codice

Per impostare preferenze di stile per il codice per i progetti C# e Visual Basic, aprire la finestra di dialogo **Opzioni** dal menu **Strumenti**. Nella finestra di dialogo **Opzioni** selezionare **Editor di testo** > [**C#** oppure **Basic**] > **Stile codice** > **Generale**. Le opzioni impostate in questa finestra sono applicabili solo al computer locale.

Quando viene selezionata, ogni voce dell'elenco visualizza un'anteprima della preferenza:

![Opzioni di stile di codice](media/code-style-quick-actions-dialog.png)

> [!NOTE]
> Questo argomento si applica a Visual Studio in Windows. Per Visual Studio per Mac, vedere [Comportamento dell'editor in Visual Studio per Mac](/visualstudio/mac/editor-behavior).

## <a name="preference-and-severity"></a>Preferenza e gravità

Per ogni voce è possibile impostare i valori **Preferenza** e **Gravità** usando i menu a discesa disponibili per ogni riga. La gravità può essere impostata su **Nessuno**, **Suggerimento**, **Avviso** o **Errore**. Se si vogliono abilitare le [Azioni rapide](../ide/quick-actions.md) per uno stile di codice, assicurarsi che l'opzione **Gravità** sia impostata su un valore diverso da **Nessuno**. L'icona a forma di lampadina di **Azioni rapide** ![icona lampadina piccola](media/vs2015_lightbulbsmall.png) viene visualizzata quando si usa uno stile non preferito ed è possibile scegliere un'opzione nell'elenco **Azioni rapide** per riscrivere automaticamente il codice con lo stile preferito.

## <a name="editorconfig-files"></a>File EditorConfig

Per .NET è possibile gestire le impostazioni relative agli stili di codice anche con un file [EditorConfig](../ide/editorconfig-code-style-settings-reference.md). Le impostazioni nel file EditorConfig hanno la precedenza sulle opzioni selezionate nella finestra di dialogo **Opzioni**. È possibile usare un file EditorConfig per applicare e configurare lo stile di scrittura del codice per l'intero repository o per l'intero progetto.

## <a name="format-document-command"></a>Comando Formatta documento

In Visual Studio 2017 versione 15.8 e versioni successive, è possibile configurare il comando **Formatta documento**, in **Modifica** > **Avanzate** > **Formatta documento**, per eseguire la pulizia del codice aggiuntivo in un file, ad esempio per rimuovere e ordinare using o applicare le preferenze di stile del codice. È possibile definire le impostazioni che si desidera applicare con **Formatta documento** nella [pagina delle opzioni Formattazione](reference/options-text-editor-csharp-formatting.md#format-document-settings).

La pulizia del codice rispetta le impostazioni configurate in un file *editorconfig* o in mancanza di tale regola o file, quelle impostate in **Strumenti** > **Opzioni** > **Editor di testo** > **C#** > [**Stile codice** oppure **Formattazione**].

La prima volta che si attiva il comando **Formatta documento** in Visual Studio 2017, una barra informazioni gialla richiede all'utente di configurare le impostazioni di pulizia del codice.

> [!TIP]
> Le regole configurate come **nessuna** in un file con estensione *EDITORCONFIG* non fanno parte della pulizia del codice, ma possono essere applicate singolarmente tramite il menu **Azioni rapide e refactoring**.

## <a name="see-also"></a>Vedere anche

- [Azioni rapide](../ide/quick-actions.md)
- [Impostazioni delle convenzioni per la scrittura del codice .NET per EditorConfig](../ide/editorconfig-code-style-settings-reference.md)
- [Comportamento dell'editor (Visual Studio per Mac)](/visualstudio/mac/editor-behavior)