---
title: IDebugSymbolProviderDirect | Microsoft Docs
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
- IDebugSymbolProviderDirect interface
ms.assetid: 872b04a8-70de-4ab5-aceb-684c81828545
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4d0586966564b0159dc0dd6d17b3e8f09f948157
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51751677"
---
# <a name="idebugsymbolproviderdirect"></a>IDebugSymbolProviderDirect
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Rappresenta un provider di simboli che ha accesso diretto alle interfacce di simbolo dei metadati e i core.  
  
## <a name="syntax"></a>Sintassi  
  
```  
IDebugSymbolProviderDirect: IUnknown  
```  
  
## <a name="methods"></a>Metodi  
 Questa interfaccia implementa i metodi seguenti:  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[GetAppIDFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getappidfromaddress.md)|Recupera l'identificatore del dominio dell'applicazione fornito l'indirizzo di debug.|  
|[GetCurrentModulesInfo](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesinfo.md)|Recupera le informazioni sui moduli del gruppo di simboli.|  
|[GetCurrentModulesState](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesstate.md)|Recupera le informazioni relative al gruppo di simboli di cui il provider di simboli è un membro.|  
|[GetMetaDataImport](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmetadataimport.md)|Recupera le informazioni di importazione dei metadati.|  
|[GetMethodFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmethodfromaddress.md)|Recupera le informazioni sul metodo in corrispondenza dell'indirizzo di debug specificato.|  
|[GetSymUnmanagedReader](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getsymunmanagedreader.md)|Recupera un lettore di simboli per codice non gestito.|  
  
## <a name="remarks"></a>Note  
 Questa interfaccia può essere utilizzata invece la maggior parte delle altre interfacce di provider di simboli. Fornisce accesso diretto ai metadati e `CorSym` interfacce.  
  
## <a name="requirements"></a>Requisiti  
 Intestazione: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

