---
title: 'CA2126: Le richieste di collegamento necessarie richieste di ereditarietà'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2126
- TypeLinkDemandsRequireInheritanceDemands
helpviewer_keywords:
- CA2126
- TypeLinkDemandsRequireInheritanceDemands
ms.assetid: 07b604e5-5579-4df9-a578-dadd0d8370a7
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 834f120994070e055fe5ac417d1fb39830c7bcef
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53904140"
---
# <a name="ca2126-type-link-demands-require-inheritance-demands"></a>CA2126: Le richieste di collegamento necessarie richieste di ereditarietà

|||
|-|-|
|TypeName|TypeLinkDemandsRequireInheritanceDemands|
|CheckId|CA2126|
|Category|Microsoft.Security|
|Modifica importante|Interruzione|

## <a name="cause"></a>Causa
 Un tipo non sealed pubblico è protetto con una richiesta di collegamento, dispone di un metodo sottoponibile a override e il tipo né il metodo è protetto con una richiesta di ereditarietà.

## <a name="rule-description"></a>Descrizione della regola
 Una richiesta di collegamento in un metodo o nel relativo tipo dichiarante richiede che il chiamante immediato del metodo di avere l'autorizzazione specificata. Una richiesta di ereditarietà in un metodo richiede un metodo di override per avere l'autorizzazione specificata. Una richiesta di ereditarietà in un tipo richiede una classe di derivazione per avere l'autorizzazione specificata.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questa regola, proteggere il tipo o il metodo con una richiesta di ereditarietà per la stessa autorizzazione della richiesta di collegamento.

## <a name="when-to-suppress-warnings"></a>Soppressione degli avvisi
 Non escludere un avviso da questa regola.

## <a name="example"></a>Esempio
 Nell'esempio seguente viene illustrato un tipo che viola la regola.

 [!code-cpp[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/CPP/ca2126-type-link-demands-require-inheritance-demands_1.cpp)]
 [!code-vb[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/VisualBasic/ca2126-type-link-demands-require-inheritance-demands_1.vb)]
 [!code-csharp[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2126-type-link-demands-require-inheritance-demands_1.cs)]

## <a name="related-rules"></a>Regole correlate
 [CA2108: Controllare la sicurezza dichiarativa sui tipi di valore](../code-quality/ca2108-review-declarative-security-on-value-types.md)

 [CA2112: I tipi protetti non devono esporre campi](../code-quality/ca2112-secured-types-should-not-expose-fields.md)

 [CA2122: Non esporre in modo indiretto metodi con richieste di collegamento](../code-quality/ca2122-do-not-indirectly-expose-methods-with-link-demands.md)

 [CA2123: Le richieste di collegamento di override devono essere identiche a di base](../code-quality/ca2123-override-link-demands-should-be-identical-to-base.md)

## <a name="see-also"></a>Vedere anche

- [Linee guida per la generazione di codice sicuro](/dotnet/standard/security/secure-coding-guidelines)
- [Richieste di collegamento](/dotnet/framework/misc/link-demands)