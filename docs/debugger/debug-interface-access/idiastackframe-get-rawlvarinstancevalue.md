---
title: Get_rawlvarinstancevalue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackFrame::get_rawLVarInstanceValue method
ms.assetid: ce526259-85a6-475b-9274-0b3a21d95db2
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 66056d2f871d142da46cae25b2e9cb589836a580
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53838437"
---
# <a name="idiastackframegetrawlvarinstancevalue"></a>IDiaStackFrame::get_rawLVarInstanceValue
Questo metodo recupera il valore della variabile locale specificata come byte non elaborati.  
  
## <a name="syntax"></a>Sintassi  
  
```C++  
HRESULT get_rawLVarInstanceValue(  
   IDiaLVarInstance* pInstance,  
   DWORD             cbDataMax,  
   DWORD*            pcbData,  
   BYTE*             pbData  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pInstance`  
 [in] Un `IDiaLVarInstance` che rappresenta un'istanza della variabile locale per ottenere il valore di oggetto.  
  
 `cbDataMax`  
 [in] Numero massimo di byte nel buffer a cui punta `pbData`. Può trattarsi di un massimo di 8 byte (`sizeof(ULONGLONG)`).  
  
 `pcbData`  
 [out] Restituisce il numero effettivo di byte memorizzati nel buffer.  
  
 `pbData`  
 [out] Un buffer per l'inserimento dei dati. Non può essere `NULL`.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="see-also"></a>Vedere anche  
 [IDiaStackFrame](../../debugger/debug-interface-access/idiastackframe.md)