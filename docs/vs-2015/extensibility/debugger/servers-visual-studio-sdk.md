---
title: Server (Visual Studio SDK) | Microsoft Docs
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
- servers, debugging
- debugging [Debugging SDK], servers
ms.assetid: 62236d64-7956-448c-9ac3-5528f3edac1d
caps.latest.revision: 18
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 20b1550773be903f3f5a0482d2971a4f5b30fabc
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51727164"
---
# <a name="servers-visual-studio-sdk"></a>Server (Visual Studio SDK)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

In termini di architettura del debugger, un **server**:  
  
-   È un contenitore delle porte e fornitori di porte e viene usato per comunicare le porte e fornitori di porte al gestore di sessione di debug (SDM) e motori di debug.  
  
-   Può identificarsi in base al nome ed enumerare le porte e i fornitori di porte.  
  
-   È rappresentato da un [IDebugCoreServer2](../../extensibility/debugger/reference/idebugcoreserver2.md) interfaccia, che viene implementato solo da Visual Studio (un'istanza di un server per ogni istanza di esecuzione di Visual Studio).  
  
## <a name="see-also"></a>Vedere anche  
 [Porte](../../extensibility/debugger/ports.md)   
 [Fornitori di porte](../../extensibility/debugger/port-suppliers.md)   
 [Concetti relativi al debugger](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugCoreServer2](../../extensibility/debugger/reference/idebugcoreserver2.md)

