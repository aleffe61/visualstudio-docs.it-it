---
title: 'CA1001: I tipi proprietari di campi disposable devono essere disposable | Microsoft Docs'
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
- CA1001
- TypesThatOwnDisposableFieldsShouldBeDisposable
helpviewer_keywords:
- CA1001
- TypesThatOwnDisposableFieldsShouldBeDisposable
ms.assetid: c85c126c-2b16-4505-940a-b5ddf873fb22
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: bf86ab422851e27eafbb165968d4005cba7ecf5d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47528075"
---
# <a name="ca1001-types-that-own-disposable-fields-should-be-disposable"></a>CA1001: I tipi proprietari di campi Disposable devono essere Disposable
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||  
|-|-|  
|TypeName|TypesThatOwnDisposableFieldsShouldBeDisposable|  
|CheckId|CA1001|  
|Category|Microsoft.Design|  
|Modifica importante|Non sostanziale - Se il tipo non è visibile all'esterno dell'assembly.<br /><br /> Rilievo - se il tipo è visibile all'esterno dell'assembly.|  
  
## <a name="cause"></a>Causa  
 Una classe dichiara e implementa un campo di istanza che è un <xref:System.IDisposable?displayProperty=fullName> tipo e la classe non implementa <xref:System.IDisposable>.  
  
## <a name="rule-description"></a>Descrizione della regola  
 Una classe che implementa il <xref:System.IDisposable> interfaccia per l'eliminazione delle risorse non gestite che possiede. Un campo di istanza che è un <xref:System.IDisposable> tipo indica che il campo proprietario di una risorsa non gestita. Una classe che dichiara un <xref:System.IDisposable> campo indirettamente proprietaria di una risorsa non gestita e deve implementare il <xref:System.IDisposable> interfaccia. Se la classe non è direttamente proprietario delle risorse non gestite, non deve implementare un finalizzatore.  
  
## <a name="how-to-fix-violations"></a>Come correggere le violazioni  
 Per correggere una violazione di questa regola, implementare <xref:System.IDisposable> e dal <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> chiamata al metodo il <xref:System.IDisposable.Dispose%2A> metodo del campo.  
  
## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi  
 Non escludere un avviso da questa regola.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente mostra una classe che viola la regola e una classe che soddisfa la regola implementando <xref:System.IDisposable>. La classe non implementa un finalizzatore in quanto la classe non dispone direttamente delle risorse non gestite.  
  
 [!code-csharp[FxCop.Design.DisposableFields#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.DisposableFields/cs/FxCop.Design.DisposableFields.cs#1)]
 [!code-vb[FxCop.Design.DisposableFields#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.DisposableFields/vb/FxCop.Design.DisposableFields.vb#1)]  
  
## <a name="related-rules"></a>Regole correlate  
 [CA2213: I campi Disposable devono essere eliminati](../code-quality/ca2213-disposable-fields-should-be-disposed.md)  
  
 [CA2216: I tipi Disposable devono dichiarare un finalizzatore](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)  
  
 [CA2215: I metodi Dispose devono chiamare il metodo Dispose della classe base](../code-quality/ca2215-dispose-methods-should-call-base-class-dispose.md)  
  
 [CA1049: I tipi delle risorse native devono essere Disposable](../code-quality/ca1049-types-that-own-native-resources-should-be-disposable.md)
