---
title: 'CA1012: I tipi astratti non devono avere costruttori'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- AbstractTypesShouldNotHaveConstructors
- CA1012
helpviewer_keywords:
- CA1012
ms.assetid: 09f458ac-dd88-4cd7-a47f-4106c1e80ece
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 81a9fe50b4141b10e3946e3494ff325d1cc302b5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53825097"
---
# <a name="ca1012-abstract-types-should-not-have-constructors"></a>CA1012: I tipi astratti non devono avere costruttori

|||
|-|-|
|TypeName|AbstractTypesShouldNotHaveConstructors|
|CheckId|CA1012|
|Category|Microsoft.Design|
|Modifica importante|Non sostanziale|

## <a name="cause"></a>Causa
 Un tipo pubblico è astratto e ha un costruttore pubblico.

## <a name="rule-description"></a>Descrizione della regola
 I costruttori sui tipi astratti possono essere chiamati solo da tipi derivati. Poiché i costruttori pubblici creano istanze di un tipo e non è possibile creare istanze di un tipo astratto, per una buona progettazione non bisognerebbe creare un tipo astratto con costruttore pubblico.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questa regola, rendere il costruttore protetto o non si dichiara il tipo come astratto.

## <a name="when-to-suppress-warnings"></a>Soppressione degli avvisi
 Non escludere un avviso da questa regola. Tipo astratto è un costruttore pubblico.

## <a name="example"></a>Esempio
 L'esempio seguente contiene un tipo astratto che violano questa regola.

 [!code-vb[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_1.vb)]
 [!code-csharp[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_1.cs)]

## <a name="example"></a>Esempio
 Nell'esempio seguente consente di correggere la violazione precedente modificando l'accessibilità del costruttore da `public` a `protected`.

 [!code-csharp[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_2.cs)]
 [!code-vb[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_2.vb)]