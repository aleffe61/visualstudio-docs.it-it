---
title: L'eliminazione di un punto di interruzione | Microsoft Docs
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
- breakpoints, deleting
- debugging [Debugging SDK], deleting breakpoints
ms.assetid: 75a046cc-d20a-4c79-ad2d-1f18426ac5d0
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b53be5e09d4579d95cb4b9d9726d6087effb8ff1
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51797390"
---
# <a name="deleting-a-breakpoint"></a>Eliminazione di un punto di interruzione
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Di seguito viene descritto il processo quando si elimina un punto di interruzione in sospeso:  
  
## <a name="deletion-process"></a>Processo di eliminazione  
 Gestore di sessione di debug (SDM) chiama il [IDebugPendingBreakpoint2::Delete](../../extensibility/debugger/reference/idebugpendingbreakpoint2-delete.md) metodo per rimuovere il punto di interruzione in sospeso e i punti di interruzione con tutti i binding associati da quest'ultimo.  
  
> [!NOTE]
>  È inoltre possibile rimuovere un singolo punto di interruzione associato da una chiamata a [IDebugBoundBreakpoint2::Delete](../../extensibility/debugger/reference/idebugboundbreakpoint2-delete.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Chiamata degli eventi del debugger](../../extensibility/debugger/calling-debugger-events.md)

