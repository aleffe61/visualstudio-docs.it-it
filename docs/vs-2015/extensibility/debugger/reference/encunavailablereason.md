---
title: EncUnavailableReason | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- EncUnavailableReason
helpviewer_keywords:
- EncUnavailableReason enumeration
ms.assetid: c10aa4c0-d7e0-4de1-b8ff-7e050985eb12
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 531d6587593db01ac1536b3111633721f4ee84f9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47517488"
---
# <a name="encunavailablereason"></a>EncUnavailableReason
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [EncUnavailableReason](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/encunavailablereason).  
  
`This is for internal use only!` Rappresenta i motivi che **modifica e continuazione** non è disponibile.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
enum tagEncUnavailableReason {  
   ENCUN_NONE,  
   ENCUN_INTEROP,  
   ENCUN_SQLCLR,  
   ENCUN_MINIDUMP,  
   ENCUN_EMBEDDED,  
   ENCUN_ATTACH,  
   ENCUN_WIN64  
};  
typedef enum tagEncUnavailableReason EncUnavailableReason;  
```  
  
```csharp  
public enum EncUnavailableReason {  
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
 Questa enumerazione è per uso interno solo da [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)]. Il [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md) e [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md) metodi come implementato da un fornitore di porte personalizzato devono sempre restituire `E_NOTIMPL`.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.idl  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Enumerazioni](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)   
 [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)
