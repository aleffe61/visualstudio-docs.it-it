---
title: Presentazione di Visual Studio per Mac
description: Visual Studio per Mac offre un ambiente di sviluppo integrato per creare applicazioni .NET in macOS, inclusi siti Web ASP.NET Core e progetti Xamarin per iOS, Android, Mac e Xamarin.Forms.
zone_pivot_groups: mac-ide-version
author: conceptdev
ms.author: crdun
ms.date: 11/03/2018
ms.assetid: 7DC64A52-AA41-4F3A-A8A1-8A20BCD81CC7
ms.openlocfilehash: e1787f6d396121263d91633a4ee6d4dd8ed2c35f
ms.sourcegitcommit: ae46be4a2b2b63da7e7049e9ed67cd80897c8102
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2018
ms.locfileid: "52895795"
---
# <a name="visual-studio-for-mac-tour"></a>Presentazione di Visual Studio per Mac

Visual Studio per Mac fa evolvere Xamarin Studio, l'IDE di Xamarin incentrato sui dispositivi mobili, in un ambiente di sviluppo mobile-first, cloud-first per Mac. Questo strumento per sviluppatori permette di sfruttare la potenza di .NET per creare applicazioni per tutte le piattaforme richieste dagli utenti.

L'esperienza utente di Visual Studio per Mac è simile a quella della relativa controparte Windows, ma con un aspetto nativo tipico di macOS. La creazione, l'apertura e lo sviluppo di app saranno operazioni familiari per chi in precedenza ha usato Visual Studio in Windows. Visual Studio per Mac usa inoltre molti degli strumenti avanzati che rendono la controparte Windows un IDE estremamente potente. La piattaforma di compilazione Roslyn viene usata per il refactoring e per IntelliSense. Il sistema del progetto e il motore di compilazione usano MSBuild e l'editor standard supporta i bundle TextMate. Vengono usati gli stessi motori di debugger per le app Xamarin e .NET Core e le stesse finestre di progettazione per Xamarin.iOS e Xamarin.Android.

Questo articolo esamina diverse sezioni di Visual Studio per Mac e presenta alcune delle caratteristiche che lo rendono uno strumento potente per la creazione di applicazioni multipiattaforma.

## <a name="ide-tour"></a>Presentazione dell'IDE

Visual Studio per Mac è organizzato in sezioni diverse per la gestione di impostazioni e file delle applicazioni, la creazione di codice delle applicazioni e il debug.

::: zone pivot="vsmac2019"

## <a name="visual-studio-for-mac-2019-start-window"></a>Finestra iniziale di Visual Studio per Mac 2019

> [!TIP]
> L'anteprima di Visual Studio 2019 per Mac è [disponibile per il download](install-preview.md) e i test.

Quando si avvia l'anteprima di Visual Studio per Mac 2019, verrà visualizzata una finestra per l'accesso. Accedere con l'account Microsoft per attivare una licenza a pagamento (se disponibile) o connettersi alle sottoscrizioni di Azure. È possibile premere **Ignora** ed eseguire l'accesso in un secondo momento tramite la voce di menu **Visual Studio > Accedi**:

![Accedere all'account Microsoft](media/ide-tour-2019-start-signin.png)

Gli utenti che hanno eseguito l'accesso visualizzeranno la nuova _finestra iniziale_, che mostra un elenco dei progetti recenti e i pulsanti per aprire un progetto esistente o crearne uno nuovo:

![Scegliere tra i progetti recenti o crearne uno nuovo](media/ide-tour-2019-start-projects.png)

::: zone-end
::: zone pivot="vsmac2017"

## <a name="welcome-screen-in-visual-studio-for-mac-2017"></a>Schermata iniziale in Visual Studio per Mac 2017

All'avvio, Visual Studio per Mac visualizza una *schermata iniziale*:

![Schermata iniziale](media/ide-tour-image1.png)

La schermata iniziale contiene le sezioni seguenti:

- **Barra degli strumenti** - Consente l'accesso rapido alla barra di ricerca. Quando viene caricata una soluzione, la barra degli strumenti viene usata per definire le configurazioni dell'app, per eseguire il debug e per visualizzare gli errori.
- **Guida introduttiva** - Consente l'accesso rapido ad argomenti utili per gli sviluppatori, per iniziare a usare Visual Studio per Mac.
- **Soluzioni recenti** - Consente l'accesso rapido alle soluzioni aperte di recente, oltre che fornire comodi pulsanti per aprire o creare progetti.
- **Novità per gli sviluppatori** - Newsfeed che offre aggiornamenti sulle ultime novità per gli sviluppatori Microsoft.

::: zone-end

## <a name="solutions-and-projects"></a>Soluzioni e progetti

L'immagine seguente mostra Visual Studio per Mac con un'applicazione caricata:

![Visual Studio per Mac con un'applicazione caricata](media/ide-tour-image17.png)

Le sezioni seguenti forniscono una panoramica delle principali aree di Visual Studio per Mac.

## <a name="solution-pad"></a>Riquadro della soluzione

Il riquadro della soluzione organizza i progetti in una soluzione:

![Progetti organizzati nel riquadro della soluzione](media/ide-tour-image18.png)

In questa posizione i file per il codice sorgente, le risorse, l'interfaccia utente e le dipendenze vengono organizzati in progetti specifici della piattaforma.

Per altre informazioni sull'uso di progetti e soluzioni in Visual Studio per Mac, vedere l'articolo [Progetti e soluzioni](projects-and-solutions.md).

## <a name="assembly-references"></a>Riferimenti dell'assembly

I riferimenti ad assembly per ogni progetto sono disponibili nella cartella Riferimenti:

![Cartella Riferimenti nel riquadro della soluzione](media/ide-tour-image19.png)

È possibile aggiungere altri riferimenti usando la finestra di dialogo **Modifica riferimenti**, visualizzata facendo doppio clic sulla cartella Riferimenti oppure scegliendo **Modifica riferimenti** tra le azioni del menu di scelta rapida:

![Finestra di dialogo Modifica riferimenti](media/ide-tour-image20.png)

Per altre informazioni sull'uso dei riferimenti in Visual Studio per Mac, vedere l'articolo [Gestione dei riferimenti in un progetto](managing-references-in-a-project.md).

## <a name="dependencies--packages"></a>Dipendenze/pacchetti

Tutte le dipendenze esterne usate nell'app vengono archiviate nella cartella Dipendenze o Pacchetti, a seconda che si stia lavorando a un progetto .NET Core o Xamarin.iOS/Xamarin.Android. In genere vengono fornite sotto forma di pacchetto NuGet.

NuGet è il più diffuso strumento di gestione pacchetti per lo sviluppo .NET. Con il supporto di NuGet di Visual Studio è possibile cercare e aggiungere facilmente pacchetti al progetto dell'applicazione.

Per aggiungere una dipendenza all'applicazione, fare clic con il pulsante destro del mouse sulla cartella Dipendenze/Pacchetti e scegliere **Aggiungi pacchetti**:

![Aggiungere un pacchetto NuGet](media/ide-tour-image21.png)

Le informazioni sull'uso di un pacchetto NuGet in un'applicazione sono disponibili nell'articolo [Inserimento di un pacchetto NuGet nel progetto](nuget-walkthrough.md).

## <a name="refactoring"></a>Refactoring

Visual Studio per Mac fornisce due metodi utili per il refactoring del codice: azioni di contesto e analisi dell'origine. Per altre informazioni, vedere l'articolo [Refactoring](refactoring.md).

## <a name="debugging"></a>Debug

Visual Studio per Mac ha un debugger nativo che offre supporto per il debug per applicazioni Xamarin.iOS, Xamarin.Mac e Xamarin.Android. Visual Studio per Mac usa Mono Soft Debugger, un debugger implementato nel runtime di Mono, per consentire all'IDE di eseguire il debug di codice gestito in tutte le piattaforme. Per altre informazioni sul debug, vedere l'articolo [Debug](debugging.md).

Il debugger contiene visualizzatori avanzati per tipi speciali come stringhe, colori, URL, oltre che dimensioni, coordinate e curve di Bézier.

Per altre informazioni sulle visualizzazioni dei dati del debugger, vedere l'articolo [Visualizzazioni dei dati](data-visualizations.md).

## <a name="version-control"></a>Controllo della versione

Visual Studio per Mac si integra con sistemi di controllo del codice sorgente Subversion e Git. I progetti sottoposti a controllo del codice sorgente sono contrassegnati con un ramo accanto al nome della soluzione:

![Nome del ramo per indicare un progetto sottoposto a controllo del codice sorgente](media/ide-tour-image22.png)

I file con modifiche non sottoposte a commit presentano un'annotazione nelle relative icone nel riquadro della soluzione, come illustrato nell'immagine seguente:

![File con modifiche non sottoposte a commit nel riquadro della soluzione](media/ide-tour-image23.png)

Per altre informazioni sul controllo della versione in Visual Studio, vedere l'articolo [Controllo della versione](version-control.md).

## <a name="see-also"></a>Vedere anche

- [IDE di Visual Studio (in Windows)](/visualstudio/ide/visual-studio-ide)