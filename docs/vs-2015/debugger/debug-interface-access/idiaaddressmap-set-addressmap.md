---
title: Set_addressmap | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
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
- IDiaAddressMap::set_addressMap method
ms.assetid: 81e82073-089b-43d5-af39-49d7a4907c7a
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 497f6ec783388c007075eed93e270a0126334605
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47528383"
---
# <a name="idiaaddressmapsetaddressmap"></a>IDiaAddressMap::set_addressMap
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [Set_addressmap](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/idiaaddressmap-set-addressmap).  
  
Fornisce un mapping di indirizzi per supportare le traduzioni di layout di immagine.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT set_addressMap (   
   DWORD                     cbData,  
   struct DiaAddressMapEntry data[],  
   BOOL                      imagetoSymbols  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `cbData`  
 [in] Il numero di elementi nel `data` parametro.  
  
 `data[]`  
 [in] Matrice di [struttura DiaAddressMapEntry](../../debugger/debug-interface-access/diaaddressmapentry.md) strutture che definiscono il mapping per la conversione.  
  
 `imagetoSymbols`  
 [in] `TRUE` se il `data` parametro definisce una mappa dal layout dell'immagine di nuovo il layout originale (come descritto per i simboli di debug). `FALSE` Se `data` è una mappa per il nuovo layout dell'immagine ricavato il layout originale.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 In genere, il DIA recupera indirizzo traduzione mappe dal file di database (con estensione pdb) del programma. Se questi valori non sono presenti, il [Set_imageheaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md) viene chiamato due volte, una volta con i `imagetoSymbols` parametro impostato su `TRUE` e una volta con il `imagetoSymbols` parametro impostato su `FALSE`. Conversioni di mapping di indirizzi non possono essere abilitate usando il [Put_addressmapenabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md) metodo a meno che non vengono fornite entrambe le mappe di traduzione.  
  
## <a name="see-also"></a>Vedere anche  
 [Struttura DiaAddressMapEntry](../../debugger/debug-interface-access/diaaddressmapentry.md)   
 [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [Put_addressmapenabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md)   
 [IDiaAddressMap::set_imageHeaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md)


