---
title: IDebugPortSupplier2::CanAddPort | Microsoft Docs
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
- IDebugPortSupplier2::CanAddPort
helpviewer_keywords:
- IDebugPortSupplier2::CanAddPort
ms.assetid: 41f69e0a-e82c-473d-8b7a-0c40fc5730fc
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e29478d71b60376bbd396650935e6257d11a7d37
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51769731"
---
# <a name="idebugportsupplier2canaddport"></a>IDebugPortSupplier2::CanAddPort
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Verifica che un fornitore di porte può aggiungere nuove porte.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT CanAddPort(   
   void   
);  
```  
  
```csharp  
int CanAddPort();  
```  
  
## <a name="return-value"></a>Valore restituito  
 Se è possibile aggiungere la porta, restituisce `S_OK`; in caso contrario, restituisce `S_FALSE` per indicare Nessuna porta può essere aggiunto a questo fornitore della porta.  
  
## <a name="remarks"></a>Note  
 Chiamare questo metodo prima di chiamare il [Aggiungi porta](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md) metodo poiché quest'ultimo metodo consente di creare la porta, nonché aggiunta, che può essere un'operazione impegnativa.  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)

