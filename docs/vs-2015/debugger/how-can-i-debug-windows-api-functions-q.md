---
title: Come è possibile eseguire il debug di funzioni API Windows? | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.api
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- debugging [C++], Windows API functions
- NT symbols and debugging Windows API functions
- Windows API functions, debugging
- Windows API, debugging API functions
- APIs, debugging
ms.assetid: 7c126f57-62ab-4d94-9805-632d696ba1f0
caps.latest.revision: 23
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a84414c6e4d6b46cc0429fb03fd739d1dff94065
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51735629"
---
# <a name="how-can-i-debug-windows-api-functions"></a>Come è possibile eseguire il debug di funzioni API Windows?
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Per eseguire il debug di una funzione API Windows con NT Symbols caricato, effettuare le operazioni seguenti.  
  
### <a name="to-set-a-breakpoint-on-a-windows-api-function-with-nt-symbols-loaded"></a>Per impostare un punto di interruzione su una funzione Windows API con NT Symbols caricato  
  
-   Immettere il nome della funzione e il nome della DLL in cui risiede la funzione. Nel codice a 32 bit, utilizzare la forma decorata del nome della funzione. Per impostare un punto di interruzione **MessageBeep**, ad esempio, è necessario immettere quanto segue.  
  
    ```  
    {,,USER32.DLL}_MessageBeep@4  
    ```  
  
     Per ottenere il nome decorato, vedere [visualizzazione di nomi decorati](http://msdn.microsoft.com/en-us/f79e2717-a4db-4d12-a689-69830cce2be0).  
  
## <a name="see-also"></a>Vedere anche  
 [Domande frequenti sul codice nativo debug](../debugger/debugging-native-code-faqs.md)   
 [Debug del codice nativo](../debugger/debugging-native-code.md)



