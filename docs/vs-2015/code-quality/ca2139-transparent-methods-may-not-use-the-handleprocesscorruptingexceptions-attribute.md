---
title: "CA2139: I metodi Transparent non deve contenere l'attributo HandleProcessCorruptingExceptions | Microsoft Docs"
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
- CA2139
ms.assetid: 45a0328a-add7-40f9-8934-dff59beb02b3
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b7780698296815da73b9862b586bc256a87f7d42
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49827059"
---
# <a name="ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute"></a>CA2139: I metodi Transparent non possono utilizzare l'attributo HandleProcessCorruptingExceptions
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TransparentMethodsMustNotHandleProcessCorruptingExceptions|
|CheckId|CA2139|
|Category|Microsoft.Security|
|Modifica importante|Interruzione|

## <a name="cause"></a>Causa
 Un metodo trasparente è contrassegnato con il <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> attributo.

## <a name="rule-description"></a>Descrizione della regola
 Questa regola viene attivata qualsiasi metodo trasparente che tenti di gestire un'eccezione che danneggia tramite il processo di <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> attributo. Un processo di eccezione che danneggia sia una classificazione di eccezione CLR versione 4.0 di tali eccezioni <xref:System.AccessViolationException>. L'attributo HandleProcessCorruptedStateExceptionsAttribute può essere utilizzato solo dai metodi critici per la sicurezza e sarà ignorato se applicato a un metodo trasparente. Per gestire le eccezioni di danneggiare processo, questo metodo deve diventare SecurityCritical o SecuritySafeCritical.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questa regola, rimuovere il <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> dell'attributo o contrassegnare il metodo con il <xref:System.Security.SecurityCriticalAttribute> o il <xref:System.Security.SecuritySafeCriticalAttribute> attributo.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Non escludere un avviso da questa regola.

## <a name="example"></a>Esempio
 In questo esempio, un metodo trasparente è contrassegnato con il <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> attributo e la regola avrà esito negativo. Il metodo deve essere contrassegnato anche con il <xref:System.Security.SecurityCriticalAttribute> o il <xref:System.Security.SecuritySafeCriticalAttribute> attributo.

 [!code-csharp[FxCop.Security.CA2139.TransparentMethodsMustNotHandleProcessCorruptingExceptions#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2139.transparentmethodsmustnothandleprocesscorruptingexceptions/cs/ca2139 - transparentmethodsmustnothandleprocesscorruptingexceptions.cs#1)]



