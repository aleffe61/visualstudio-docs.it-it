---
title: Con il Store impostazioni | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Settings Store, using
ms.assetid: 447ec08a-eca5-40b8-89b0-f98fdf3d39a4
caps.latest.revision: 29
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0b106604455814e8d8ed13a6c6e1eb3a2d8196b8
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47532136"
---
# <a name="using-the-settings-store"></a>Uso dell'archivio delle impostazioni
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [usando le impostazioni Store](https://docs.microsoft.com/visualstudio/extensibility/using-the-settings-store).  
  
Esistono due tipi di archivi di impostazioni:  
  
-   Impostazioni di configurazione, che sono impostazioni di Visual Studio e package VS di sola lettura. Visual Studio unisce le impostazioni da tutti i file con estensione pkgdef noti in questo archivio.  
  
-   Impostazioni utente, che sono impostazioni scrivibile, ad esempio quelli che vengono visualizzati nelle pagine di **opzioni** nella finestra di dialogo Pagine delle proprietà e alcune altre finestre di dialogo. Estensioni di Visual Studio possono usarle per l'archiviazione locale di piccole quantità di dati.  
  
 Questa procedura dettagliata illustra come leggere i dati dall'archivio di impostazione di configurazione. Visualizzare [scrivendo la Store impostazioni utente](../extensibility/writing-to-the-user-settings-store.md) per una spiegazione di come scrivere nell'archivio delle impostazioni utente.  
  
## <a name="creating-the-example-project"></a>Creazione del progetto di esempio  
 Questa sezione illustra come creare un progetto di estensione semplice con un comando di menu a scopo dimostrativo.  
  
1.  Ogni estensione di Visual Studio inizia con un progetto di distribuzione VSIX che contiene gli asset di estensione. Creare un [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] progetto VSIX denominato `SettingsStoreExtension`. È possibile trovare il modello di progetto VSIX nel **nuovo progetto** nella finestra di dialogo **Visual c# / Extensibility**.  
  
2.  A questo punto aggiungere un modello di elemento di comando personalizzato denominato **SettingsStoreCommand**. Nel **Aggiungi nuovo elemento** finestra di dialogo passa alla **Visual c# / Extensibility** e selezionare **comando personalizzato**. Nel **Name** campo nella parte inferiore della finestra, modificare il nome di file di comando da **SettingsStoreCommand.cs**. Per altre informazioni su come creare un comando personalizzato, vedere [creazione di un'estensione con un comando di Menu](../extensibility/creating-an-extension-with-a-menu-command.md)  
  
## <a name="using-the-configuration-settings-store"></a>Con il Store le impostazioni di configurazione  
 In questa sezione viene illustrato come rilevare e visualizzare le impostazioni di configurazione.  
  
1.  Nel file SettingsStorageCommand.cs, aggiungere quanto segue usando istruzioni:  
  
    ```  
    using System.Collections.Generic;  
    using Microsoft.VisualStudio.Settings;  
    using Microsoft.VisualStudio.Shell.Settings;  
    using System.Windows.Forms;  
    ```  
  
2.  In `MenuItemCallback`, rimuovere il corpo del metodo e aggiungere l'archivio delle impostazioni di configurazione di ottenere le righe seguenti:  
  
    ```  
    SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
    SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
    ```  
  
     Il <xref:Microsoft.VisualStudio.Shell.Settings.ShellSettingsManager> è una classe helper gestita tramite il <xref:Microsoft.VisualStudio.Shell.Interop.IVsSettingsManager> servizio.  
  
3.  A questo punto è scoprire se sono installati gli strumenti di Windows Phone. Il codice dovrebbe essere simile al seguente:  
  
    ```  
    private void MenuItemCallback(object sender, EventArgs e)  
    {  
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
        SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
        bool arePhoneToolsInstalled = configurationSettingsStore.CollectionExists(@"InstalledProducts\Microsoft Windows Phone Developer Tools");  
        string message = "Microsoft Windows Phone Developer Tools: " + arePhoneToolsInstalled;  
        MessageBox.Show(message);  
    }  
    ```  
  
4.  Testare il codice. Compilare il progetto e avviare il debug.  
  
5.  Nell'istanza sperimentale, sul **degli strumenti** menu, fare clic su **SettingsStoreCommand richiamare**.  
  
     Si dovrebbe vedere un messaggio **Microsoft Windows Phone Developer Tools:** aggiungendo **True** oppure **False**.  
  
 Visual Studio mantiene l'archivio delle impostazioni nel Registro di sistema.  
  
#### <a name="to-use-a-registry-editor-to-verify-configuration-settings"></a>Usare un editor del Registro di sistema per verificare le impostazioni di configurazione  
  
1.  Aprire Regedit.exe.  
  
2.  Passare a HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\14.0Exp_Config\InstalledProducts\\.  
  
    > [!NOTE]
    >  Assicurarsi che si sta esaminando la chiave che contiene \14.0Exp_Config\ e non \14.0_Config\\. Quando si esegue l'istanza sperimentale di Visual Studio, le impostazioni di configurazione disponibili nell'hive del Registro di sistema "14.0Exp_Config".  
  
3.  Espandere il nodo \Installed Products\. Se il messaggio nei passaggi precedenti **installata di Microsoft Windows Phone Developer Tools: True**, \Installed Products\ deve contenere un nodo di Microsoft Windows Phone Developer Tools. Se il messaggio **installata di Microsoft Windows Phone Developer Tools: False**, quindi \Installed Products\ non deve contenere un nodo di Microsoft Windows Phone Developer Tools.
