---
title: Metodo GetTaskSchedulersForDebugger | Microsoft Docs
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
- GetTaskSchedulersForDebugger method, TaskScheduler class [.NET Framework debug engines]
ms.assetid: 58aa236a-5ab8-4695-b303-89dffdbcd946
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f748eae50ab810477cb625eac4373903236fec82
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51749596"
---
# <a name="gettaskschedulersfordebugger-method"></a>Metodo GetTaskSchedulersForDebugger
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Recupera una matrice di tutti <xref:System.Threading.Tasks.TaskScheduler> gli oggetti che sono attualmente attivi.  
  
 **Spazio dei nomi:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Assembly:** mscorlib (in mscorlib. dll)  
  
 Poiché è possibile accedere a questo membro interno da .NET Framework, la sintassi seguente viene fornita in comune Intermediate Language (CIL).  
  
## <a name="syntax"></a>Sintassi  
  
```  
.method assembly hidebysig static class System.Threading.Tasks.TaskScheduler[] GetTaskSchedulersForDebugger() cil managed  
```  
  
## <a name="return-value"></a>Valore restituito  
 Una matrice di tutti i <xref:System.Threading.Tasks.TaskScheduler> gli oggetti che sono attualmente attivi in questo <xref:System.AppDomain>.  
  
## <a name="remarks"></a>Note  
 Questo metodo non è thread-safe e non deve essere utilizzato contemporaneamente ad altre istanze di <xref:System.Threading.Tasks.TaskScheduler>. Deve essere chiamato da un debugger solo quando il debugger ha sospeso tutti gli altri thread.  
  
## <a name="see-also"></a>Vedere anche  
 [Classe TaskScheduler](../../extensibility/debugger/taskscheduler-class-internal-members.md)

