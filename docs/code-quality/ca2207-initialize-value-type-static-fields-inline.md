---
title: 'CA2207: Inizializzare i campi statici del tipo di valore inline'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- InitializeValueTypeStaticFieldsInline
- CA2207
helpviewer_keywords:
- CA2207
- InitializeValueTypeStaticFieldsInline
ms.assetid: d1ea9d8b-ecc2-46ca-86e2-c41dd0e76658
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ee4ffd51eef5b8a4f0523dd2356d4e0bdb29b945
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53869159"
---
# <a name="ca2207-initialize-value-type-static-fields-inline"></a>CA2207: Inizializzare i campi statici del tipo di valore inline

|||
|-|-|
|TypeName|InitializeValueTypeStaticFieldsInline|
|CheckId|CA2207|
|Category|Microsoft.Usage|
|Modifica importante|Non importante|

## <a name="cause"></a>Causa
 Un tipo di valore dichiara un costruttore statico esplicito.

## <a name="rule-description"></a>Descrizione della regola
 Quando viene dichiarato un tipo di valore, viene sottoposto a inizializzazione una predefinita in tutti i campi di tipo di valore sono impostati su zero e tutti i campi di tipo riferimento sono impostati su `null` (`Nothing` in Visual Basic). Un costruttore statico esplicito è garantito solo per l'esecuzione prima di un costruttore di istanza o viene chiamato un membro statico del tipo. Pertanto, se il tipo viene creato senza dover chiamare un costruttore di istanza, il costruttore statico non è garantito per l'esecuzione.

 Se tutti i dati statici vengono inizializzati inline e non viene dichiarato alcun costruttore statico esplicito, i compilatori c# e Visual Basic aggiungono il `beforefieldinit` flag per la definizione della classe MSIL. I compilatori di aggiungono anche un costruttore statico privato che contiene il codice di inizializzazione statica. Questo costruttore statico privato ti consente di eseguire prima di tutti i campi statici del tipo sono accessibili.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Per correggere una violazione di questa regola inizializzare tutti i dati statici quando viene dichiarato e rimuovere il costruttore statico.

## <a name="when-to-suppress-warnings"></a>Soppressione degli avvisi
 Non escludere un avviso da questa regola.

## <a name="related-rules"></a>Regole correlate
 [CA1810: Inizializzare i campi statici del tipo di riferimento inline](../code-quality/ca1810-initialize-reference-type-static-fields-inline.md)