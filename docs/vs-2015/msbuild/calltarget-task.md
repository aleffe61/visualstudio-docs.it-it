---
title: Attività CallTarget | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- CallTarget task [MSBuild]
- MSBuild, CallTarget task
ms.assetid: bb1fe2c4-4383-436f-8326-c24cc4a46150
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fc3c5822732a4ae584500bfe1c48d7ba9e29b038
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49307677"
---
# <a name="calltarget-task"></a>Attività CallTarget
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Richiama le destinazioni specificate nel file di progetto.  
  
## <a name="task-parameters"></a>Parametri dell'attività  
 Nella tabella che segue vengono descritti i parametri dell'attività `CallTarget`.  
  
|Parametro|Descrizione|  
|---------------|-----------------|  
|`RunEachTargetSeparately`|Parametro di ouput facoltativo `Boolean`.<br /><br /> Se `true`, il motore [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] viene chiamato una volta per ogni destinazione. Se `false`, il motore [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] viene chiamato una volta per compilare tutte le destinazioni. Il valore predefinito è `false`.|  
|`TargetOutputs`|Parametro di output <xref:Microsoft.Build.Framework.ITaskItem>`[]` facoltativo.<br /><br /> Contiene l'output di tutte le destinazioni compilate.|  
|`Targets`|Parametro `String[]` facoltativo.<br /><br /> Specifica la destinazione o le destinazioni da compilare.|  
|`UseResultsCache`|Parametro `Boolean` facoltativo.<br /><br /> Se `true`, viene restituito il risultato memorizzato nella cache, se presente.<br /><br /> **Nota** Se l'attività MSBuild viene eseguita, il relativo output viene memorizzato nella cache in un ambito (ProjectFileName, GlobalProperties)[TargetNames] come elenco di elementi di compilazione.|  
  
## <a name="remarks"></a>Note  
 Se una destinazione specificata in `Targets` ha esito negativo e `RunEachTargetSeparately` è `true`, l'attività continua a compilare le destinazioni rimanenti.  
  
 Per compilare le destinazioni predefinite, usare l'[attività MSBuild](../msbuild/msbuild-task.md) e impostare il parametro `Projects` uguale a `$(MSBuildProjectFile)`.  
  
 Oltre ai parametri elencati sopra, questa attività eredita i parametri dalla classe <xref:Microsoft.Build.Tasks.TaskExtension>, che a sua volta eredita dalla classe <xref:Microsoft.Build.Utilities.Task>. Per un elenco di questi parametri aggiuntivi e le rispettive descrizioni, vedere [TaskExtension Base Class](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Esempio  
 L'esempio seguente chiama `TargetA` dall'interno di `CallOtherTargets`.  
  
```  
<Project DefaultTargets="CallOtherTargets"  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <Target Name="CallOtherTargets">  
        <CallTarget Targets="TargetA"/>  
    </Target>  
  
    <Target Name="TargetA">  
        <Message Text="Building TargetA..." />  
    </Target>  
  
</Project>  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimento alle attività](../msbuild/msbuild-task-reference.md)   
 [Destinazioni](../msbuild/msbuild-targets.md)



