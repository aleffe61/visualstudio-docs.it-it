---
title: IPerPropertyBrowsing2::GetPredefinedStrings | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IPerPropertyBrowsing2.GetPredefinedStrings
apilocation:
- scrobj.dll
helpviewer_keywords:
- IPerPropertyBrowsing2::GetPredefinedStrings
ms.assetid: d2fa30f7-a566-4dbd-8b47-ffdc00419771
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3bec9643a89d40a7b1e37d019d4211bd7167ee65
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088608"
---
# <a name="iperpropertybrowsing2getpredefinedstrings"></a>IPerPropertyBrowsing2::GetPredefinedStrings
Consente al chiamante da riempire una casella di riepilogo con una matrice calcolata di puntatori a stringhe che rappresentano i valori possibili per questa proprietà.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp
HRESULT GetPredefinedStrings(  
   DISPID  dispid,  
   CALPOLESTR*  pCaStrings,  
   CADWORD*  pCaCookies  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `dispid`  
 [in] ID dispatch della proprietà per il quale il chiamante sta richiedendo l'elenco di stringhe.  
  
 `pCaStrings`  
 [out] Puntatore a una struttura di matrice allocata dal chiamante a conteggio che contiene il numero di elementi e l'indirizzo di una matrice di puntatori di stringa allocata (metodo). Se il metodo ha esito negativo, viene allocata nessuna memoria e il contenuto della struttura è definito.  
  
 `pCaCookies`  
 [out] Puntatore alla struttura di matrice allocata dal chiamante a conteggio che contiene il numero di elementi e l'indirizzo di una matrice di valori DWORD allocate (metodo). Se il metodo ha esito negativo, viene allocata nessuna memoria e il contenuto della struttura è definito.  
  
## <a name="return-value"></a>Valore restituito  
 Restituisce un valore valido `HRESULT`, in genere `S_OK`.  
  
## <a name="see-also"></a>Vedere anche  
 [Interfaccia 1 IPerPropertyBrowsing2](../../winscript/reference/iperpropertybrowsing2-interface-1.md)