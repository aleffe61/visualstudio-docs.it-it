---
title: ': CA2133 delegati devono ai metodi con trasparenza consistente | Microsoft Docs'
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
- CA2133
ms.assetid: a09672e2-63cb-4abd-9e8f-dff515e101ce
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 16e766979e71b36f816e1265ef5da520c16d85b4
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49909707"
---
# <a name="ca2133-delegates-must-bind-to-methods-with-consistent-transparency"></a>CA2133: Delegati devono essere associati ai metodi con trasparenza consistente
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DelegatesMustBindWithConsistentTransparency|
|CheckId|CA2133|
|Category|Microsoft.Security|
|Modifica importante|Interruzione|

> [!NOTE]
>  Questo avviso viene applicato solo al codice che esegue CoreCLR (la versione di CLR è specifico per le applicazioni Silverlight Web).

## <a name="cause"></a>Causa
 Questo avviso viene attivato su un metodo che associa un delegato contrassegnato con il <xref:System.Security.SecurityCriticalAttribute> a un metodo trasparente o contrassegnato con il <xref:System.Security.SecuritySafeCriticalAttribute>. L'avviso genera anche un metodo che associa un delegato che è trasparente o critico per la sicurezza a un metodo critico.

## <a name="rule-description"></a>Descrizione della regola
 I tipi delegati e i metodi che vengono associate devono avere trasparenza consistente. I delegati trasparenti e richiamabile da codice trasparente possono associare solo ad altri metodi trasparente o critico. Allo stesso modo, critici delegati possono solo associare ai metodi critici. Queste regole di associazione assicurano che l'unico codice che può richiamare un metodo tramite un delegato può inoltre aver richiamato il metodo di stesso direttamente. Ad esempio, regole di associazione impediscono di chiamata di codice critico direttamente tramite un delegato trasparente codice trasparente.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questo avviso, modificare la trasparenza del delegato o del metodo che associa in modo che la trasparenza dei due sono equivalenti.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Non escludere un avviso da questa regola.

### <a name="code"></a>Codice
 [!code-csharp[FxCop.Security.CA2133.DelegatesMustBindWithConsistentTransparency#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2133.delegatesmustbindwithconsistenttransparency/cs/ca2133 - delegatesmustbindwithconsistenttransparency.cs#1)]



