---
title: IDebugCanStopEvent2::GetDocumentContext | Microsoft Docs
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
- IDebugCanStopEvent2::GetDocumentContext
helpviewer_keywords:
- IDebugCanStopEvent2::GetDocumentContext
ms.assetid: 936a6c4e-30c5-4c7e-9ad5-910cc605a4b5
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 53a19df56a4f685272fc2b188e1d17f5a87d0997
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47526564"
---
# <a name="idebugcanstopevent2getdocumentcontext"></a>IDebugCanStopEvent2::GetDocumentContext
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [IDebugCanStopEvent2::GetDocumentContext](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugcanstopevent2-getdocumentcontext).  
  
Ottiene il contesto del documento che descrive la posizione di questo evento.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT GetDocumentContext (   
   IDebugDocumentContext2** ppDocCxt  
);  
```  
  
```csharp  
int GetDocumentContext (   
   out IDebugDocumentContext2 ppDocCxt  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `ppDocCxt`  
 [out] Restituisce il [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) interfaccia che rappresenta una posizione in un documento di file di origine corrispondente al percorso del codice corrente.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 In genere, il contesto del documento può essere considerato come una posizione in un file di origine.  
  
 Per ottenere il contesto del codice, che è orientato verso le istruzioni di codice, chiamare il [GetCodeContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getcodecontext.md) (metodo).  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugCanStopEvent2](../../../extensibility/debugger/reference/idebugcanstopevent2.md)   
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [GetCodeContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getcodecontext.md)
