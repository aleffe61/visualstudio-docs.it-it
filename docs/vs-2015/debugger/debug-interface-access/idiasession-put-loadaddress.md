---
title: Put_loadaddress | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::put_loadAddress method
ms.assetid: b157b245-1ea0-4b80-8962-d8b278dbc742
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: daf1e7748a95ae0ad2d7fce3592e0a6948077f45
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51762009"
---
# <a name="idiasessionputloadaddress"></a>IDiaSession::put_loadAddress
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Imposta l'indirizzo di caricamento del file eseguibile che corrisponde ai simboli in questo archivio dei simboli.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT put_loadAddress (   
   ULONGLONG NewVal  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `NewVal`  
 [in] Carica l'indirizzo del file eseguibile.  
  
## <a name="remarks"></a>Note  
 Proprietà dei simboli indirizzo virtuale (valutazione della vulnerabilità) vengono calcolate utilizzando il valore di questo metodo. Gli indirizzi virtuali non vengono calcolati solo se questa proprietà è impostata su diverso da zero.  
  
> [!NOTE]
>  È necessario chiamare questo metodo quando si riceve la [IDiaSession](../../debugger/debug-interface-access/idiasession.md) dell'oggetto e prima di iniziare a utilizzare l'oggetto se è necessario usare qualsiasi proprietà virtuali sui simboli.  
  
## <a name="see-also"></a>Vedere anche  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)



