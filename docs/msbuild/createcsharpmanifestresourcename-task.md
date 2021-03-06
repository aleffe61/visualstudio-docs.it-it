---
title: Attività CreateCSharpManifestResourceName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, CreateCSharpManifestResourceName task
- CreateCSharpManifestResourceName task [MSBuild]
ms.assetid: 2ace88c1-d757-40a7-8158-c1d3f5ff0511
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 18f2ea8db1e3f68ef20db09b8b129a50272e44f9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53966385"
---
# <a name="createcsharpmanifestresourcename-task"></a>Attività CreateCSharpManifestResourceName
Crea un nome di manifesto nello stile di [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] da un nome file con estensione *resx* specifico o da un'altra risorsa.  

## <a name="parameters"></a>Parametri  
 La tabella seguente descrive i parametri dell'[attività CreateCSharpManifestResourceName](../msbuild/createcsharpmanifestresourcename-task.md).  


| Parametro | Description |
| - | - |
| `ManifestResourceNames` | Parametro <xref:Microsoft.Build.Framework.ITaskItem> `[]` di output di sola lettura.<br /><br /> Nomi di manifesto risultanti. |
| `ResourceFiles` | Parametro `String` obbligatorio.<br /><br /> Nome del file di risorse da cui creare il nome del manifesto [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)]. |
| `RootNamespace` | Parametro `String` facoltativo.<br /><br /> Spazio dei nomi radice del file di risorse, in genere derivato dal file di progetto. Può essere `null`. |
| `PrependCultureAsDirectory` | Parametro `Boolean` facoltativo.<br /><br /> Se `true`, il nome delle impostazioni cultura viene aggiunto come nome di directory prima del nome di risorsa di manifesto. Il valore predefinito è `true`. |
| `ResourceFilesWithManifestResourceNames` | Parametro di output di sola lettura `String` facoltativo.<br /><br /> Restituisce il nome del file di risorse che include ora il nome di risorsa di manifesto. |

## <a name="remarks"></a>Note  
 L'[attività CreateVisualBasicManifestResourceName](../msbuild/createvisualbasicmanifestresourcename-task.md) determina il nome di risorsa di manifesto appropriato da assegnare a un file con estensione *resx* specificato o a un altro file di risorse. L'attività fornisce un nome logico a un file di risorse e quindi lo associa a un parametro di output come metadato.  

 Oltre ai parametri elencati sopra, questa attività eredita i parametri dalla classe <xref:Microsoft.Build.Tasks.TaskExtension>, che a sua volta eredita dalla classe <xref:Microsoft.Build.Utilities.Task>. Per un elenco di questi parametri aggiuntivi e le rispettive descrizioni, vedere [Classe di base TaskExtension](../msbuild/taskextension-base-class.md).  

## <a name="see-also"></a>Vedere anche  
 [Attività](../msbuild/msbuild-tasks.md)   
 [Riferimenti delle attività MSBuild](../msbuild/msbuild-task-reference.md)