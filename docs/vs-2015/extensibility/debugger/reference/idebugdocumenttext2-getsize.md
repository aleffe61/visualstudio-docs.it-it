---
title: IDebugDocumentText2::GetSize | Microsoft Docs
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
- IDebugDocumentText2::GetSize
helpviewer_keywords:
- IDebugDocumentText2::GetSize
ms.assetid: bf515a8f-dcee-4004-8f81-543d547ceaae
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f7cd8f691b8c94dee8666a85f707674acaa73fa9
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51745346"
---
# <a name="idebugdocumenttext2getsize"></a>IDebugDocumentText2::GetSize
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Recupera la dimensione del testo nella posizione specificata nel documento.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT GetSize(   
   ULONG* pcNumLines,  
   ULONG* pcNumChars  
);  
```  
  
```csharp  
int GetSize(   
   ref uint pcNumLines,  
   ref uint pcNumChars  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pcNumLines`  
 [out] Restituisce il numero di righe di testo.  
  
 `pcNumChars`  
 [out] Restituisce il numero di caratteri del testo.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 [Solo C++] Se non si desidera un valore specifico, passare un valore NULL per il parametro.  
  
 [C# solo] Specificare entrambi i parametri.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugDocumentText2](../../../extensibility/debugger/reference/idebugdocumenttext2.md)

