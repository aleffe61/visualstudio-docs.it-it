---
title: 'CA1801: Rivedere i parametri inutilizzati | Microsoft Docs'
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
- AvoidUnusedParameters
- CA1801
- ReviewUnusedParameters
helpviewer_keywords:
- CA1801
- ReviewUnusedParameters
ms.assetid: 5d73545c-e153-4b7c-a7b2-be6bf5aca5be
caps.latest.revision: 31
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b0946e315aef0c333207d49eb14820d287a9b361
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49269685"
---
# <a name="ca1801-review-unused-parameters"></a>CA1801: Rivedere i parametri inutilizzati
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Per la documentazione più recente di Visual Studio 2017, vedere [CA1801: rivedere i parametri inutilizzati](https://docs.microsoft.com/visualstudio/code-quality/ca1801-review-unused-parameters) su docs.microsoft.com.  
  
|||  
|-|-|  
|TypeName|ReviewUnusedParameters|  
|CheckId|CA1801|  
|Category|Microsoft.Usage|  
|Modifica importante|Non importante: se il membro non è visibile all'esterno dell'assembly, indipendentemente dalle modifiche apportate.<br /><br /> Non importante: se si modifica il membro per usare il parametro nel relativo corpo.<br /><br /> Rilievo - se si rimuove il parametro ed è visibile all'esterno dell'assembly.|  
  
## <a name="cause"></a>Causa  
 Una firma di metodo include un parametro non utilizzato nel corpo del metodo. Questa regola non esamina i metodi seguenti:  
  
-   Metodi di cui viene fatto riferimento da un delegato.  
  
-   Metodi usati come gestori eventi.  
  
-   I metodi dichiarati con la `abstract` (`MustOverride` in Visual Basic) modificatore.  
  
-   I metodi dichiarati con la `virtual` (`Overridable` in Visual Basic) modificatore.  
  
-   I metodi dichiarati con la `override` (`Overrides` in Visual Basic) modificatore.  
  
-   I metodi dichiarati con la `extern` (`Declare` istruzione in Visual Basic) modificatore.  
  
## <a name="rule-description"></a>Descrizione della regola  
 Esaminare i parametri dei metodi non virtuali che non vengono utilizzati nel corpo del metodo per verificare che sia che non presente alcun correttezza riguardo all'errore per accedervi. I parametri inutilizzati comportano costi di manutenzione e prestazioni.  
  
 In alcuni casi una violazione di questa regola può puntare a un bug di implementazione del metodo. Ad esempio, il parametro deve essere utilizzato nel corpo del metodo. Eliminare gli avvisi di questa regola se il parametro deve essere presente per compatibilità con le versioni precedenti.  
  
## <a name="how-to-fix-violations"></a>Come correggere le violazioni  
 Per correggere una violazione di questa regola, rimuovere il parametro non usato (una modifica di rilievo) o usare il parametro nel corpo del metodo (una modifica irrilevante).  
  
## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi  
 È possibile eliminare un avviso da questa regola per il codice fornito in precedenza per il quale la correzione sarebbe una modifica sostanziale.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente illustra due metodi. Un metodo viola la regola e l'altro metodo soddisfa la regola.  
  
 [!code-csharp[FxCop.Usage.ReviewUnusedParameters#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.ReviewUnusedParameters/cs/FxCop.Usage.ReviewUnusedPerameters.cs#1)]  
  
## <a name="related-rules"></a>Regole correlate  
 [CA1811: Evitare il codice privato non chiamato](../code-quality/ca1811-avoid-uncalled-private-code.md)  
  
 [CA1812: Evitare classi interne prive di istanze](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)  
  
 [CA1804: Rimuovere locali non usati](../code-quality/ca1804-remove-unused-locals.md)

