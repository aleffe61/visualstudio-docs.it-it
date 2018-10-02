---
title: IDebugDisassemblyStream2::GetScope | Microsoft Docs
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
- IDebugDisassemblyStream2::GetScope
helpviewer_keywords:
- IDebugDisassemblyStream2::GetScope
ms.assetid: 71c6e632-642a-42d8-a995-77e4ac190a5b
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e201bcc4e6de8b39ce8e72c7648045eeb7b9ec72
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47517344"
---
# <a name="idebugdisassemblystream2getscope"></a>IDebugDisassemblyStream2::GetScope
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [IDebugDisassemblyStream2::GetScope](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugdisassemblystream2-getscope).  
  
Ottiene l'ambito del flusso di disassemblaggio.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT GetScope(   
   DISASSEMBLY_STREAM_SCOPE* pdwScope  
);  
```  
  
```csharp  
int GetScope(   
   out enum_ DISASSEMBLY_STREAM_SCOPE pdwScope  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pdwScope`  
 [out] Restituisce un valore di [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md) enumerazione che descrive l'ambito di questo flusso disassembly.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 L'ambito del disassembly potrebbe essere una funzione o l'intero modulo, ad esempio.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)   
 [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md)
