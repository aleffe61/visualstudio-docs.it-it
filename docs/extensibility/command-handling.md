---
title: La gestione dei comandi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - command handling
ms.assetid: 78f67d92-77f7-45cb-ad75-6e3346379cc3
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 4198cf6bbed2d8f6172872e4f98f1edb4749e7d7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53926320"
---
# <a name="command-handling"></a>Gestione dei comandi
L'editor è possibile definire nuovi comandi. I comandi vengono in genere visualizzati in un menu, in una barra degli strumenti o in un menu di scelta rapida.  
  
 Per altre informazioni sulla definizione dei comandi e menu, vedere [comandi, menu e barre degli strumenti](../extensibility/internals/commands-menus-and-toolbars.md).  
  
 Un servizio di linguaggio è possibile controllare il menu di scelta rapida vengono visualizzati nell'editor, mediante l'intercettazione di <xref:Microsoft.VisualStudio.VSConstants.VSStd2KCmdID> enumerazione. In alternativa, è possibile controllare il menu di scelta rapida in base al marcatore. Per altre informazioni, vedere [comandi importanti per i filtri dei servizi di linguaggio](../extensibility/internals/important-commands-for-language-service-filters.md).  
  
## <a name="add-commands-to-the-editor-context-menu"></a>Aggiungere comandi al menu di scelta rapida editor  
 Per aggiungere un comando di menu di scelta rapida, è innanzitutto necessario definire un set di comandi di menu che appartengono a un gruppo specifico. L'esempio seguente è tratto dal *vsct* file generato come parte della procedura dettagliata [procedura dettagliata: Aggiungere funzionalità a un editor personalizzato](../extensibility/walkthrough-adding-features-to-a-custom-editor.md):  
  
 \<Menu guid = "guidCustomEditorCmdSet" id = "IDMX_RTF" priorità = "0x0000" type = "Contesto" >  
  
 \<Guid padre = "guidCustomEditorCmdSet" id = "0" / >  
  
 \<Le stringhe >  
  
 \<ButtonText > menu di scelta rapida di CustomEditor\</ButtonText >  
  
 \<CommandName > CustomEditorContextMenu\</CommandName >  
  
 \</ Stringhe di >  
  
 \</ Menu >  
  
 \<E menu >  
  
 Il testo precedente aggiunge un comando di menu di scelta rapida con il testo **menu di scelta rapida CustomEditor**. Il GUID del Menu fa parte del set di comandi che viene creato con questo editor. Il tipo è "Context".  
  
 È anche possibile usare comandi predefiniti che non devono essere definite nel *vsct* file. Ad esempio, esaminare i *EditorPane.cs* file generato dal modello di pacchetto di Visual Studio. Si noterà che un set di comandi predefiniti, ad esempio <xref:Microsoft.VisualStudio.VSConstants.VSStd97CmdID> definito da <xref:Microsoft.VisualStudio.VSConstants.GUID_VSStandardCommandSet97>, vengono gestiti nei gestori comando, ad esempio il `onSelectAll` (metodo).  
  
## <a name="see-also"></a>Vedere anche  
 [I comandi, menu e barre degli strumenti](../extensibility/internals/commands-menus-and-toolbars.md)