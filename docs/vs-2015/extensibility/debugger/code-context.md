---
title: Codice contesto | Microsoft Docs
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
- debugging [Debugging SDK], contexts
ms.assetid: 65e4d37a-086b-426e-9394-a3534967fd59
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1c9bdd138fbbfb4eea29004db5eb1e92814bdfec
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51753661"
---
# <a name="code-context"></a>Contesto del codice
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nelle [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] debug, una **contesto codice**:  
  
-   Fornisce un'astrazione di una posizione nel codice come nota al motore di debug (DE). Per la maggior parte delle architetture di run-time oggi, un contesto del codice può essere considerato come un indirizzo nel flusso di istruzioni del programma. Per le lingue non convenzionale, dove codice non può essere rappresentato da istruzioni, un contesto del codice può essere rappresentato da un altro modo.  
  
-   Descrive la posizione corrente nel flusso di esecuzione del programma in fase di debug.  
  
-   Esiste solo quando un programma è stata interrotta in un punto di interruzione.  
  
-   Ha un contesto di documento associato.  
  
-   Viene implementato da un [IDebugCodeContext2](../../extensibility/debugger/reference/idebugcodecontext2.md) interfaccia.  
  
## <a name="see-also"></a>Vedere anche  
 [Contesto di documento](../../extensibility/debugger/document-context.md)   
 [Contesti del debugger](../../extensibility/debugger/debugger-contexts.md)

