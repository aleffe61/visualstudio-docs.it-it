---
title: 'DA0010: Funzione GetHashCode dispendiosa | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DAExpensiveGetHashCode
- vs.performance.DA0010
- vs.performance.rules.DA0010
- vs.performance.10
ms.assetid: 3987e21a-5b4f-45e4-8a33-6b3f0a472c08
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c4bb60104fa865cffa3e06ac088b92081e444457
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49877231"
---
# <a name="da0010-expensive-gethashcode"></a>DA0010: Funzione GetHashCode dispendiosa

|||  
|-|-|  
|ID regola|DA0010|  
|Category|Uso di .NET Framework|  
|Metodi di profilatura|Campionamento<br /><br /> Memoria .NET|  
|Messaggio|Le funzioni GetHashCode dovrebbero essere semplici e non allocare memoria. Se possibile, ridurre la complessità della funzione di codice hash.|  
|Tipo messaggio|Avviso|  

## <a name="cause"></a>Causa  
 Le chiamate al metodo GetHashCode del tipo rappresentano una percentuale significativa dei dati di profilatura o il metodo alloca memoria.  

## <a name="rule-description"></a>Descrizione della regola  
 Hash è una tecnica per individuare rapidamente un particolare elemento in una raccolta di grandi dimensioni. Poiché possono avere dimensioni grandi e devono supportare frequenze di accesso molto elevate, le tabelle hash devono essere efficienti. Per questa ragione, i metodi GetHashCode in .NET Framework non devono allocare memoria. L'allocazione di memoria aumenta il carico del Garbage Collector ed espone il metodo a possibili ritardi se diventa necessario eseguire l'operazione di Garbage Collection in seguito alla richiesta di allocazione.  

## <a name="how-to-fix-violations"></a>Come correggere le violazioni  
 Ridurre la complessità del metodo.