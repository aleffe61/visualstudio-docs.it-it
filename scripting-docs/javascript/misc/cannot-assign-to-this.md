---
title: Non è possibile assegnare a 'this' | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT5000
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: ba2b0a2b-f0f8-4698-b335-a4ab6c166671
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f47778075b0395e4f0791d8f485188d40fab87a4
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/27/2018
ms.locfileid: "53802592"
---
# <a name="cannot-assign-to-this"></a>Assegnazione a 'this' non consentita
Si è provato ad assegnare un valore per **ciò**. **Ciò** è un [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] parola chiave che fa riferimento a:

- l'oggetto attualmente in esecuzione un metodo,

- l'oggetto globale, se nessun metodo corrente (o il metodo non appartiene a qualsiasi altro oggetto).

Un metodo è un [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] funzione che viene richiamato tramite un oggetto. All'interno di un metodo, il **ciò** è un riferimento all'oggetto è stato richiamato il metodo tramite la parola chiave (che sembra essere l'oggetto creato tramite la chiamata al costruttore di classe con il **nuovi** operatore).

All'interno di un metodo, è possibile usare **ciò** per fare riferimento all'oggetto corrente, ma è possibile assegnare un nuovo valore per **ciò**.

## <a name="to-correct-this-error"></a>Per correggere l'errore

- Non tentare di assegnare ai **ciò**. Per accedere a una proprietà o metodo di un oggetto istanza, usare l'operatore punto (ad esempio, **circle.radius**).

  > [!NOTE]
  > È possibile assegnare il nome variabile creata dall'utente **ciò**; è un [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] parola riservata.

## <a name="see-also"></a>Vedere anche

- [Istruzione this](../../javascript/reference/this-statement-javascript.md)
- [Risoluzione dei problemi relativi agli script](../../javascript/advanced/troubleshooting-your-scripts-javascript.md)