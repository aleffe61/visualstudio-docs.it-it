---
title: 'CA2230: Utilizzare params per argomenti variabili | Microsoft Docs'
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
- UseParamsForVariableArguments
- CA2230
helpviewer_keywords:
- CA2230
- UseParamsForVariableArguments
ms.assetid: bf98b733-4855-4110-9f16-eba5a9e79421
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ad0f43ac18c39d1dfdf6464e5cd260b669e1a0da
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49892729"
---
# <a name="ca2230-use-params-for-variable-arguments"></a>CA2230: Utilizzare params per argomenti variabili
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|UseParamsForVariableArguments|
|CheckId|CA2230|
|Category|Microsoft.Usage|
|Modifica importante|Interruzione|

## <a name="cause"></a>Causa
 Un tipo pubblico o protetto contiene un metodo pubblico o protetto che utilizza il `VarArgs` convenzione di chiamata.

## <a name="rule-description"></a>Descrizione della regola
 Il `VarArgs` convenzione di chiamata viene usato con alcune definizioni di metodi che accettano un numero variabile di parametri. Un metodo tramite la `VarArgs` convenzione di chiamata non Common Language Specification (conforme a CLS) e potrebbe non essere accessibile in linguaggi di programmazione.

 In c#, il `VarArgs` convenzione di chiamata viene utilizzato quando l'elenco dei parametri del metodo termina con il `__arglist` (parola chiave). Visual Basic non supporta il `VarArgs` convenzione di chiamata e Visual C++ consente l'utilizzo solo nel codice non gestito che utilizza l'ellisse `...` notation.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione della regola nel linguaggio c#, usare il [params](http://msdn.microsoft.com/library/1690815e-b52b-4967-8380-5780aff08012) parola chiave anziché `__arglist`.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Non escludere un avviso da questa regola.

## <a name="example"></a>Esempio
 L'esempio seguente illustra due metodi, uno che viola la regola e uno che soddisfa la regola.

 [!code-csharp[FxCop.Usage.UseParams#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.UseParams/cs/FxCop.Usage.UseParams.cs#1)]

## <a name="see-also"></a>Vedere anche
 <xref:System.Reflection.CallingConventions?displayProperty=fullName> [Indipendenza del linguaggio e componenti indipendenti dal linguaggio](http://msdn.microsoft.com/library/4f0b77d0-4844-464f-af73-6e06bedeafc6)



