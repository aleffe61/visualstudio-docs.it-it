---
title: IDebugArrayField::GetRank | Microsoft Docs
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
- IDebugArrayField::GetRank
helpviewer_keywords:
- IDebugArrayField::GetRank method
ms.assetid: 2364b876-5be1-4bab-9b8f-3b6121da35c6
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2ff33ddc6ba41eb43f63ecfb92ad440f205f253a
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51797730"
---
# <a name="idebugarrayfieldgetrank"></a>IDebugArrayField::GetRank
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ottiene il numero di dimensioni o il numero di dimensioni della matrice.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT GetRank(   
   DWORD* pdwRank  
);  
```  
  
```csharp  
int GetRank(  
   out uint pdwRank  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pdwRank`  
 [out] Restituisce il rango.  
  
## <a name="return-value"></a>Valore restituito  
 Se l'operazione riesce, restituisce S_OK; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 Il rango della matrice corrisponde al numero di dimensioni. In C++ e c#, le matrici multidimensionali sono in realtà le matrici di matrici e pertanto può essere considerate solo una matrice unidimensionale (e `GetRank` metodo restituirà sempre 1). Nelle [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)], d'altra parte, le matrici multidimensionali sono gestite in modo diverso e il numero di dimensioni di una matrice di questo tipo riflette il numero di dimensioni (e `GetRank` metodo restituisce sempre il numero di dimensioni).  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugArrayField](../../../extensibility/debugger/reference/idebugarrayfield.md)

