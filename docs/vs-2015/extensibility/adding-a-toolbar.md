---
title: Aggiunta di una barra degli strumenti | Microsoft Docs
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
- toolbars [Visual Studio], adding to IDE
- IDE, adding toolbars
ms.assetid: 17302c25-6f59-4e97-8c85-54f95336a07f
caps.latest.revision: 39
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 038b8e8503a89dd0ec565d3d1b5acf20e6437600
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51787952"
---
# <a name="adding-a-toolbar"></a>Aggiunta di una barra degli strumenti
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Questa procedura dettagliata viene illustrato come aggiungere una barra degli strumenti all'IDE di Visual Studio.  
  
 Una barra degli strumenti è visualizzata una striscia orizzontale o verticale che contiene i pulsanti associati a comandi. A seconda della relativa implementazione, una barra degli strumenti nell'IDE possibile riposizionare, ancorato a qualsiasi lato della finestra IDE principale o rendere essere davanti altre finestre.  
  
 Inoltre, gli utenti possono aggiungere comandi a una barra degli strumenti o rimuoverli da esso tramite il **Personalizza** nella finestra di dialogo. In genere, le barre degli strumenti in VSPackage sono personalizzabili dall'utente. L'IDE gestisce tutte le personalizzazioni e il pacchetto VSPackage risponde ai comandi. Il pacchetto VSPackage non è necessario sapere dove è situato fisicamente un comando.  
  
 Per altre informazioni sui menu, vedere [comandi, menu e barre degli strumenti](../extensibility/internals/commands-menus-and-toolbars.md).  
  
## <a name="prerequisites"></a>Prerequisiti  
 A partire da Visual Studio 2015, non installare Visual Studio SDK dall'area download. È incluso come funzionalità facoltativa nel programma di installazione di Visual Studio. È anche possibile installare il SDK di Visual Studio in un secondo momento. Per altre informazioni, vedere [installazione di Visual Studio SDK](../extensibility/installing-the-visual-studio-sdk.md).  
  
## <a name="creating-an-extension-with-a-toolbar"></a>Creazione di un'estensione con una barra degli strumenti  
 Creare un progetto VSIX denominato `IDEToolbar`. Aggiungere un modello di elemento di comando di menu denominato **ToolbarTestCommand**. Per informazioni su come eseguire questa operazione, vedere [creazione di un'estensione con un comando di Menu](../extensibility/creating-an-extension-with-a-menu-command.md).  
  
## <a name="creating-a-toolbar-for-the-ide"></a>Creazione di una barra degli strumenti per l'IDE  
  
1.  In ToolbarTestCommandPackage.vsct, cercare la sezione di simboli. Nell'elemento GuidSymbol denominato guidToolbarTestCommandPackageCmdSet, aggiungere le dichiarazioni per una barra degli strumenti e un gruppo della barra degli strumenti, come indicato di seguito.  
  
    ```xml  
    <IDSymbol name="Toolbar" value="0x1000" />  
    <IDSymbol name="ToolbarGroup" value="0x1050" />  
  
    ```  
  
2.  Nella parte superiore della sezione di comandi, creare una sezione di menu. Aggiungere un elemento Menu con la sezione di menu per definire la barra degli strumenti.  
  
    ```xml  
    <Menus>  
        <Menu guid="guidToolbarTestCommandPackageCmdSet" id="Toolbar"  
            type="Toolbar" >  
            <CommandFlag>DefaultDocked</CommandFlag>  
            <Strings>  
                <ButtonText>Test Toolbar</ButtonText>  
                <CommandName>Test Toolbar</CommandName>  
            </Strings>  
          </Menu>  
    </Menus>  
    ```  
  
     Le barre degli strumenti non possono essere annidati, come sottomenu. Pertanto, non è necessario assegnare un gruppo padre. Inoltre, non è necessario impostare la priorità, perché l'utente può spostare barre degli strumenti. In genere, la posizione iniziale di una barra degli strumenti è definita a livello di codice, ma le successive modifiche dall'utente vengono rese persistenti.  
  
3.  Nel [gruppi](../extensibility/groups-element.md) sezione, dopo la voce di gruppo esistente, definire una [gruppo](../extensibility/group-element.md) elemento per contenere i comandi per la barra degli strumenti.  
  
    ```xml  
    <Group guid="guidToolbarTestCommandPackageCmdSet" id="ToolbarGroup"  
          priority="0x0000">  
      <Parent guid="guidToolbarTestCommandPackageCmdSet" id="Toolbar"/>  
    </Group>  
    ```  
  
4.  Visualizzare il pulsante sulla barra degli strumenti. Nella sezione pulsanti, sostituire il blocco padre nel pulsante alla barra degli strumenti. Il blocco pulsante risultante dovrebbe essere simile al seguente:  
  
    ```xml  
    <Button guid="guidToolbarTestCommandPackageCmdSet" id="ToolbarTestCommandId" priority="0x0100" type="Button">  
        <Parent guid= "guidToolbarTestCommandPackageCmdSet" id="ToolbarGroup" />  
                <Icon guid="guidImages" id="bmpPic1" />  
        <Strings>  
            <ButtonText>Invoke ToolbarTestCommand</ButtonText>  
        </Strings>  
    </Button>  
    ```  
  
     Per impostazione predefinita, se una barra degli strumenti non dispone di alcun comando, non visualizzato.  
  
5.  Compilare il progetto e avviare il debug. L'istanza sperimentale dovrebbe essere visualizzato.  
  
6.  Fare clic sulla barra dei menu di Visual Studio per ottenere l'elenco delle barre degli strumenti. Selezionare **sulla barra degli strumenti di Test**.  
  
7.  Si noterà ora la barra degli strumenti ridotta a icona a destra della scheda Cerca nei icona dei file. Quando si fa clic sull'icona, si dovrebbe essere una finestra di messaggio con la dicitura **ToolbarTestCommandPackage. All'interno di IDEToolbar.ToolbarTestCommand.MenuItemCallback()**.  
  
## <a name="see-also"></a>Vedere anche  
 [Comandi, menu e barre degli strumenti](../extensibility/internals/commands-menus-and-toolbars.md)

