---
title: EncUnavailableReason | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- EncUnavailableReason
helpviewer_keywords:
- EncUnavailableReason enumeration
ms.assetid: c10aa4c0-d7e0-4de1-b8ff-7e050985eb12
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a3c68aa25a009bad385bec87dba47fcb9957133d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53872043"
---
# <a name="encunavailablereason"></a>EncUnavailableReason
`This is for internal use only!` Rappresenta i motivi che **modifica e continuazione** non è disponibile.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
enum tagEncUnavailableReason {  
   ENCUN_NONE,  
   ENCUN_INTEROP,  
   ENCUN_SQLCLR,  
   ENCUN_MINIDUMP,  
   ENCUN_EMBEDDED,  
   ENCUN_ATTACH,  
   ENCUN_WIN64  
};  
typedef enum tagEncUnavailableReason EncUnavailableReason;  
```  
  
```csharp  
public enum EncUnavailableReason {  
   ENCUN_NONE,  
   ENCUN_INTEROP,  
   ENCUN_SQLCLR,  
   ENCUN_MINIDUMP,  
   ENCUN_EMBEDDED,  
   ENCUN_ATTACH,  
   ENCUN_WIN64  
};  
```  
  
#### <a name="parameters"></a>Parametri  
 ENCUN_NONE  
 Nessun motivo specifico per cui modifica e continuazione non è disponibile.  
  
 ENCUN_INTEROP  
 Modifica e continuazione non è disponibile durante una chiamata di interoperabilità.  
  
 ENCUN_SQLCLR  
 Modifica e continuazione non è disponibile durante una chiamata di procedura SQL che usa Common Language Runtime (CLR).  
  
 ENCUN_MINIDUMP  
 Modifica e continuazione non è disponibile durante l'elaborazione di un minidump.  
  
 ENCUN_EMBEDDED  
 Modifica e continuazione non è disponibile durante l'elaborazione del codice incorporato.  
  
 ENCUN_ATTACH  
 Modifica e continuazione non è disponibile perché la sessione è stata collegata a, non viene avviata da, il debugger.  
  
 ENCUN_WIN64  
 Modifica e continuazione non è disponibile durante l'elaborazione di codice Windows a 64 bit.  
  
## <a name="remarks"></a>Note  
 Questa enumerazione è per uso interno solo da [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]. Il [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md) e [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md) metodi come implementato da un fornitore di porte personalizzato devono sempre restituire `E_NOTIMPL`.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.idl  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Enumerazioni](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)   
 [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)