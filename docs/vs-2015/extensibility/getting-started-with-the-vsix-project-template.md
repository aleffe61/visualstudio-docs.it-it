---
title: Introduzione al modello di progetto VSIX | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Visual Studio SDK, VSIX project template
ms.assetid: 89fac33e-9380-4723-9b45-048a6e16f0ed
caps.latest.revision: 26
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1f7230bce49342ad8e31baeb3f46c72f1c45d776
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51787731"
---
# <a name="getting-started-with-the-vsix-project-template"></a>Introduzione al modello di progetto VSIX
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

È possibile usare il modello di progetto VSIX per creare un'estensione o per un'estensione esistente per la distribuzione del pacchetto. Il modello di progetto VSIX contiene le versioni di Visual Basic e Visual c# e viene installato come parte di Visual Studio SDK.  
  
 Il modello di progetto VSIX semplicemente è costituito da un file vsixmanifest, che contiene informazioni sull'estensione e gli asset che è disponibile.  
  
 Per trovare il modello di progetto VSIX, è necessario installare Visual Studio SDK. Per altre informazioni, vedere [Visual Studio SDK](../extensibility/visual-studio-sdk.md).  
  
## <a name="deploying-a-custom-project-template-using-the-vsix-project-template"></a>Distribuzione di un modello di progetto personalizzati usando il modello di progetto VSIX  
 I passaggi seguenti illustrano come usare il progetto VSIX per creare un pacchetto di un modello di progetto che è possibile condividere con altri sviluppatori o caricare in Visual Studio Gallery.  
  
1.  Creare un modello di progetto.  
  
    1.  Aprire il progetto da cui creare un modello. Questo progetto può essere di qualsiasi tipo di progetto.  
  
    2.  Nel menu **File** scegliere**Esporta modello**. Completare i passaggi della procedura guidata.  
  
         Viene creato un file con estensione zip in %USERPROFILE%\My Documents\Visual Studio  *\<versione >* \My Exported Templates\\.  
  
2.  Creare un progetto VSIX vuoto.  
  
     Scegliere **Nuovo** dal menu **File** , quindi fare clic su **Progetto**. Selezionare uno **Visual Basic** oppure **Visual c#**. Sotto il nodo selezionato, selezionare **estendibilità**, quindi selezionare **progetto VSIX**.  
  
3.  Aggiungere il file con estensione zip per il progetto. Impostare relativi **copia in Directory di Output** proprietà `Copy Always`.  
  
4.  Nel **Esplora soluzioni**, fare doppio clic il `source.extension.vsixmanifest` file per aprirlo nel **progettazione del manifesto VSIX**e quindi apportare le modifiche seguenti:  
  
    -   Impostare il **Product Name** campo **risorse del modello di progetto**.  
  
    -   Impostare il **ID prodotto** campo **MyProjectTemplate - 1**.  
  
    -   Impostare il **Author** campo **Fabrikam**.  
  
    -   Impostare il **descrizione** campo **modello di progetto personale**.  
  
    -   Nel **Assets** sezione, aggiungere un **Microsoft.VisualStudio.ProjectTemplate** digitare e impostarne il percorso per il nome del file con estensione zip.  
  
5.  Salvare e chiudere il file vsixmanifest.  
  
6.  Compilare il progetto.  
  
7.  Nella directory di output, fare doppio clic sul file con estensione VSIX.  
  
8.  Oggetto **programma di installazione VSIX** verrà visualizzata la finestra di messaggio. Seguire le istruzioni per installare l'estensione.  
  
9. Chiudere Visual Studio e quindi aprirlo nuovamente.  
  
10. Selezionare **estensioni e aggiornamenti** (nel **Tools** menu) e selezionare il **modelli** categoria. Deve essere una delle estensioni disponibili **modello di progetto personale**.  
  
11. Il nuovo modello di progetto viene visualizzato nei **nuovo progetto** finestra di dialogo nella stessa posizione come il modello di progetto originale. Ad esempio, se è stato creato un modello denominato **VB Console** da un'applicazione console Visual Basic, **Console di Visual Basic** viene visualizzato nel riquadro stesso come Visual Basic **applicazione Console**modello.  
  
#### <a name="to-specify-the-location-of-the-template-in-the-new-project-dialog-box"></a>Per specificare il percorso del modello nella finestra di dialogo Nuovo progetto  
  
1.  Cartelle dei modelli si trovano nel *percorso di installazione di Visual Studio*\Common7\IDE\ProjectTemplates e *percorso di installazione di Visual Studio*\Common7\IDE\ItemTemplates directory. I nomi delle sezioni di primo livello nella finestra di dialogo Nuovo progetto non corrispondono esattamente i nomi delle cartelle dei modelli. Dove si differenziano, usare il nome della cartella del modello.  
  
     Modificare l'estensione di file con estensione VSIX in. zip e quindi aprire il file.  
  
2.  Creare una nuova cartella con lo stesso nome della sezione della finestra di dialogo Nuovo progetto in che di modello deve essere visualizzato.  
  
3.  Se il modello deve trovarsi in una sottosezione, creare una sottocartella con lo stesso nome.  
  
4.  Spostare il file zip del modello nella nuova cartella.  
  
5.  Modificare l'estensione zip in VSIX.  
  
6.  Aprire il manifesto VSIX.  
  
7.  Nel manifesto VSIX, aggiornare il **Asset** percorso del modello in modo che punti alla radice della struttura di directory che contiene il file di modello. Ad esempio, se il modello è in \CSharp\Windows, \CSharp deve puntare il riferimento.

