---
title: IDebugProgramPublisher2::PublishProgram | Microsoft Docs
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
- IDebugProgramPublisher2::PublishProgram
helpviewer_keywords:
- IDebugProgramPublisher2::PublishProgram
ms.assetid: 92ff63f0-e869-4040-b3ae-b2c899e708ff
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 53ddd111710eccb14fba2a6d2a4a9a3648c51f4e
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51755210"
---
# <a name="idebugprogrampublisher2publishprogram"></a>IDebugProgramPublisher2::PublishProgram
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Questo metodo rende disponibili per i motori di debug (DEs a) un programma e il gestore di sessione di debug.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp  
HRESULT PublishProgram(  
   CONST_GUID_ARRAY Engines,  
   LPCOLESTR        szFriendlyName,  
   IUnknown*        pDebuggeeInterface  
);  
```  
  
```csharp  
int PublishProgram(  
   CONST_GUID_ARRAY Engines,  
   string           szFriendlyName,  
   object           pDebuggeeInterface  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `Engines`  
 [in] Matrice di GUID per la crittografia DEs che possono avviare o connettersi a questo programma.  
  
 `szFriendlyName`  
 [in] Nome descrittivo per il programma (ciò viene visualizzato nei menu o finestre di dialogo presentate all'utente).  
  
 `pDebuggeeInterface`  
 [in] `IUnknown` interfaccia per il programma (questo valore viene usato come un cookie per identificare in modo univoco il programma; questo stesso valore viene utilizzato per il programma "unpublish")  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="remarks"></a>Note  
 Per rendere non è più disponibile per il debug di un programma, chiamare [UnpublishProgram](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogram.md).  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md)   
 [UnpublishProgram](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogram.md)

