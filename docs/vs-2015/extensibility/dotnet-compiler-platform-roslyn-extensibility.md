---
title: .NET compiler Platform (&quot;Roslyn&quot;) estendibilità | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 564201b3-1e18-4b88-b615-42c2f57f3fe8
caps.latest.revision: 5
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: de01ec4f857042c6eaaaa70632b28cfc830886cb
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51817087"
---
# <a name="net-compiler-platform-quotroslynquot-extensibility"></a>Estendibilità di .NET Compiler Platform (&quot;Roslyn&quot;)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Lo scopo fondamentale di .NET Compiler Platform ("Roslyn") è di aprire i compilatori c# e Visual Basic e consentendo di strumenti e agli sviluppatori di condividere i compilatori di informazioni dettagliate sui programmi. Strumenti di analisi codice migliorare la qualità del codice e generatori aiuto nella costruzione dell'applicazione del codice. Man mano che strumenti acquisisce più intelligenti, devono accedere a più e più della conoscenza di codice avanzato che possiedono solo dai compilatori. Anziché essere opachi traduttori (codice sorgente e oggetto codice out), i compilatori Roslyn offrono API che è possibile usare per le attività correlate a codice negli strumenti e applicazioni.  
  
 L'aspetto più interessante è che i compilatori Roslyn, le relative API, esempi e procedure dettagliate e gli strumenti reali partendo da queste API sono tutte completamente open source in [github.com/dotnet/roslyn](https://github.com/dotnet/Roslyn). Visitare il sito di SharePoint Server per altre informazioni e iniziare a usare Roslyn. Sono disponibili collegamenti per ottenere le funzionalità di Visual Basic che è possibile usare come un utente finale e più recenti c#, nonché i collegamenti per iniziare a usare come generatore strumento sfruttando APIs Roslyn.  
  
## <a name="see-also"></a>Vedere anche  
 [Introduzione agli analizzatori di Roslyn](../extensibility/getting-started-with-roslyn-analyzers.md)

