---
title: Enumeratore di codice di comando | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- command code enumerator
- source control plug-ins, command code enumeration
ms.assetid: 5d2c360c-59e4-4da8-bcb4-dd07c7441e40
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bcdba2dd1f6629a3e92c3b07d998b27b83f221a3
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51807494"
---
# <a name="command-code-enumerator"></a>Enumeratore di codice di comando
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Questo enumeratore viene utilizzato nelle opzioni per la [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md) e il [SccPopulateList](../extensibility/sccpopulatelist-function.md)per indicare il comando per il quale vengono specificate le opzioni.  
  
## <a name="syntax"></a>Sintassi  
  
```  
enum SCCCOMMAND {  
   SCC_COMMAND_GET,  
   SCC_COMMAND_CHECKOUT,  
   SCC_COMMAND_CHECKIN,  
   SCC_COMMAND_UNCHECKOUT,  
   SCC_COMMAND_ADD,  
   SCC_COMMAND_REMOVE,  
   SCC_COMMAND_DIFF,  
   SCC_COMMAND_HISTORY,  
   SCC_COMMAND_RENAME,  
   SCC_COMMAND_PROPERTIES,  
   SCC_COMMAND_OPTIONS  
};  
```  
  
## <a name="members"></a>Membri  
 SCC_COMMAND_GET  
 Corrisponde alla [SccGet](../extensibility/sccget-function.md).  
  
 SCC_COMMAND_CHECKOUT  
 Corrisponde alla [SccCheckout](../extensibility/scccheckout-function.md).  
  
 SCC_COMMAND_CHECKIN  
 Corrisponde alla [SccCheckin](../extensibility/scccheckin-function.md).  
  
 SCC_COMMAND_UNCHECKOUT  
 Corrisponde alla [SccUncheckout](../extensibility/sccuncheckout-function.md).  
  
 SCC_COMMAND_ADD  
 Corrisponde alla [SccAdd](../extensibility/sccadd-function.md).  
  
 SCC_COMMAND_REMOVE  
 Corrisponde alla [SccRemove](../extensibility/sccremove-function.md).  
  
 SCC_COMMAND_DIFF  
 Corrisponde alla [SccDiff](../extensibility/sccdiff-function.md).  
  
 SCC_COMMAND_HISTORY  
 Corrisponde alla [SccHistory](../extensibility/scchistory-function.md).  
  
 SCC_COMMAND_RENAME  
 Corrisponde alla [SccRename](../extensibility/sccrename-function.md).  
  
 SCC_COMMAND_PROPERTIES  
 Corrisponde alla [SccProperties](../extensibility/sccproperties-function.md).  
  
 SCC_COMMAND_OPTIONS  
 Corrisponde alla [SccSetOption](../extensibility/sccsetoption-function.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Plug-in controllo codice sorgente](../extensibility/source-control-plug-ins.md)   
 [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md)   
 [SccPopulateList](../extensibility/sccpopulatelist-function.md)

