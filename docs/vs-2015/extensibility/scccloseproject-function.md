---
title: Funzione SccCloseProject | Microsoft Docs
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
- SccCloseProject
helpviewer_keywords:
- SccCloseProject function
ms.assetid: 259c2069-d349-4814-810f-1c3151b7fb84
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e4af9d73c19708369bcd4d341b573e421f8bc015
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51807544"
---
# <a name="scccloseproject-function"></a>Funzione SccCloseProject
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Questa funzione consente di chiudere un progetto, contrassegna la fine di una determinata sessione.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
SCCRTN SccCloseProject (  
   LPVOID pvContext  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 pvContext  
 La struttura del contesto plug-in del controllo origine.  
  
## <a name="return-value"></a>Valore restituito  
 Implementazione di plug-in del controllo dell'origine di questa funzione deve restituire uno dei valori seguenti:  
  
|Valore|Descrizione|  
|-----------|-----------------|  
|SCC_OK|Il progetto è stato chiuso.|  
|SCC_E_PROJNOTOPEN|Nessun progetto è aperto.|  
|SCC_E_NOTAUTHORIZED|L'utente non è autorizzato a eseguire questa operazione.|  
|SCC_E_NONSPECIFICERROR|Errore non specifico.|  
  
## <a name="remarks"></a>Note  
 Il [SccOpenProject](../extensibility/sccopenproject-function.md) viene sempre chiamato prima di questa funzione. Una chiamata a questa funzione viene quindi seguita da una chiamata a uno il `SccOpenProject` funzione o il [SccUninitialize](../extensibility/sccuninitialize-function.md), che termina la connessione al sistema di controllo di origine completamente.  
  
## <a name="see-also"></a>Vedere anche  
 [Funzioni API del plug-in controllo di origine](../extensibility/source-control-plug-in-api-functions.md)   
 [SccOpenProject](../extensibility/sccopenproject-function.md)   
 [SccInitialize](../extensibility/sccinitialize-function.md)

