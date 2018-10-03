---
title: Usando tipi di carattere e colori | Microsoft Docs
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
- fonts, controlling in IDE
- IDE, controlling text color and fonts
- Fonts and Colors property page
- font and color control [Visual Studio SDK]
- text, IDE
ms.assetid: d1a9b99f-fbdc-45ed-920a-e08c3d931ac9
caps.latest.revision: 28
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6db4f030a3367a5fd2fb449b3515643fe6cd6033
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47518245"
---
# <a name="using-fonts-and-colors"></a>Usando tipi di carattere e colori
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [utilizzando i tipi di carattere e colori](https://docs.microsoft.com/visualstudio/extensibility/using-fonts-and-colors).  
  
Il [!INCLUDE[vsipsdk](../includes/vsipsdk-md.md)] fornisce il supporto per l'utilizzo di tipi di carattere e colori per visualizzare il testo.  
  
## <a name="in-this-section"></a>In questa sezione  
 [Panoramica di tipi di carattere e colori](../extensibility/font-and-color-overview.md)  
 Vengono illustrate impostazioni testo di carattere e colori nella [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] ambiente di sviluppo integrato (IDE). Inoltre vengono illustrati i concetti di categorie e di elementi visualizzati e viene descritto come i pacchetti VSPackage e l'editor principale di utilizzare gli attributi di testo.  
  
 [Recupero di informazioni su tipi di carattere e colori per la colorazione del testo](../extensibility/getting-font-and-color-information-for-text-colorization.md)  
 Vengono fornite linee guida per l'implementazione di colorazione del testo nei pacchetti VSPackage che gestiscono **categorie** diverso da **Editor di testo**.  
  
 [Accesso alle impostazioni di tipi di carattere e colori archiviate](../extensibility/accessing-stored-font-and-color-settings.md)  
 Illustra la modalità corrente di carattere e colori impostazioni possano essere archiviate, recuperate e applicate.  
  
 [Implementazione di categorie ed elementi di visualizzazione personalizzati](../extensibility/implementing-custom-categories-and-display-items.md)  
 Descrive i passaggi di base mediante il quale è possibile creare e usare il proprio di una finestra **elementi visualizzati** e **categorie** per supportare la visualizzazione del testo.  
  
 Questo approccio richiede un pacchetto VSPackage implementare il <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider> interfaccia e interfacce correlate.  
  
 [Procedura: Accedere i tipi di carattere e alle combinazioni colori predefiniti](../extensibility/how-to-access-the-built-in-fonts-and-color-scheme.md)  
 Viene illustrato come definire e registrare una categoria, utilizzando i colori e tipi di carattere incorporati e avviare l'uso di caratteri fornita dal sistema e i colori.  
  
## <a name="reference"></a>Riferimenti  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider>  
 Fornisce un'istanza del `IVsFontAndColorDefaults` o il <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup> interfaccia che corrisponde a un determinato elemento presente nel **Mostra impostazioni per** nell'elenco il **tipi di carattere e colori** pagina della finestra di **Opzioni** nella finestra di dialogo.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults>  
 Consente a un pacchetto VSPackage a supporto dell'IDE **Fonts and Colors** pagina mediante la definizione di tipi di carattere predefiniti e i colori per una finestra o un componente dell'interfaccia utente.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup>  
 Fornisce un meccanismo mediante il quale un pacchetto VSPackage che fornisce il supporto del tipo di carattere e colore può specificare un gruppo di elemento visualizzato - una categoria superiore che rappresenta l'unione di due o più categorie.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage>  
 Consente a un VSPackage di recuperare i dati di carattere e colori oppure salvarlo nel Registro di sistema.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorEvents>  
 Notifica ai pacchetti VSPackage che utilizzano le informazioni di carattere e colori sulle modifiche nelle impostazioni del tipo di carattere e colore.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorUtilities>  
 Fornisce gli strumenti per lavorare con i dati di input e outpui che viene usati dai metodi della [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] **carattere e colori** meccanismo.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorCacheManager>  
 Controlla la memorizzazione nella cache delle impostazioni del tipo di carattere e colore.  
  
## <a name="related-sections"></a>Sezioni correlate  
 [Sviluppo di un servizio di linguaggio legacy](../extensibility/internals/developing-a-legacy-language-service.md)  
 Illustra come i pacchetti VSPackage possono usare servizi di linguaggio per personalizzare il [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] editor.  
  
 [Colorazione della sintassi negli editor personalizzati](../extensibility/syntax-coloring-in-custom-editors.md)  
 Descries il [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] editor utilizza servizi di linguaggio per implementare la colorazione della sintassi.  
  
 [Estensione di altre parti di Visual Studio](../extensibility/extending-other-parts-of-visual-studio.md)  
 Viene illustrato come utilizzare [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] per creare elementi dell'interfaccia utente che corrispondono al resto dei servizi [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].
