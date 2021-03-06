---
title: LocationType | Microsoft Docs
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
- LocationType enumeration
ms.assetid: d3e1eedc-bfd3-4c91-881b-d69565138d0f
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a41eb64cc1a93f39a50187d54ecf556246f31913
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51752857"
---
# <a name="locationtype"></a>LocationType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Indica il tipo di informazioni di percorso contenute in un simbolo.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
enum LocationType {   
   LocIsNull,  
   LocIsStatic,  
   LocIsTLS,  
   LocIsRegRel,  
   LocIsThisRel,  
   LocIsEnregistered,  
   LocIsBitField,  
   LocIsSlot,  
   LocIsIlRel,  
   LocInMetaData,  
   LocIsConstant,  
   LocTypeMax  
};  
```  
  
## <a name="elements"></a>Elementi  
 `LocIsNull`  
 Informazioni sulla posizione non è disponibile.  
  
 `LocIsStatic`  
 Posizione è statica.  
  
 `LocIsTLS`  
 Si trova nell'archiviazione thread-local.  
  
 `LocIsRegRel`  
 Percorso è relativo al registro.  
  
 `LocIsThisRel`  
 Percorso è `this`-relativo.  
  
 `LocIsEnregistered`  
 Si trova in un registro di sistema.  
  
 `LocIsBitField`  
 Si trova in un campo di bit.  
  
 `LocIsSlot`  
 Trova uno slot di Microsoft Intermediate Language (MSIL).  
  
 `LocIsIlRel`  
 Percorso è relativo al codice MSIL.  
  
 `LocInMetaData`  
 Si trova nei metadati.  
  
 `LocIsConstant`  
 Si trova in un valore costante.  
  
 `LocTypeMax`  
 Il numero di tipi di percorso di questa enumerazione.  
  
## <a name="remarks"></a>Note  
 Le proprietà disponibili per il [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md) interfaccia dipendono dalla posizione del simbolo all'interno del file di immagine. Per altre informazioni, vedere [percorsi di simboli](../../debugger/debug-interface-access/symbol-locations.md).  
  
 I valori di questa enumerazione vengono restituiti da una chiamata per il [Get_locationtype](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md) (metodo).  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: cvconst.h  
  
## <a name="see-also"></a>Vedere anche  
 [Enumerazioni e strutture](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [Get_locationtype](../../debugger/debug-interface-access/idiasymbol-get-locationtype.md)   
 [Percorsi dei simboli](../../debugger/debug-interface-access/symbol-locations.md)



