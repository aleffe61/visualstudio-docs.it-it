---
title: Sostituire una variabile temporanea con il valore corrispondente
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: aa329dd3fe7d01046c35be9829aed4ca4519c3e1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53909034"
---
# <a name="inline-a-temporary-variable-refactoring"></a>Refactoring con variabile temporanea inline

Questo refactoring si applica a:

- C#

- Visual Basic

**Cosa:** consente di rimuovere una variabile temporanea e sostituirla con il valore corrispondente.

**Quando:** l'uso della variabile temporanea rende più difficile la comprensione del codice.

**Perché?:** la rimozione di una variabile temporanea può migliorare la leggibilità del codice.

## <a name="how-to"></a>Procedura

1. Evidenziare o posizionare il cursore di testo all'interno della variabile temporanea da rendere inline:

   - C#:

       ![Codice evidenziato - C#](media/inline-highlight-cs.png)

   - Visual Basic:

       ![Codice evidenziato - Visual Basic](media/inline-highlight-vb.png)

2. Eseguire quindi una delle operazioni seguenti:

   - **Tastiera**
      - Premere **CTRL**+**.** per attivare il menu **Azioni rapide e refactoring**.
   - **Mouse**
      - Fare clic con il pulsante destro del mouse sul codice e scegliere il menu **Azioni rapide e refactoring**.

3. Selezionare **Variabile temporanea Inline** dal popup della finestra di anteprima.

   La variabile viene rimossa e i relativi utilizzi sostituiti con il valore della variabile.

   - C#:

      ![Risultato inline - C#](media/inline-result-cs.png)

   - Visual Basic:

      ![Risultato inline - Visual Basic](media/inline-result-vb.png)

## <a name="see-also"></a>Vedere anche

- [Refactoring](../refactoring-in-visual-studio.md)