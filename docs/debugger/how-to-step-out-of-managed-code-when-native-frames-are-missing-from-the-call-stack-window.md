---
title: Passaggio di C# il codice quando sono visualizzati frame nativi mancanti dallo stack di chiamate | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
- SQL
helpviewer_keywords:
- Call Stack window, missing native frames
- code, managed code
- native frames
- stepping, out of managed code
- managed code, stepping out of
ms.assetid: 97cdd2a8-02a9-4a06-a5b1-c92b1e431979
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 741afb6befdbc29cafab39c3c9b0d7bb2761d7b1
ms.sourcegitcommit: 708f77071c73c95d212645b00fa943d45d35361b
ms.translationtype: MTE95
ms.contentlocale: it-IT
ms.lasthandoff: 12/07/2018
ms.locfileid: "53057652"
---
# <a name="how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window"></a>Procedura: Uscire da codice gestito quando sono visualizzati frame nativi mancanti dalla finestra Stack di chiamate

Se il codice contiene frame nativi non visibili nella finestra **Stack di chiamate**, l'uscita dal codice gestito può produrre risultati imprevisti. Una soluzione possibile consiste nell'utilizzare un punto di interruzione invece del comando **Esci da istruzione/routine**.

> [!NOTE]
> Le finestre di dialogo e i comandi di menu visualizzati potrebbero essere diversi da quelli descritti nella Guida a seconda delle impostazioni attive o dell'edizione del programma. Per modificare le impostazioni, scegliere **Importa/Esporta impostazioni** dal menu **Strumenti** . Per altre informazioni, vedere [Reimpostare le impostazioni](../ide/environment-settings.md#reset-settings).

## <a name="step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-display"></a>Uscire da codice gestito quando nella visualizzazione dello stack di chiamate non sono visualizzati frame nativi

1.  Nel codice nativo impostare un punto di interruzione di posizione dopo la chiamata a codice gestito.

2.  Scegliere **Continua** dal menu **Debug**.

     Una volta completata la chiamata gestita, l'esecuzione si interromperà in corrispondenza del punto di interruzione nel codice nativo.

## <a name="see-also"></a>Vedere anche

- [Procedura: Usare la finestra Stack di chiamate](../debugger/how-to-use-the-call-stack-window.md)