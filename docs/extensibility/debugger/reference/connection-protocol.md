---
title: CONNECTION_PROTOCOL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- CONNECTION_PROTOCOL
helpviewer_keywords:
- CONNECTION_PROTOCOL enumeration
ms.assetid: 99df5865-8b36-486d-9f4c-d10ae2bc688a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f619bde5d2f81b37f50a5896c13c655aaf9fd80e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53907865"
---
# <a name="connectionprotocol"></a>CONNECTION_PROTOCOL
Indica il protocollo usato per la comunicazione tra un server di debug e il pacchetto di debug (DE).  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
typedef enum tagCONNECTION_PROTOCOL {  
   CONNECTION_NONE    = 0,  
   CONNECTION_UNKNOWN = 1,  
   CONNECTION_LOCAL   = 2,  
   CONNECTION_PIPE    = 3,  
   CONNECTION_TCPIP   = 4,  
   CONNECTION_HTTP    = 5,  
   CONNECTION_OTHER   = 6  
} CONNECTION_PROTOCOL;  
```  
  
```csharp  
public enum CONNECTION_PROTOCOL {  
   CONNECTION_NONE    = 0,  
   CONNECTION_UNKNOWN = 1,  
   CONNECTION_LOCAL   = 2,  
   CONNECTION_PIPE    = 3,  
   CONNECTION_TCPIP   = 4,  
   CONNECTION_HTTP    = 5,  
   CONNECTION_OTHER   = 6  
};  
```  
  
#### <a name="parameters"></a>Parametri  
 CONNECTION_NONE  
 Non è stata stabilita alcuna connessione a un server.  
  
 CONNECTION_UNKNOWN  
 È stata stabilita una connessione, ma è di tipo sconosciuto.  
  
 CONNECTION_LOCAL  
 Connessione è a un server locale.  
  
 CONNECTION_PIPE  
 Connessione avviene tramite una named pipe.  
  
 CONNECTION_TCPIP  
 Connessione Usa TCP/IP.  
  
 CONNECTION_HTTP  
 Connessione utilizza HTTP (tramite un server Web).  
  
 CONNECTION_OTHER  
 Un altro tipo di connessione è stato stabilito (questo valore non viene attualmente utilizzato).  
  
## <a name="remarks"></a>Note  
 Questi valori vengono restituiti dai [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md) (metodo).  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: msdbg.h  
  
 Spazio dei nomi: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Enumerazioni](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md)