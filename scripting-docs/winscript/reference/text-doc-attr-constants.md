---
title: Costanti TEXT_DOC_ATTR | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- TEXT_DOC_ATTR
apilocation:
- scrobj.dll
helpviewer_keywords:
- TEXT_DOC_ATTR constants
ms.assetid: fd9c53a4-8f73-4c6a-abe5-6b831ecd5b1e
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7e3fd21ba720dfed394e497a9a56a1bb6898dc60
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097253"
---
# <a name="textdocattr-constants"></a>Costanti TEXT_DOC_ATTR
Descrivono gli attributi del documento.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp
typedef DWORD TEXT_DOC_ATTR;  
```  
  
## <a name="constants"></a>Costanti  
  
|Costante|Value|Descrizione|  
|--------------|-----------|-----------------|  
|TEXT_DOC_ATTR_READONLY|0x00000001|Il documento è di sola lettura.|  
|TEXT_DOC_ATTR_TYPE_PRIMARY|0x00000002|Il documento è il file primario di questa struttura documento.|  
|TEXT_DOC_ATTR_TYPE_WORKER|0x00000004|Il documento è un ruolo di lavoro.|  
|TEXT_DOC_ATTR_TYPE_SCRIPT|0x00000008|Il documento è un file di script.|  
  
## <a name="see-also"></a>Vedere anche  
 [Costanti, enumerazioni e strutture del debugger di script ActiveX](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)