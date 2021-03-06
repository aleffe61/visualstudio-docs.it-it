---
title: Interfaccia IActiveScriptDebug | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptDebug interface
ms.assetid: e3e28cba-ee08-4a52-973a-b74be488c348
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0e21f4c99da886bc4907acf8b0934e1b46d57689
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942088"
---
# <a name="iactivescriptdebug-interface"></a>Interfaccia IActiveScriptDebug
Implementata dai motori di script che supportano il debug. In genere, un oggetto che implementa il `IActiveScriptDebug` implementa anche di interfaccia di `IActiveScript` interfaccia. In questo caso, chiama il `IActiveScript::QueryInterface` metodo per ottenere il `IActiveScriptDebug` interfaccia.  
  
 Il `IActiveScriptDebug` interfaccia fornisce i mezzi per:  
  
- Smart host ad assumere la gestione dei documenti.  
  
- Gestione di debug di processo per sincronizzare il debug di più motori di script.  
  
  Oltre ai metodi ereditati da `IUnknown`, il `IActiveScriptDebug` interfaccia espone i metodi seguenti.  
  
## <a name="methods-in-vtable-order"></a>Metodi nell'ordine Vtable  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[IActiveScriptDebug::GetScriptTextAttributes](../../winscript/reference/iactivescriptdebug-getscripttextattributes.md)|Restituisce gli attributi di testo per un blocco di testo dello script arbitrario.|  
|[IActiveScriptDebug::GetScriptletTextAttributes](../../winscript/reference/iactivescriptdebug-getscriptlettextattributes.md)|Restituisce gli attributi di testo per un scriptlet arbitrario.|  
|[IActiveScriptDebug::EnumCodeContextsOfPosition](../../winscript/reference/iactivescriptdebug-enumcodecontextsofposition.md)|Delega a `IDebugDocumentContext::EnumCodeContexts`.|