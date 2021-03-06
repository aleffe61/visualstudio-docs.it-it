---
title: 'CA1030: Utilizzare eventi dove appropriato | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- UseEventsWhereAppropriate
- CA1030
helpviewer_keywords:
- CA1030
- UseEventsWhereAppropriate
ms.assetid: ea051367-deeb-40f9-9b65-eb818f1e133a
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b1b4989b5b8ca47bc41328c75610cf984926aae2
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49870133"
---
# <a name="ca1030-use-events-where-appropriate"></a>CA1030: Utilizzare eventi dove appropriato
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|UseEventsWhereAppropriate|
|CheckId|CA1030|
|Category|Microsoft.Design|
|Modifica importante|Non sostanziale|

## <a name="cause"></a>Causa
 Nome di un metodo pubblico, protetto o privato inizia con uno dei seguenti:

-   Componente aggiuntivo

-   RemoveOn

-   Incendi

-   Raise

## <a name="rule-description"></a>Descrizione della regola
 Questa regola rileva i metodi che presentano nomi comunemente utilizzati per gli eventi. Gli eventi di seguono lo schema progettuale osservatore o Publish-Subscribe; vengono utilizzati quando una modifica dello stato in un oggetto deve essere comunicata ad altri oggetti. Se un metodo viene chiamato in risposta a una modifica dello stato chiaramente definita, il metodo deve essere richiamato da un gestore eventi. Gli oggetti che chiamano il metodo devono generare eventi anziché chiamare direttamente il metodo.

 Alcuni esempi comuni di eventi si trovano in applicazioni con interfaccia utente in cui un'azione dell'utente, ad esempio facendo clic su un pulsante fa sì che un segmento di codice da eseguire. Il [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] modello di eventi non è limitato alle interfacce utente, deve essere usata ovunque è necessario comunicare lo stato passa a uno o più oggetti.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Se il metodo viene chiamato quando cambia lo stato di un oggetto, è consigliabile modificare la progettazione per utilizzare il [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] modello di eventi.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Eliminare un avviso da questa regola se il metodo non funziona con il [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] modello di eventi.



