---
title: Editor e linguaggio servizio estensioni | Microsoft Docs
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
- editors [Visual Studio SDK]
ms.assetid: 5653bac9-724f-4948-a820-68ce6aa96365
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b5e0b568cee873d29f73eb2b81e38d49b76b5844
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51778761"
---
# <a name="editor-and-language-service-extensions"></a>Estensioni dell'editor e dei servizi di linguaggio
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

È possibile estendere la maggior parte delle funzionalità dell'editor del codice di Visual Studio. L'editor basato su Windows Presentation Foundation (WPF) e viene scritto in codice gestito. Anche se questa progettazione è diverso dalle progettazioni nelle versioni precedenti di Visual Studio, fornisce la maggior parte delle stesse funzionalità. Per estendere l'editor, usare Managed Extensibility Framework (MEF).  
  
 Visual Studio SDK fornisce adapter detto *shim* per supportare i pacchetti VSPackage che sono state scritte per versioni precedenti. Tuttavia, se si dispone di un pacchetto VSPackage esistente, è consigliabile aggiornarla per la nuova tecnologia per ottenere affidabilità e prestazioni migliori.  
  
## <a name="related-topics"></a>Argomenti correlati  
  
|Titolo|Descrizione|  
|-----------|-----------------|  
|[Creazione di un'estensione con un modello di elemento dell'editor](../extensibility/creating-an-extension-with-an-editor-item-template.md)|Introduzione all'uso di modelli di elemento dell'Editor.|  
|[Estensione dell'editor e dei servizi di linguaggio](../extensibility/extending-the-editor-and-language-services.md)|Collegamenti ai documenti che presentano la progettazione e le funzionalità dell'editor di base e mostrano come estendere la soluzione.|  
|[Interfacce legacy nell'editor](../extensibility/legacy-interfaces-in-the-editor.md)|Collegamenti ai documenti che illustrano come accedere all'editor di core da codice esistente.|  
|[Creazione di finestre di progettazione ed editor personalizzati](../extensibility/creating-custom-editors-and-designers.md)|Include collegamenti a documenti che illustrano come creare editor personalizzati.|  
|[Estendibilità dei servizi di linguaggio legacy](../extensibility/internals/legacy-language-service-extensibility.md)|Include collegamenti a documenti che descrivono come integrare i linguaggi di programmazione in Visual Studio.|  
|[Managed Extensibility Framework (MEF)](http://msdn.microsoft.com/library/6c61b4ec-c6df-4651-80f1-4854f8b14dde)|Introduce Managed Extensibility Framework (MEF).|  
|[Windows Presentation Foundation](http://msdn.microsoft.com/library/f667bd15-2134-41e9-b4af-5ced6fafab5d)|Introduce di Windows Presentation Foundation (WPF).|

