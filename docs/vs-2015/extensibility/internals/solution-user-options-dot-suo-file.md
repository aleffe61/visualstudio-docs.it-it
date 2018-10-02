---
title: Opzioni utente della soluzione (. File suo) | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- .suo files, VSPackages
- suo files, VSPackages
- solutions, .suo files
- solutions, user options
- solution user options (.suo) file
ms.assetid: 75258e0d-600d-4a3d-94f4-3d7ac12cb47c
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 408acad4031417f4c3dd70b49758f8bee8e2819d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519543"
---
# <a name="solution-user-options-suo-file"></a>File delle opzioni utente della soluzione (con estensione suo)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [opzioni utente della soluzione (. File suo)](https://docs.microsoft.com/visualstudio/extensibility/internals/solution-user-options-dot-suo-file).  
  
Il file (con estensione suo) opzioni utente della soluzione contiene le opzioni di soluzione per ogni utente. Questo file non deve essere archiviato al controllo del codice sorgente.  
  
 Il file (con estensione suo) opzioni utente della soluzione è un'archiviazione strutturata o istruzione composta, file archiviati in un formato binario. Con il nome del flusso in corso la chiave che verrà usata per identificare le informazioni nel file con estensione suo è salvare le informazioni utente in flussi. Il file opzioni utente della soluzione viene usato per archiviare le impostazioni delle preferenze utente e viene creato automaticamente quando Visual Studio salva una soluzione.  
  
 Quando l'ambiente si apre un file con estensione suo, enumera tutti i pacchetti VSPackage attualmente caricati. Se un pacchetto VSPackage implementa il <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts> interface, quindi l'ambiente chiama il <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts.LoadUserOptions%2A> metodo nel pacchetto VSPackage chiedendo di caricare tutti i relativi dati dal file con estensione suo.  
  
 È responsabilità del VSPackage conoscere ciò che crea un flusso potrebbero essere state scritte nel file con estensione suo. Per ogni flusso che è stata scritta, il pacchetto VSPackage chiama nuovamente nell'ambiente tramite <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence.LoadPackageUserOpts%2A> per caricare un flusso specifico identificato dalla chiave, ovvero il nome del flusso. L'ambiente chiama quindi tornare a VSPackage per leggere tale flusso specifico passando il nome del flusso e un `IStream` puntatore per il <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence.LoadPackageUserOpts%2A> (metodo).  
  
 A questo punto, in cui viene effettuata un'altra chiamata a `LoadUserOptions` per verificare se esiste un'altra sezione del file con estensione suo che deve essere letto. Questo processo continua finché tutti i flussi di dati nel file con estensione suo sono stati letti ed elaborati dall'ambiente.  
  
 Quando la soluzione viene salvata o chiuso, l'ambiente chiama il <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence.SavePackageSolutionProps%2A> metodo con un puntatore al <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts.SaveUserOptions%2A> (metodo). Un `IStream` contenente le informazioni da salvare binarie viene passato per il <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts.WriteUserOptions%2A> metodo, che quindi scrive le informazioni per il file con estensione suo e chiama il `SaveUserOptions` metodo per verificare se esiste un altro flusso di informazioni per scrivere il suo file.  
  
 Questi due metodi, `SaveUserOptions` e `WriteUserOptions`, vengono chiamati in modo ricorsivo per ogni flusso di informazioni da salvare nel file con estensione suo, passando il puntatore a `IVsSolutionPersistence`. Tali metodi vengono chiamati in modo ricorsivo per consentire la scrittura di più flussi per il file con estensione suo. In tal modo, le informazioni utente sono persistenti con la soluzione e vengano garantito che sia presente alla successiva apertura della soluzione.  
  
## <a name="see-also"></a>Vedere anche  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts>   
 [Soluzioni](../../extensibility/internals/solutions.md)
