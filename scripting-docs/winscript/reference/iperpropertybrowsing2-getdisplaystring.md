---
title: IPerPropertyBrowsing2::GetDisplayString | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IPerPropertyBrowsing2.GetDisplayString
apilocation:
- scrobj.dll
helpviewer_keywords:
- IPerPropertyBrowsing2::GetDisplayString
ms.assetid: 8f75c6a9-86a9-4e2d-8cb4-74e7b1c0a524
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e4947ebdeac26ae759fb739dd417607dea885ee5
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2019
ms.locfileid: "54091573"
---
# <a name="iperpropertybrowsing2getdisplaystring"></a>IPerPropertyBrowsing2::GetDisplayString
Ottiene una stringa da visualizzare i tipi che non sono intrinsecamente visualizzabili il testo restituito è un nome che descrive la proprietà e può essere visualizzata nell'interfaccia utente del chiamante.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp
HRESULT GetDisplayString(  
   DISPID  dispid,  
   BSTR*  pBstr  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `dispid`  
 [in] ID dispatch della proprietà il cui nome visualizzato è richiesta.  
  
 `pBstr`  
 [out] Puntatore per il `BSTR` contenente il nome visualizzato per la proprietà identificata da `dispID`.  
  
## <a name="return-value"></a>Valore restituito  
 Restituisce un valore valido `HRESULT`, in genere `S_OK`.  
  
## <a name="remarks"></a>Note  
 La stringa restituita non è un valore consentito della proprietà. È semplicemente una visualizzazione di stringa della proprietà.  
  
## <a name="see-also"></a>Vedere anche  
 [Interfaccia 1 IPerPropertyBrowsing2](../../winscript/reference/iperpropertybrowsing2-interface-1.md)