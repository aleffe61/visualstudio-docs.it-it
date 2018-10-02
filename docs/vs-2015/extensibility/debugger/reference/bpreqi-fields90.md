---
title: BPREQI_FIELDS90 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- BPREQI_FIELDS90 enumeration
ms.assetid: bf6f7efc-39f2-46a2-906d-c3647bf89995
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5ddba39cc7a540c1c88997c09fd864dd8c22464f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47540821"
---
# <a name="bpreqifields90"></a>BPREQI_FIELDS90
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [BPREQI_FIELDS90](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/bpreqi-fields90).  
  
Enumera i valori validi che specificano le informazioni da recuperare su una richiesta di punto di interruzione. Questa enumerazione estende la [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md) enumerazione.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
enum enum_BPREQI_FIELDS90  
{  
   // VS 8.0 values  
   BPREQI90_BPLOCATION                = 0x0001,  
   BPREQI90_LANGUAGE                  = 0x0002,  
   BPREQI90_PROGRAM                   = 0x0004,  
   BPREQI90_PROGRAMNAME               = 0x0008,  
   BPREQI90_THREAD                    = 0x0010,  
   BPREQI90_THREADNAME                = 0x0020,  
   BPREQI90_PASSCOUNT                 = 0x0040,  
   BPREQI90_CONDITION                 = 0x0080,  
   BPREQI90_FLAGS                     = 0x0100,  
   BPREQI90_ALLOLDFIELDS              = 0x01ff,  
   BPREQI90_VENDOR                    = 0x0200,  
   BPREQI90_CONSTRAINT                = 0x0400,  
   BPREQI90_TRACEPOINT                = 0x0800,  
  
   // Values added in VS 9.0  
   BPREQI90_MACROTRACEPOINT           = 0x1000,  
  
   BPREQI90_ALLFIELDS                 = 0xffff  
};  
typedef DWORD BPREQI_FIELDS90;  
```  
  
```csharp  
public enum enum_BPREQI_FIELDS90  
{  
    // VS 8.0 values  
    BPREQI90_BPLOCATION                = 0x0001,  
    BPREQI90_LANGUAGE                  = 0x0002,  
    BPREQI90_PROGRAM                   = 0x0004,  
    BPREQI90_PROGRAMNAME               = 0x0008,  
    BPREQI90_THREAD                    = 0x0010,  
    BPREQI90_THREADNAME                = 0x0020,  
    BPREQI90_PASSCOUNT                 = 0x0040,  
    BPREQI90_CONDITION                 = 0x0080,  
    BPREQI90_FLAGS                     = 0x0100,  
    BPREQI90_ALLOLDFIELDS              = 0x01ff,  
    BPREQI90_VENDOR                    = 0x0200,  
    BPREQI90_CONSTRAINT                = 0x0400,  
    BPREQI90_TRACEPOINT                = 0x0800,  
  
    // Values added in VS 9.0  
    BPREQI90_MACROTRACEPOINT           = 0x1000,  
  
    BPREQI90_ALLFIELDS                 = 0xffff  
};  
```  
  
#### <a name="parameters"></a>Parametri  
 BPREQI90_BPLOCATION  
 Inizializzare o usare il `bpLocation` campo (posizione punto di interruzione) del [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) oppure [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) struttura.  
  
 BPREQI90_LANGUAGE  
 Inizializzare o usare il `guidLanguage` campo le `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_PROGRAM  
 Inizializzare o usare il `pProgram` campo le `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_PROGRAMNAME  
 Inizializzare o usare il `bstrProgramName` campo le `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_THREAD  
 Inizializzare o usare il `pThread` campo le `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_THREADNAME  
 Inizializzare o usare il `bstrThreadName` campo le `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_PASSCOUNT  
 Inizializzare o usare il `bpPassCount` campo le `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_CONDITION  
 Inizializzare o usare il `bpCondition` campo (condizione di punto di interruzione) del `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_FLAGS  
 Inizializzare o usare il `dwFlags` campo le `BP_REQUEST_INFO` o `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_ALLOLDFIELDS  
 Inizializzare o usare tutti i campi per la del `BP_REQUEST_INFO` struttura.  
  
 BPREQI90_VENDOR  
 Inizializzare o usare il `guidVendor` campo `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_CONSTRAINT  
 Inizializzare o usare il `bstrConstraint` campo `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_TRACEPOINT  
 Inizializzare o usare il `bstrTracepoint` campo `BP_REQUEST_INFO2` struttura.  
  
 BPREQI90_MACROTRACEPOINT  
 Inizializzare o usare il `bstrMacroTracepoint` campo `BP_REQUEST_INFO2` struttura. BPREQI_ALLFIELDS non include questo campo.  
  
 BPREQI90_ALLFIELDS  
 Specifica tutti i campi per il `BP_REQUEST_INFO2` struttura.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: Msdbg90.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vedere anche  
 [Enumerazioni](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
