---
title: Enumerazione SCRIPTTRACEINFO | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cb8a4767-8c8e-4fa0-a735-038767a8c500
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 866f507b4d107c8f395be6588a85f67ea6bb45c9
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086749"
---
# <a name="scripttraceinfo-enumeration"></a>Enumerazione SCRIPTTRACEINFO
Rappresenta l'evento di script che si sta tracciando. Utilizzato nel [metodo iactivescriptsitetraceinfo:: Sendscripttraceinfo](../../winscript/reference/iactivescriptsitetraceinfo-sendscripttraceinfo-method.md).  
  
## <a name="syntax"></a>Sintassi  
  
```cpp
typedef enum tagSCRIPTTRACEINFO {      SCRIPTTRACEINFO_SCRIPTSTART = 0,      SCRIPTTRACEINFO_SCRIPTEND   = 1,      SCRIPTTRACEINFO_COMCALLSTART    = 2,      SCRIPTTRACEINFO_COMCALLEND  = 3,      SCRIPTTRACEINFO_CREATEOBJSTART  = 4,      SCRIPTTRACEINFO_CREATEOBJEND    = 5,      SCRIPTTRACEINFO_GETOBJSTART = 6,      SCRIPTTRACEINFO_GETOBJEND   = 7,  } SCRIPTTRACEINFO ;  
```  
  
## <a name="enumeration-values"></a>Valori di enumerazione  
  
|||  
|-|-|  
|SCRIPTTRACEINFO_SCRIPTSTART|L'inizio di uno script.|  
|SCRIPTTRACEINFO_SCRIPTEND|Fine dello script.|  
|SCRIPTTRACEINFO_COMCALLSTART|L'inizio di una chiamata COM.|  
|SCRIPTTRACEINFO_COMCALLEND|Fine di una chiamata COM.|  
|SCRIPTTRACEINFO_CREATEOBJSTART|Inizio della creazione dell'oggetto.|  
|SCRIPTTRACEINFO_CREATEOBJEND|Fine della creazione dell'oggetto.|  
|SCRIPTTRACEINFO_GETOBJSTART|L'inizio di una chiamata GetObject.|  
|SCRIPTTRACEINFO_GETOBJEND|Fine di una chiamata GetObject.|