---
title: '&lt;riepilogo&gt; (JavaScript) | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- summary JavaScript XML tag
- <summary> JavaScript XML tag
ms.assetid: 6540582d-bdb3-42ec-ad2f-c176783e6f9c
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 8ee08ed1e2a5feb1f5a87f7d6337a4b5f1e47a22
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49252408"
---
# <a name="ltsummarygt-javascript"></a>&lt;riepilogo&gt; (JavaScript)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Specifica la descrizione di una funzione o di un metodo.  
  
## <a name="syntax"></a>Sintassi  
  
```  
<summary locid="descriptionID">description  
</summary>  
```  
  
#### <a name="parameters"></a>Parametri  
 `locid`  
 Facoltativo. L'identificatore per le informazioni di localizzazione sulla funzione o al metodo. L'identificatore è un membro ID o corrisponde alla `name` valore in un bundle di messaggio definito dai metadati OpenAjax dell'attributo. Il tipo di identificatore dipende dal formato specificato nella [ \<loc >](../ide/loc-javascript.md) elemento.  
  
 `description`  
 Facoltativo. Descrizione della funzione o del metodo.  
  
## <a name="remarks"></a>Note  
 Gli elementi utilizzati per annotare le funzioni, tra cui [ \<riepilogo >](../ide/summary-javascript.md), [ \<param >](../ide/param-javascript.md), e [ \<restituisce >](../ide/returns-javascript.md), deve essere inserito nel corpo della funzione prima di qualsiasi istruzione.  
  
## <a name="example"></a>Esempio  
 Il codice seguente viene illustrato come utilizzare il `<summary>` elemento.  
  
```javascript  
function areaFunction(radiusParam)  
{  
    /// <summary>Determines the area of a circle when supplied a radius parameter.</summary>  
    /// <param name="radiusParam" type="Number">The radius of the circle.</param>  
    /// <returns type="Number">The area.</returns>  
    var areaVal;  
    areaVal = Math.PI * radiusParam * radiusParam;  
    return areaVal;  
}  
  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Commenti relativi alla documentazione XML](../ide/xml-documentation-comments-javascript.md)



