---
title: IDebugDisassemblyStream2::Read | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDisassemblyStream2::Read
helpviewer_keywords:
- IDebugDisassemblyStream2::Read
ms.assetid: 7db5f6bb-73ee-45bc-b187-c1b6aa2dfdd5
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 6ce82bc81ef54cff9dbfb0a6282411e03775ebc9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53892014"
---
# <a name="idebugdisassemblystream2read"></a>IDebugDisassemblyStream2::Read
Legge le istruzioni a partire dalla posizione corrente nel flusso di disassemblaggio.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
HRESULT Read(   
   DWORD                     dwInstructions,  
   DISASSEMBLY_STREAM_FIELDS dwFields,  
   DWORD*                    pdwInstructionsRead,  
   DisassemblyData*          prgDisassembly  
);  
```  
  
```csharp  
int Read(   
   uint                           dwInstructions,  
   enum_DISASSEMBLY_STREAM_FIELDS dwFields,  
   out uint                       pdwInstructionsRead,  
   DisassemblyData[]              prgDisassembly  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `dwInstructions`  
 [in] Il numero di istruzioni da disassemblare. Questo valore è anche la lunghezza massima del `prgDisassembly` matrice.  
  
 `dwFields`  
 [in] Una combinazione di flag dal [DISASSEMBLY_STREAM_FIELDS](../../../extensibility/debugger/reference/disassembly-stream-fields.md) enumerazione che indicano quali campi della `prgDisassembly` sono da compilare.  
  
 `pdwInstructionsRead`  
 [out] Restituisce il numero di istruzioni effettivamente disassemblato.  
  
 `prgDisassembly`  
 [out] Matrice di [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) strutture che viene compilato con il codice disassemblato, una struttura per ogni istruzione disassemblato. La lunghezza di questa matrice è determinata dal `dwInstructions` parametro.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 Il numero massimo di istruzioni che sono disponibili nell'ambito corrente può essere ottenuto chiamando il [GetSize](../../../extensibility/debugger/reference/idebugdisassemblystream2-getsize.md) (metodo).  
  
 La posizione corrente in cui l'istruzione successiva viene letto da può essere modificata chiamando il [Seek](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md) (metodo).  
  
 Il `DSF_OPERANDS_SYMBOLS` flag può essere aggiunti al `DSF_OPERANDS` flag nel `dwFields` parametro per indicare che i nomi dei simboli devono essere utilizzati quando le istruzioni di disassemblaggio.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)   
 [DISASSEMBLY_STREAM_FIELDS](../../../extensibility/debugger/reference/disassembly-stream-fields.md)   
 [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)   
 [GetSize](../../../extensibility/debugger/reference/idebugdisassemblystream2-getsize.md)   
 [Seek](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)