---
title: IDiaSession::findInlineeLinesByLinenum | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: cf32ae7c-a0c8-4800-bc8f-d64fdd15fb06
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 279ccc53176f0e1959ffb3ecd69fcbb39aa59dad
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942608"
---
# <a name="idiasessionfindinlineelinesbylinenum"></a>IDiaSession::findInlineeLinesByLinenum
Recupera un'enumerazione che consente a un client di eseguire l'iterazione attraverso le informazioni sul numeri di riga di tutte le funzioni che vengono impostati come inline, direttamente o indirettamente, il numero di file e righe di origine specificato.  
  
## <a name="syntax"></a>Sintassi  
  
```C++  
HRESULT findInlineeLinesByVA (   
   IDiaSymbol*           compiland,  
   IDiaSourceFile*       file,  
   DWORD                 linenum,  
   DWORD                 column,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `compiland`  
 [in] Un' [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md) oggetto che rappresenta il modulo in cui cercare i numeri di riga. Questo parametro non può essere `NULL`.  
  
 `file`  
 [in] Un' [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md) oggetto che rappresenta il file di origine in cui cercare. Questo parametro non può essere `NULL`.  
  
 `linenum`  
 [in] Specifica un numero di riga in base uno.  
  
> [!NOTE]
>  È possibile usare zero per specificare tutte le righe (usare il [Findlines](../../debugger/debug-interface-access/idiasession-findlines.md) metodo per trovare tutte le righe).  
  
 `column`  
 [in] Specifica il numero di colonna. Usare zero per specificare tutte le colonne. Una colonna è un offset di byte in una riga.  
  
 `ppResult`  
 [out] Restituisce un [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md) oggetto che contiene un elenco di numeri di riga che sono stati recuperati.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="see-also"></a>Vedere anche  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum (enumerazione)](../../debugger/debug-interface-access/symtagenum.md)   
 [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)