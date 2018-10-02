---
title: 'CA1505: Evitare codice non gestibile | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- AvoidUnmaintainableCode
- CA1505
helpviewer_keywords:
- AvoidUnmaintainableCode
- CA1505
ms.assetid: 8292b268-5929-4221-b699-f9c414bcec5d
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ee836af1ee0030c3eea56e12ea5fe767c4b7255b
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2018
ms.locfileid: "47589718"
---
# <a name="ca1505-avoid-unmaintainable-code"></a>CA1505: evitare codice non manutenibile
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [CA1505: evitare codice non gestibile](https://docs.microsoft.com/visualstudio/code-quality/ca1505-avoid-unmaintainable-code).

|||
|-|-|
|TypeName|AvoidUnmantainableCode|
|CheckId|CA1505|
|Category|Microsoft.Maintainability|
|Modifica importante|Non sostanziale|

## <a name="cause"></a>Causa
 Un tipo o metodo presenta un valore di indice di gestibilità basso.

## <a name="rule-description"></a>Descrizione della regola
 L'indice di manutenibilità viene calcolato usando le metriche seguenti: righe di codice, il volume del programma e complessità ciclomatica. Il volume del programma è una misura della difficoltà di comprensione di un tipo o metodo che si basa sul numero di operatori e operandi nel codice. Complessità ciclomatica è una misura della complessità strutturale del tipo o metodo. Altre informazioni sulla metrica del codice in [misurazione della complessità e manutenibilità del codice gestito](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md).

 Un indice di manutenibilità basso indica che un tipo o metodo è probabilmente difficile da gestire e sarebbe un buon candidato per la riprogettazione.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere questa violazione, riprogettare il tipo o metodo e tentare di suddividerlo in più mirati e limitati di tipi o metodi.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Escludere questo avviso quando un tipo o metodo è considerato accettabile nonostante le grandi dimensioni o quando il tipo o metodo non può essere divisa.

## <a name="see-also"></a>Vedere anche
 [Avvisi di manutenibilità](../code-quality/maintainability-warnings.md) [misurazione della complessità e della manutenibilità del codice gestito](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)


