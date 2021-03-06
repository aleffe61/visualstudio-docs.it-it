---
title: Distribuire in una cartella locale
ms.date: 06/22/2018
ms.topic: quickstart
helpviewer_keywords:
- deployment, local folder
ms.assetid: adb461c4-812a-4b8c-b2ab-96002379f6a9
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b4dff7adb3942fce20b7b6cb5b09c29965320399
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53854035"
---
# <a name="deploy-an-app-to-a-local-folder-using-visual-studio"></a>Distribuire un'app in una cartella locale usando Visual Studio

È possibile usare lo strumento **Pubblica** per la pubblicazione di app ASP.NET, ASP.NET Core, .NET Core e Python in una cartella locale da Visual Studio. Per Node.js la procedura è supportata, ma l'interfaccia utente è diversa.

[!INCLUDE [quickstart-prereqs](includes/quickstart-prereqs.md)]

## <a name="deploy-to-a-local-folder"></a>Distribuire in una cartella locale

1. In Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto e scegliere **Pubblica** o usare la voce di menu **Compila** > **Pubblica**.

    ![Il comando Pubblica nel menu di scelta rapida del progetto in Esplora soluzioni](../deployment/media/quickstart-publish.png "scegliere Pubblica")

1. Se sono stati configurati dei profili di pubblicazione, viene visualizzato il riquadro **Pubblica**. Selezionare **Crea nuovo profilo**.

1. Nella finestra di dialogo **Selezionare una destinazione di pubblicazione** scegliere **Cartella**.

    ![Scegliere la cartella locale come una destinazione per la pubblicazione](../deployment/media/quickstart-publish-folder.png "Scegli cartella")

1. Immettere un percorso o selezionare **Esplora** per specificare una cartella locale.

1. Selezionare **Pubblica**. Visual Studio compila il progetto e lo pubblica nella cartella specificata. Viene visualizzato il riquadro **Pubblica** delle proprietà del progetto con un riepilogo del profilo.

    ![Riquadro Pubblica delle proprietà con il riepilogo di un profilo](../deployment/media/quickstart-publish-folder-summary.png)

1. Per configurare le impostazioni di distribuzione, selezionare **Configura** nel riepilogo del profilo e selezionare la scheda **Impostazioni**.

    ![Impostazioni del profilo](../deployment/media/quickstart-profile-settings.png "Impostazioni del profilo")

1. Configurare le opzioni, ad esempio se distribuire una configurazione di debug o di rilascio e selezionare **Salva**.

1. Per pubblicare di nuovo, selezionare **Pubblica**.

Distribuire i file pubblicati con il metodo desiderato. È ad esempio possibile inserire i file in un file *zip*, usare un semplice comando di copia o distribuire i file con un pacchetto di installazione a scelta.

## <a name="next-steps"></a>Passaggi successivi

- [Distribuire un'applicazione .NET Core con lo strumento di pubblicazione](/dotnet/core/deploying/deploy-with-vs?toc=/visualstudio/deployment/toc.json&bc=/visualstudio/deployment/_breadcrumb/toc.json)
- [Creare un pacchetto dell'applicazione desktop per Microsoft Store (Desktop Bridge)](/windows/uwp/porting/desktop-to-uwp-packaging-dot-net?toc=/visualstudio/deployment/toc.json&bc=/visualstudio/deployment/_breadcrumb/toc.json)
- (.NET) [Distribuzione di .NET Framework e delle applicazioni](/dotnet/framework/deployment/)
