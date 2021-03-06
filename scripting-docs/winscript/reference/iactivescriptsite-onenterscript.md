---
title: IActiveScriptSite::OnEnterScript | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.OnEnterScript
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_OnEnterScript
ms.assetid: 1ed9178c-fe80-41c4-b74d-23b85f9cddbf
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ccef1b2bf63c4421843d3a33cab2e4f471a48251
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094068"
---
# <a name="iactivescriptsiteonenterscript"></a>IActiveScriptSite::OnEnterScript
Comunica all'host che il motore di scripting è iniziata l'esecuzione del codice di script.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp
HRESULT OnEnterScript(void);  
```  
  
## <a name="return-value"></a>Valore restituito  
 Se l'esito è positivo, restituisce `S_OK`.  
  
## <a name="remarks"></a>Note  
 Il motore di scripting deve chiamare questo metodo per ogni singola voce o reingresso nel motore di scripting. Ad esempio, se lo script chiama un oggetto che genera un evento come gestito dal motore di script, il motore di scripting deve chiamare `IActiveScriptSite::OnEnterScript` prima di eseguire l'evento e deve chiamare il [IActiveScriptSite::OnLeaveScript](../../winscript/reference/iactivescriptsite-onleavescript.md) metodo dopo l'esecuzione dell'evento, ma prima di restituire l'oggetto che ha generato l'evento. Chiamate a questo metodo possono essere annidate. Ogni chiamata a questo metodo richiede una chiamata corrispondente al `IActiveScriptSite::OnLeaveScript`.  
  
## <a name="see-also"></a>Vedere anche  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)