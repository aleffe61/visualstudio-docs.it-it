---
title: 'CA1719: I nomi dei parametri non devono corrispondere ai nomi dei membri | Microsoft Docs'
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
- ParameterNamesShouldNotMatchMemberNames
- CA1719
helpviewer_keywords:
- CA1719
- ParameterNamesShouldNotMatchMemberNames
ms.assetid: c6fea690-1659-4ee7-a1c5-125ad6754525
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 74897625a8d8fced4a87a6e5d722d9edf04769b4
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49828220"
---
# <a name="ca1719-parameter-names-should-not-match-member-names"></a>CA1719: I nomi dei parametri non devono corrispondere ai nomi dei membri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ParameterNamesShouldNotMatchMemberNames|
|CheckId|CA1719|
|Category|Microsoft.Naming|
|Modifica importante|Interruzione|

## <a name="cause"></a>Causa
 Il nome di un membro visibile esternamente corrisponde, in un confronto tra maiuscole e minuscole, il nome di uno dei relativi parametri.

## <a name="rule-description"></a>Descrizione della regola
 Un nome di parametro deve comunicare il significato di un parametro e un nome di membro deve comunicare il significato di un membro. Le progettazioni in cui questi nomi coincidono sono rare. Assegnare a un parametro lo stesso nome del relativo membro non è intuitiva e rende più complesso l'utilizzo della libreria.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Selezionare un nome di parametro che non corrispondono al nome di membro.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Per i nuovi sviluppi, nessun noti verificarsi gli scenari in cui è necessario eliminare un avviso da questa regola. Per le librerie, potrebbe essere necessario eliminare un avviso da questa regola.

## <a name="related-rules"></a>Regole correlate
 [CA1709: Gli identificatori devono essere digitati correttamente con distinzione tra maiuscole e minuscole](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)

 [CA1708: Gli identificatori non si devono differenziare solo in base alle maiuscole e minuscole](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

 [CA1707: Gli identificatori non devono contenere caratteri di sottolineatura](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)



