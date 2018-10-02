---
title: DebugBreak e DebugBreak | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- DebugBreak
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- debugging [C++], DebugBreak function
- DebugBreak function
- breakpoints, DebugBreak function
ms.assetid: 9787c795-df94-4f48-bc8d-3bf899b67421
caps.latest.revision: 26
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 005490038b293dbb644ec99ca2fbeaa77c0eb2c9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47532514"
---
# <a name="debugbreak-and-debugbreak"></a>DebugBreak e __debugbreak
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [DebugBreak e DebugBreak](https://docs.microsoft.com/visualstudio/debugger/debugbreak-and-debugbreak).  
  
È possibile chiamare la funzione DebugBreak Win32 o la [DebugBreak](http://msdn.microsoft.com/library/1d1e1c0c-891a-4613-ae4b-d790094ba830) intrinseco in qualsiasi punto nel codice. `DebugBreak` e `__debugbreak` hanno lo spesso effetto dell'impostazione di un punto di interruzione nella stessa posizione.  
  
 Poiché `DebugBreak` è una chiamata a una funzione di sistema, è necessario che siano installati i simboli di debug del sistema per garantire che vengano visualizzate le informazioni corrette sullo stack di chiamate dopo l'interruzione. In alternativa, le informazioni sullo stack di chiamate visualizzate dal debugger possono essere spostate di un frame. Se si usa `__debugbreak`, i simboli non sono obbligatori.  
  
## <a name="see-also"></a>Vedere anche  
 [Intrinseci del compilatore](http://msdn.microsoft.com/library/48bb9929-7d78-4fd8-a092-ae3c9f971858)   
 [Sicurezza del debugger](../debugger/debugger-security.md)   
 [Debug del codice nativo](../debugger/debugging-native-code.md)   
 [Specificare file di simboli (PDB) e di origine](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)


