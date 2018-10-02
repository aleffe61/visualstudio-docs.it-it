---
title: ': Ca1306 specificare le impostazioni locali per i tipi di dati | Microsoft Docs'
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
- CA1306
- SetLocaleForDataTypes
helpviewer_keywords:
- CA1306
- SetLocaleForDataTypes
ms.assetid: 104297b2-5806-4de0-a8d9-c589380a796c
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 6e0ef53aa81d4e58463b4dd16e146fcbf65f47fe
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2018
ms.locfileid: "47589611"
---
# <a name="ca1306-set-locale-for-data-types"></a>CA1306: Specificare le impostazioni locali per i tipi di dati
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [CA1306: specificare le impostazioni locali per i tipi di dati](https://docs.microsoft.com/visualstudio/code-quality/ca1306-set-locale-for-data-types).

|||
|-|-|
|TypeName|SetLocaleForDataTypes|
|CheckId|CA1306|
|Category|Microsoft.Globalization|
|Modifica importante|Non sostanziale|

## <a name="cause"></a>Causa
 Un metodo o costruttore ha creato uno o più <xref:System.Data.DataTable?displayProperty=fullName> oppure <xref:System.Data.DataSet?displayProperty=fullName> istanze e non imposta in modo esplicito le proprietà delle impostazioni locali (<xref:System.Data.DataTable.Locale%2A?displayProperty=fullName> o <xref:System.Data.DataSet.Locale%2A?displayProperty=fullName>).

## <a name="rule-description"></a>Descrizione della regola
 Le impostazioni locali determinano elementi di presentazione specifiche delle impostazioni cultura per i dati, ad esempio la formattazione usata per i valori numerici, simboli di valuta e criterio di ordinamento. Quando si crea una <xref:System.Data.DataTable> o <xref:System.Data.DataSet>, è necessario impostare in modo esplicito le impostazioni locali. Per impostazione predefinita, le impostazioni locali per questi tipi sono le impostazioni cultura correnti. Per i dati vengono archiviati in un database o file e vengono condivise globalmente, in genere il locale deve essere impostato per la lingua inglese (<xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>). Quando i dati vengono condivisi tra le impostazioni cultura, usando le impostazioni locali predefinite può causare il contenuto del <xref:System.Data.DataTable> o <xref:System.Data.DataSet> la presentazione o interpretati erroneamente.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questa regola, impostare in modo esplicito le impostazioni locali per il <xref:System.Data.DataTable> o <xref:System.Data.DataSet>.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 È possibile eliminare un avviso da questa regola quando la libreria o l'applicazione è per un numero limitato di utenti locale, i dati non sono condivisa o l'impostazione predefinita restituisce il comportamento desiderato in tutti gli scenari supportati.

## <a name="example"></a>Esempio
 L'esempio seguente crea due <xref:System.Data.DataTable> istanze.

 [!code-csharp[FxCop.Globalization.DataTable#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.DataTable/cs/FxCop.Globalization.DataTable.cs#1)]

## <a name="see-also"></a>Vedere anche
 <xref:System.Data.DataTable?displayProperty=fullName> <xref:System.Data.DataSet?displayProperty=fullName>
 <xref:System.Globalization.CultureInfo?displayProperty=fullName>
 <xref:System.Globalization.CultureInfo.CurrentUICulture%2A?displayProperty=fullName>
 <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>


