---
title: IDiaSession::findAcceleratorInlineesByLinenum | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 386c87aa-f7b2-4d38-9dd6-fffba9ff01f0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b90a253baefad62bba205ccbf0fb8b8fff81712d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49917466"
---
# <a name="idiasessionfindacceleratorinlineesbylinenum"></a>IDiaSession::findAcceleratorInlineesByLinenum
Restituisce un'enumerazione dei simboli per i frame inline che corrispondono al percorso di origine specificato.  
  
## <a name="syntax"></a>Sintassi  
  
```C++  
HRESULT findAcceleratorInlineeLinesByName (   
   IDiaSymbol*           parent,  
   IDiaSourceFile*       file,  
   DWORD                 linenum,  
   DWORD                 colnum,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `parent`  
 [in] Un `IDiaSymbol` che corrisponde alla funzione di stub di tasti di scelta rapida che deve essere eseguita la ricerca.  
  
 `file`  
 [in] Il `IDiaSourceFile` della posizione di origine.  
  
 `linenum`  
 [in] Numero di riga della posizione di origine.  
  
 `colnum`  
 [in] Il numero di colonna della posizione di origine.  
  
 `ppResult`  
 [out] Un puntatore a un `IDiaEnumLineNumbers` puntatore a interfaccia che viene inizializzato con il risultato.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="see-also"></a>Vedere anche  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)