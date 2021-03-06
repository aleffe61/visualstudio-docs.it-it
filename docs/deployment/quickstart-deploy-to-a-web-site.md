---
title: Eseguire la pubblicazione in un sito Web
ms.date: 06/22/2018
ms.topic: quickstart
helpviewer_keywords:
- deployment, website
ms.assetid: fc82b1f1-d342-4b82-9a44-590479f0a895
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e9744493a8be24ff9ab3e1f8749b02d77d8cc0b4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53937205"
---
# <a name="publish-a-web-app-to-a-web-site-using-visual-studio"></a>Eseguire la pubblicazione un'app Web in un sito Web usando Visual Studio

È possibile usare lo strumento **Pubblica** per la pubblicazione di app ASP.NET, ASP.NET Core, .NET Core e Python in sito Web da Visual Studio. Per Node.js la procedura è supportata, ma l'interfaccia utente è diversa.

[!INCLUDE [quickstart-prereqs](includes/quickstart-prereqs.md)]

## <a name="publish-to-a-web-site"></a>Eseguire la pubblicazione in un sito Web

1. In Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto e scegliere **Pubblica** o usare la voce di menu **Compila** > **Pubblica**.

    ![Il comando Pubblica nel menu di scelta rapida del progetto in Esplora soluzioni](../deployment/media/quickstart-publish.png "scegliere Pubblica")

1. Se sono stati configurati dei profili di pubblicazione, viene visualizzato il riquadro **Pubblica**. Selezionare **Crea nuovo profilo**.

1. Nella finestra di dialogo **Selezionare una destinazione di pubblicazione** scegliere **IIS, FTP e così via**.

    ![Scegliere IIS, FTP e così via](../deployment/media/quickstart-publish-iis-ftp.png "Scegliere IIS, FTP e così via.")

1. Selezionare **Pubblica**. Viene visualizzata la finestra di dialogo delle impostazioni di pubblicazione del profilo.

    ![Scegli cartella](../deployment/media/quickstart-publish-settings-web.png "Scegli cartella")

1. Nel campo **Metodo di pubblicazione** scegliere un metodo, ad esempio **Distribuzione Web** oppure **FTP**. Le impostazioni visualizzate corrispondono al metodo di pubblicazione. La funzionalità Distribuzione Web semplifica la distribuzione di applicazioni Web e siti Web ai server IIS e deve essere installata come applicazione nel server. Usare la [Installazione guidata piattaforma Web](https://www.microsoft.com/web/downloads/platform.aspx) per installarla.

1. Configurare le impostazioni necessarie per il metodo di pubblicazione e selezionare **Convalida connessione**. Se il server o la destinazione è disponibile e le impostazioni sono corrette, un messaggio avvisa che la connessione è stata convalidata e si può pubblicare.

    ![Convalidare la connessione](../deployment/media/quickstart-publish-web-deploy.png "Convalidare la connessione")

1. Selezionare **Impostazioni** per configurare altre impostazioni di distribuzione, ad esempio se distribuire una configurazione di debug o di rilascio e selezionare **Salva**. Per le operazioni di debug eseguite in modalità remota, è necessario distribuire una configurazione di debug.

1. Per pubblicare selezionare **Pubblica**. La finestra Output mostra i risultati e lo stato della distribuzione.

## <a name="next-steps"></a>Passaggi successivi

In questa guida introduttiva è stato descritto come usare Visual Studio per creare un profilo di pubblicazione. È anche possibile configurare un profilo di pubblicazione importando le impostazioni di pubblicazione.

> [!div class="nextstepaction"]
> [Importare impostazioni di pubblicazione e distribuzione in IIS](tutorial-import-publish-settings-iis.md)
