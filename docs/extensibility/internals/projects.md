---
title: I progetti | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- solutions [Visual Studio]
- custom tools [Visual Studio SDK]
- project subtypes [Visual Studio SDK]
- projects [Visual Studio SDK]
- project types [Visual Studio SDK]
ms.assetid: 237742e4-a638-4d5b-a9b3-6a69d627763c
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 893dbdb8a1ff92d338b6e8ee654f60578990c7e2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53876744"
---
# <a name="projects"></a>Progetti
In Visual Studio, i progetti sono contenitori utilizzati dagli sviluppatori per organizzare file di codice sorgente e altre risorse che vengono visualizzati nella **Esplora soluzioni**. In genere, i progetti sono file (ad esempio, un file con estensione csproj per un progetto c#) che archiviano i riferimenti ai file del codice sorgente e le risorse, ad esempio i file bitmap. I progetti consentono di organizzare, compilare, eseguire il debug e distribuire il codice sorgente, i riferimenti a servizi Web e database e altre risorse. I pacchetti VSPackage possono estendere il sistema di progetto di Visual Studio in tre modi principali: *tipi di progetto*, *sottotipi di progetto*, e *strumenti personalizzati*.  
  
## <a name="in-this-section"></a>In questa sezione  
 [Tipi di progetto](../../extensibility/internals/project-types.md)  
 *Tipi di progetto* aggiungere il supporto per nuovi tipi di progetti, ad esempio linguaggi di programmazione. Ad esempio, ogni lingua supportata di Visual Studio ha un proprio tipo di progetto e l'esempio di integrazione di IronPython include un tipo di progetto per il linguaggio IronPython. È necessario creare un tipo di progetto per linguaggi diversi da c# o Visual Basic per personalizzare come gli elementi sono compilati, il debug, distribuiti e visualizzati nella **Esplora soluzioni**. Per altre informazioni, vedere [tipi di progetto](../../extensibility/internals/project-types.md).  
  
 [Sottotipi di progetto](../../extensibility/internals/project-subtypes.md)  
 *Sottotipi di progetto* sono basati sui tipi di progetto e può essere utilizzato per personalizzare il modo in cui i progetti vengono compilati, il debug e distribuiti. Visual Studio Usa sottotipi di progetto con i progetti Smart Device. la personalizzazione di distribuzione tramite la copia di un programma appena compilato da un computer di sviluppo nel dispositivo di destinazione. I tipi di progetto Visual Basic e c# possono essere utilizzati come base per sottotipi di progetto; Tipi di progetto C++ non è possibile. Tipi di progetto personalizzati nonché come base per sottotipi di progetto. Per altre informazioni, vedere [sottotipi di progetto](../../extensibility/internals/project-subtypes.md).  
  
 [Progetti Web](../../extensibility/internals/web-projects.md)  
 Viene illustrato il progetto Web, che consentono di creare applicazioni Web.  
  
 [Nuova generazione del progetto: Dietro le quinte, parte 1](../../extensibility/internals/new-project-generation-under-the-hood-part-one.md) e [nuova generazione progetto: Dietro le quinte, parte 2](../../extensibility/internals/new-project-generation-under-the-hood-part-two.md)  
 Viene illustrato ciò che effettivamente si verifica quando si crea un nuovo progetto.  
  
 [Esempi di VSSDK](http://aka.ms/vs2015sdksamples)  
 Contiene gli esempi VSSDK che trattano di progetti e soluzioni.  
  
## <a name="related-sections"></a>Sezioni correlate  
 [Componenti e funzionalità di Visual Studio SDK](../../extensibility/internals/inside-the-visual-studio-sdk.md)  
 Illustra diversi aspetti di estendibilità di Visual Studio.