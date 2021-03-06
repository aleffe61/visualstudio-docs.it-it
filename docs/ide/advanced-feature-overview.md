---
title: Funzionalità avanzate di Visual Studio 2017
titleSuffix: ''
ms.date: 06/01/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 739426d5d93628c90638fef32526484f27eef3e8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53828498"
---
# <a name="features-of-visual-studio-2017"></a>Funzionalità di Visual Studio 2017

L'articolo [Panoramica dell'IDE di Visual Studio](../get-started/visual-studio-ide.md) offre un'introduzione a Visual Studio. Questo articolo descrive funzionalità che potrebbero essere più appropriate per gli sviluppatori esperti o per chi ha già familiarità con Visual Studio.

## <a name="modular-installation"></a>Installazione modulare

Il programma di installazione modulare di Visual Studio consente di scegliere e installare *carichi di lavoro* specifici, ovvero gruppi di funzionalità necessarie per il linguaggio di programmazione o la piattaforma preferiti. Questa strategia riduce il footprint dell'installazione di Visual Studio e questo significa anche una maggiore velocità di installazione e aggiornamento.

Se Visual Studio 2017 non è ancora installato, accedere alla pagina [Download di Visual Studio](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) per installarlo gratuitamente.

Per altre informazioni sull'installazione di Visual Studio nel sistema, vedere [Installare Visual Studio 2017](../install/install-visual-studio.md).

## <a name="create-cloud-enabled-apps-for-azure"></a>Creare app abilitate per il cloud per Azure

Visual Studio offre un gruppo di strumenti che consentono di creare facilmente applicazioni abilitate per il cloud con tecnologia Microsoft Azure. È possibile gestire la configurazione, la compilazione, il debug, l'inserimento in pacchetti e la distribuzione di applicazioni e servizi in Microsoft Azure direttamente dall'IDE. Per ottenere gli strumenti e i modelli di progetto di Azure, selezionare il carico di lavoro **Sviluppo di Azure** quando si installa Visual Studio.

![Carico di lavoro Sviluppo di Azure](../data-tools/media/azure-development-workload.png)

Dopo aver installato il carico di lavoro **Sviluppo di Azure**, vengono resi disponibili i modelli **Cloud** seguenti per C# nella finestra di dialogo **Nuovo progetto**:

![Modelli progetto cloud per Visual Studio](media/cloud-project-templates.png)

[Cloud Explorer](/azure/vs-azure-tools-resources-managing-with-cloud-explorer) di Visual Studio consente di visualizzare e gestire le risorse cloud basate su Azure in Visual Studio. Queste risorse possono includere macchine virtuali, tabelle, database SQL e altro ancora. **Cloud Explorer** rende disponibili le risorse di Azure in tutti gli account gestiti con la sottoscrizione di Azure a cui si è connessi. E se una particolare operazione richiede il portale di Azure, **Cloud Explorer** specifica i collegamenti che consentono di accedere al punto del portale di Azure in cui si vuole arrivare.

![Cloud Explorer in Visual Studio](media/cloud-explorer.png)

È possibile sfruttare i servizi di Azure per le app usando **Servizi connessi**, ad esempio:

- [Servizio connesso di Active Directory](/azure/active-directory/develop/vs-active-directory-add-connected-service) in modo che gli utenti possano usare i propri account [Azure Active Directory](/azure/active-directory/active-directory-whatis) per connettersi alle app Web
- [Servizio connesso Archiviazione di Azure](/azure/vs-azure-tools-connected-services-storage) per archiviazione BLOB, code e tabelle
- [Servizio connesso Key Vault](/azure/key-vault/vs-key-vault-add-connected-service) per gestire i segreti per le app web

I **servizi connessi** disponibili dipendono dal tipo di progetto. Aggiungere un servizio facendo clic con il pulsante destro del mouse sul progetto in **Esplora soluzioni** e scegliendo **Aggiungi** > **Servizio connesso**.

![Servizi connessi di Visual Studio](media/connected-services.png)

Per altre informazioni, vedere [Passare al cloud con Visual Studio e Azure](https://visualstudio.microsoft.com/vs/azure-tools/).

## <a name="create-apps-for-the-web"></a>Creare app per il Web

Il mondo moderno è dominato dal Web e Visual Studio può essere utile per scrivere app per questa piattaforma. È possibile creare app Web con ASP.NET, Node.js, Python, JavaScript e TypeScript. Visual Studio riconosce framework Web quali Angular, jQuery, Express e altri. ASP.NET Core e .NET Core supportano i sistemi operativi Windows, Mac e Linux. [ASP.NET Core](http://www.asp.net/core/overview) è un aggiornamento principale per MVC, WebAPI e SignalR e viene eseguito in Windows, Mac e Linux.  ASP.NET Core è stato completamente riprogettato per fornire uno stack .NET pulito e componibile per la compilazione di moderni servizi e app Web basati sul cloud.

Per altre informazioni, vedere [Strumenti Web moderni](https://visualstudio.microsoft.com/vs/modern-web-tooling/).

## <a name="build-cross-platform-apps-and-games"></a>Creare app e giochi multipiattaforma

È possibile usare Visual Studio per compilare app e giochi per macOS, Linux e Windows, nonché per Android, iOS e altri [dispositivi mobili](https://visualstudio.microsoft.com/vs/mobile-app-development/).

- Compilare app [.NET Core](/dotnet/core/) da eseguire in Windows, macOS e Linux.

- Compilare app per dispositivi mobili per iOS, Android e Windows in C# e F# usando [Xamarin](https://developer.xamarin.com/guides/cross-platform/windows/visual-studio/).

- Usare le tecnologie Web standard&mdash;HTML, CSS e JavaScript&mdash; per compilare app per dispositivi mobili per iOS, Android e Windows usando [Apache Cordova](/visualstudio/cross-platform/tools-for-cordova/).

- Compilare giochi 2D e 3D in C# tramite [Visual Studio Tools per Unity](../cross-platform/visual-studio-tools-for-unity.md).

- Compilare app C++ native per dispositivi iOS, Android e Windows e condividere il codice comune nelle librerie create per iOS, Android e Windows usando [C++ per lo sviluppo multipiattaforma](../cross-platform/visual-cpp-for-cross-platform-mobile-development.md).

- Distribuire, testare ed eseguire il debug di app Android con l'[emulatore Android](../cross-platform/visual-studio-emulator-for-android.md).

## <a name="connect-to-databases"></a>Connettersi ai database

**Esplora server** consente di esplorare e gestire le istanze e le risorse di SQL Server in locale, in remoto e in Azure, Salesforce.com, Office 365 e in siti Web. Per aprire **Esplora server**, scegliere **Visualizza** > **Esplora server** dal menu principale. Per altre informazioni su Esplora server, vedere [Add new connections](../data-tools/add-new-connections.md) (Aggiungere nuove connessioni).

[SQL Server Data Tools (SSDT)](/sql/ssdt/download-sql-server-data-tools-ssdt) è un ambiente di sviluppo avanzato per SQL Server, database SQL di Azure e Azure SQL Data Warehouse. Consente di creare, eseguire il debug, gestire ed effettuare il refactoring di database. È possibile usare un progetto di database o direttamente un'istanza del database connesso locale o remota.

**Esplora oggetti di SQL Server** in Visual Studio offre una visualizzazione degli oggetti di database simile a quella di SQL Server Management Studio. Esplora oggetti di SQL Server consente di eseguire operazioni semplici di progettazione e amministrazione dei database, tra cui la modifica dei dati di tabelle, il confronto di schemi, l'esecuzione di query usando i menu di scelta rapida direttamente da Esplora oggetti di SQL Server e altro ancora.

![Esplora oggetti di SQL Server](../ide/media/vs2015_sqlobjectexplorer.png)

## <a name="debug-test-and-improve-your-code"></a>Eseguire il debug del codice, testarlo e migliorarlo

Durante la scrittura del codice è necessario eseguirlo e testarlo per individuare eventuali bug e controllarne le prestazioni. Il sistema di debug all'avanguardia di Visual Studio consente di eseguire il debug del codice in esecuzione nel progetto locale, in un dispositivo remoto o in un [emulatore di dispositivo](../cross-platform/visual-studio-emulator-for-android.md). È possibile esaminare il codice un'istruzione alla volta e controllare le variabili man mano. È possibile impostare punti di interruzione che vengono raggiunti solo quando viene soddisfatta una condizione specificata. Tutte queste funzionalità possono essere gestite nell'editor del codice stesso, senza uscire dal codice. Per altri dettagli sul debug in Visual Studio, vedere [Tour delle funzionalità del debugger](../debugger/debugger-feature-tour.md).

Per altre informazioni su come migliorare le prestazioni delle app, vedere la funzionalità di [profilatura](../profiling/profiling-feature-tour.md) di Visual Studio.

Per le operazioni di [test](../test/improve-code-quality.md), Visual Studio supporta il testing unità, Live Unit Testing, IntelliTest, test di carico e delle prestazioni e altro ancora. Visual Studio include anche funzionalità avanzate di [analisi del codice](../code-quality/code-analysis-for-managed-code-overview.md) per individuare difetti di progettazione, sicurezza e di altro tipo.

## <a name="deploy-your-finished-application"></a>Distribuire l'applicazione completata

Quando l'applicazione è pronta per la distribuzione a utenti o clienti, Visual Studio offre gli strumenti appropriati, a seconda che si tratti di una distribuzione in Microsoft Store, in un sito di SharePoint o tramite le tecnologie InstallShield o Windows Installer. Tutti gli strumenti sono accessibili dall'IDE. Per altre informazioni, vedere [Distribuzione di applicazioni, servizi e componenti](../deployment/deploying-applications-services-and-components.md).

## <a name="manage-your-source-code-and-collaborate-with-others"></a>Gestire il codice sorgente e collaborare con altri utenti

È possibile gestire il codice sorgente in repository GIT ospitati da qualsiasi provider, incluso GitHub. In alternativa, usare [Azure DevOps Services](/azure/devops/index) per gestire il codice insieme ai bug e agli elementi di lavoro per l'intero progetto. Per altre informazioni sulla gestione dei repository GIT in Visual Studio con Team Explorer, vedere [Get Started with Git and Azure Repos](/azure/devops/repos/git/gitquickstart?tabs=visual-studio) (Introduzione a GIT e Azure Repos). Visual Studio include anche altre funzionalità predefinite di controllo del codice sorgente. Per altre informazioni su tali funzionalità, vedere il post del blog [New Git Features in Visual Studio 2017](https://blogs.msdn.microsoft.com/devops/2017/03/06/new-git-features-in-visual-studio-2017/) (Nuove funzionalità GIT in Visual Studio 2017).

Azure DevOps Services è un insieme di servizi basati sul cloud per la pianificazione, l'hosting, l'automazione e la distribuzione del software nonché la collaborazione nei team. Azure DevOps Services supporta sia i repository GIT (controllo della versione distribuito), sia il controllo della versione di Team Foundation (controllo della versione centralizzato), nonché le pipeline di compilazione e rilascio continui (CI/CD) del codice archiviato nei sistemi di controllo delle versioni. Azure DevOps Services supporta anche le metodologie di sviluppo Scrum, CMMI e Agile.

Team Foundation Server (TFS) è l'hub di gestione del ciclo di vita delle applicazioni per Visual Studio. Consente a tutte le parti interessate di partecipare al processo di sviluppo usando un'unica soluzione. TFS è utile anche per la gestione di team e progetti eterogenei.

Se in rete è presente un'organizzazione di Azure DevOps o Team Foundation Server, è possibile connettersi usando la finestra **Team Explorer** in Visual Studio. Da questa finestra è possibile archiviare o estrarre il codice dal controllo del codice sorgente, gestire gli elementi di lavoro, avviare le compilazioni e accedere alle chat team e alle aree di lavoro. È possibile aprire **Team Explorer** dalla casella **Avvio veloce** o dal menu principale tramite **Visualizza** > **Team Explorer** o **Team** > **Gestisci connessioni**.

L'immagine seguente illustra la finestra **Team Explorer** per una soluzione ospitata in Azure DevOps Services.

![Visual Studio Team Explorer](../ide/media/vs2017_teamexplorer.png)

È anche possibile automatizzare il processo di compilazione per compilare il codice che gli sviluppatori del team hanno archiviato nel controllo della versione. È possibile ad esempio compilare uno o più progetti di notte o ogni volta che il codice viene controllato. Per altre informazioni, vedere [Azure Pipelines](/azure/devops/pipelines/index?view=vsts).

## <a name="extend-visual-studio"></a>Estendere Visual Studio

Se Visual Studio non include la funzionalità esatta di cui si ha bisogno, è possibile aggiungerla. È possibile personalizzare l'IDE in base al flusso e allo stile di lavoro personali, aggiungere il supporto per strumenti esterni non ancora integrati in Visual Studio e modificare le funzionalità esistenti per aumentare la produttività. Per trovare la versione più recente degli strumenti di estendibilità di Visual Studio (VS SDK), vedere [Visual Studio SDK](../extensibility/visual-studio-sdk.md).

È possibile usare .NET Compiler Platform ("Roslyn") per scrivere analizzatori di codice e generatori di codice personalizzati. Tutto ciò che serve è disponibile nella pagina di [Roslyn](https://github.com/dotnet/Roslyn).

Cercare le [estensioni esistenti](https://marketplace.visualstudio.com/vs) per Visual Studio create dagli sviluppatori Microsoft, nonché dalla community di sviluppo.

Per altre informazioni sull'estensione di Visual Studio, vedere [Estendi Visual Studio IDE](https://visualstudio.microsoft.com/vs/extend/).

## <a name="see-also"></a>Vedere anche

- [Panoramica dell'IDE di Visual Studio](../get-started/visual-studio-ide.md)
- [Novità di Visual Studio 2017](../ide/whats-new-in-visual-studio.md)