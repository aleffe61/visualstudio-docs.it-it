---
title: 'Idebugdocumenthost:: Oncreatedocumentcontext | Microsoft Docs'
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHost.OnCreateDocumentContext
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugDocumentHost::OnCreateDocumentContext
ms.assetid: 080c8604-cfd7-484e-a337-15040870e683
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c0f8ce73e05fa8dd163564184361254fd58163ee
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096336"
---
# <a name="idebugdocumenthostoncreatedocumentcontext"></a>IDebugDocumentHost::OnCreateDocumentContext
Notifica all'host che un nuovo contesto del documento viene creato e consente all'host facoltativamente restituire un controllo sconosciuto per il nuovo contesto.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp
HRESULT OnCreateDocumentContext(  
   IUnknown**  ppunkOuter  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `ppunkOuter`  
 [out] Un oggetto che controlla il nuovo contesto.  
  
## <a name="return-value"></a>Valore restituito  
 Il metodo restituisce un tipo `HRESULT`. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.  
  
|Value|Descrizione|  
|-----------|-----------------|  
|`S_OK`|Il metodo è riuscito.|  
|`E_NOTIMPL`|L'host non fornisce un oggetto di controllo.|  
  
## <a name="remarks"></a>Note  
 Questo metodo consente all'host aggiungere nuove funzionalità per i contesti di documento fornito dall'helper. Questo metodo può restituire **E_NOTIMPL** o un oggetto esterno null, nel qual caso il chiamante è responsabile della creazione del contesto.  
  
## <a name="see-also"></a>Vedere anche  
 [Interfaccia IDebugDocumentHost](../../winscript/reference/idebugdocumenthost-interface.md)