---
title: Eseguire il debug di violazioni di accesso durante l'esecuzione di un'app all'esterno del debugger | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.access
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- access violation debugging
- debugging [Visual Studio], access violations
ms.assetid: 780a298a-132e-4245-8370-8c82ca27c6c1
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8b65c10b07b93e657a9e3cb9da5f94d5c9b14362
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53854022"
---
# <a name="how-can-i-debug-access-violations-when-running-my-program-outside-the-debugger"></a>Come è possibile eseguire il debug di violazioni di accesso quando si esegue un programma fuori dal debugger?

## <a name="problem-description"></a>Descrizione del problema  
 Il programma viene eseguito correttamente nell'ambiente di Visual Studio, ma quando viene eseguito autonomamente con il sistema operativo Windows, genera una violazione di accesso. Come è possibile effettuare il debug di questo problema?  
  
## <a name="solution"></a>Soluzione  
 Impostare l'opzione [Debug JIT](../debugger/just-in-time-debugging-in-visual-studio.md) ed eseguire il programma autonomamente finché non si verifica la violazione di accesso. Nella finestra di dialogo **Violazione di accesso** sarà quindi possibile fare clic su **Annulla** per avviare il debugger.  
  
## <a name="see-also"></a>Vedere anche  
 [Domande frequenti sul debug del codice nativo](../debugger/debugging-native-code-faqs.md)   
 [Debug del codice nativo](../debugger/debugging-native-code.md)