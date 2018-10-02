---
title: 'CA1064: Le eccezioni devono essere pubbliche | Microsoft Docs'
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
- CA1064
- ExceptionsShouldBePublic
helpviewer_keywords:
- ExceptionsShouldBePublic
- CA1064
ms.assetid: 83eb224c-2456-4368-acf4-3b3378e67759
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c35906c41a4c39557b2f72c83308b25cf650f676
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2018
ms.locfileid: "47589950"
---
# <a name="ca1064-exceptions-should-be-public"></a>CA1064: Le eccezioni devono essere pubbliche
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [CA1064: le eccezioni devono essere pubbliche](https://docs.microsoft.com/visualstudio/code-quality/ca1064-exceptions-should-be-public).

|||
|-|-|
|TypeName|ExceptionsShouldBePublic|
|CheckId|CA1064|
|Category|Microsoft.Design|
|Modifica importante|Non importante|

## <a name="cause"></a>Causa
 Un'eccezione non pubblica deriva direttamente dalla <xref:System.Exception>, <xref:System.SystemException>, o <xref:System.ApplicationException>.

## <a name="rule-description"></a>Descrizione della regola
 È visibile nel relativo ambito interno solo un'eccezione interna. Se l'eccezione si verifica al di fuori dell'ambito interno, può essere rilevata solo tramite l'eccezione di base. Se l'eccezione interna è ereditata da <xref:System.Exception>, <xref:System.SystemException>, o <xref:System.ApplicationException>, il codice esterno non avrà informazioni sufficienti per sapere cosa fare con l'eccezione.

 Ma, se il codice è un'eccezione pubblica in un secondo momento viene utilizzata come base per un'eccezione interna, è ragionevole supporre che il codice ulteriormente out sarà in grado di eseguire un'operazione intelligente con l'eccezione di base. L'eccezione pubblico avranno più informazioni rispetto a quanto offerto dai T:System.Exception, T:System.SystemException o T:System.ApplicationException.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Rendere pubblico l'eccezione o l'eccezione interna da un'eccezione di tipo pubblica che non derivano <xref:System.Exception>, <xref:System.SystemException>, o <xref:System.ApplicationException>.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Eliminare un messaggio da questa regola se si è certi in tutti i casi l'eccezione privato verrà rilevata nel relativo ambito interno.

## <a name="example"></a>Esempio
 Questa regola viene attivata nel primo metodo di esempio, FirstCustomException perché la classe di eccezione deriva direttamente da eccezioni ed è interna. La regola non viene generato nella classe SecondCustomException perché anche se la classe deriva anche direttamente dall'eccezione, la classe è dichiarata pubblica. La terza classe inoltre non venga attivato la regola perché non deriva direttamente dalla <xref:System.Exception?displayProperty=fullName>, <xref:System.SystemException?displayProperty=fullName>, o <xref:System.ApplicationException?displayProperty=fullName>.

 [!code-csharp[FxCop.Design.ExceptionsShouldBePublic.CA1064#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.design.exceptionsshouldbepublic.ca1064/cs/ca1064 - exceptionsshouldbepublic.cs#1)]


