---
title: 'CA1504: Controllare i nomi dei campi fuorvianti | Microsoft Docs'
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
- ReviewMisleadingFieldNames
- CA1504
helpviewer_keywords:
- CA1504
- ReviewMisleadingFieldNames
ms.assetid: 94136ff1-4aaf-4dc2-9170-48c171ab7499
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c927457e2e16f19c221204ba445dad6c127da850
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49878388"
---
# <a name="ca1504-review-misleading-field-names"></a>CA1504: Controllare i nomi dei campi fuorvianti
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ReviewMisleadingFieldNames|
|CheckId|CA1504|
|Category|Microsoft.Maintainability|
|Modifica importante|Non sostanziale|

## <a name="cause"></a>Causa
 Il nome di un campo di istanza inizia con "s _" o il nome di un `static` (`Shared` in [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]) campo inizia con "m _".

## <a name="rule-description"></a>Descrizione della regola
 I nomi dei campi che iniziano con "s _" sono associati i dati statici da molti utenti. Analogamente, i nomi dei campi che iniziano con "m _" sono associati a dati dell'istanza (membro). Per semplificare la gestione del codice, i nomi devono seguire le convenzioni a livello generale.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questa regola, rinominare il campo utilizzando il prefisso appropriato. In alternativa, rendere il campo conforme con il suffisso corrente aggiungendo o rimuovendo il `static` modificatore.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Non escludere un avviso da questa regola.



