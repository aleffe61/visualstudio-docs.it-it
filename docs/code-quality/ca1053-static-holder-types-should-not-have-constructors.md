---
title: 'CA1053: I tipi statici non devono avere costruttori'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- StaticHolderTypesShouldNotHaveConstructors
- CA1053
helpviewer_keywords:
- CA1053
- StaticHolderTypesShouldNotHaveConstructors
ms.assetid: 10302b9a-fa5e-4935-a06a-513d9600f613
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 998d941d0dd0ec06ff7d0f8a727ad3bf50718065
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53928519"
---
# <a name="ca1053-static-holder-types-should-not-have-constructors"></a>CA1053: I tipi statici non devono avere costruttori

|||
|-|-|
|TypeName|StaticHolderTypesShouldNotHaveConstructors|
|CheckId|CA1053|
|Category|Microsoft.Design|
|Modifica importante|Interruzione|

## <a name="cause"></a>Causa
 Un tipo pubblico o annidato dichiara solo membri statici e presenta un costruttore predefinito pubblico o protetto.

## <a name="rule-description"></a>Descrizione della regola
 Il costruttore non è necessario perché la chiamata a membri statici non richiede un'istanza del tipo. Inoltre, perché il tipo non dispone di membri non statici, creare un'istanza non fornisce l'accesso a uno dei membri del tipo.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questa regola, rimuovere il costruttore predefinito o renderla privata.

> [!NOTE]
>  Se il tipo non definisce alcun costruttore, alcuni compilatori di creano automaticamente un costruttore predefinito pubblico. Se questo è il caso con il tipo, aggiungere un costruttore privato predefinito per eliminare la violazione.

## <a name="when-to-suppress-warnings"></a>Soppressione degli avvisi
 Non escludere un avviso da questa regola. La presenza del costruttore suggerisce che il tipo non è un tipo statico.

## <a name="example"></a>Esempio
 Nell'esempio seguente viene illustrato un tipo che viola la regola. Si noti che nel codice sorgente non sia presente alcun costruttore predefinito. Quando questo codice viene compilato in un assembly, il compilatore C# inserirà un costruttore predefinito, che verrà violano questa regola. Per risolvere il problema, dichiarare un costruttore privato.

 [!code-csharp[FxCop.Design.StaticTypes#1](../code-quality/codesnippet/CSharp/ca1053-static-holder-types-should-not-have-constructors_1.cs)]