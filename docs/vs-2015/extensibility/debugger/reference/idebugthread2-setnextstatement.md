---
title: IDebugThread2::SetNextStatement | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugThread2::SetNextStatement
helpviewer_keywords:
- IDebugThread2::SetNextStatement
ms.assetid: 9e2834dd-4ecf-45af-8e6c-f9318ebdac06
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5956a57e9bd6db646091a5c0b7a0948d3cdac4bb
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51776239"
---
# <a name="idebugthread2setnextstatement"></a>IDebugThread2::SetNextStatement
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Imposta il puntatore all'istruzione corrente nel contesto del codice di errore specificati.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT SetNextStatement (   
   IDebugStackFrame2*  pStackFrame,  
   IDebugCodeContext2* pCodeContext  
);  
```  
  
```csharp  
int SetNextStatement (   
   IDebugStackFrame2  pStackFrame,  
   IDebugCodeContext2 pCodeContext  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pStackFrame`  
 Riservato per utilizzi futuri; Impostare su un valore null.  
  
 `pCodeContext`  
 [in] Un' [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) che descrive la posizione del codice sta per essere eseguita e il relativo contesto.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore. Nella tabella seguente mostra altri valori possibili.  
  
|Valore|Descrizione|  
|-----------|-----------------|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_NONLEAF_FRAME|L'istruzione successiva non può essere in uno stack frame più approfondito sullo stack frame.|  
|E_CANNOT_SETIP_TO_DIFFERENT_FUNCTION|L'istruzione successiva non è associato a qualsiasi frame nello stack.|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_EXCEPTION|Alcuni motori di debug non è possibile impostare l'istruzione successiva dopo un'eccezione.|  
  
## <a name="remarks"></a>Note  
 Il puntatore all'istruzione indica la successiva istruzione o l'istruzione da eseguire. Questo metodo viene utilizzato per ripetere una riga di codice sorgente o per forzare l'esecuzione di continuare in un'altra funzione, ad esempio.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)

