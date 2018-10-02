---
title: Attività LIB | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VC.Project.VCLibrarianTool.Name
- VC.Project.VCLibrarianTool.TreatLibWarningsAsErrors
- VC.Project.VCLibrarianTool.Verbose
- vc.task.lib
- VC.Project.VCLibrarianTool.ErrorReporting
- VC.Project.VCLibrarianTool.LinkLibraryDependencies
- VC.Project.VCLibrarianTool.LinkTimeCodeGeneration
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), LIB task
- LIB task (MSBuild (Visual C++))
ms.assetid: e062c7f9-cc69-4a83-9361-1bb5355e5fe8
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dcdcece820af764e627aafc43ef405c627724b68
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/05/2018
ms.locfileid: "47590838"
---
# <a name="lib-task"></a>Attività LIB
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [attività LIB](https://docs.microsoft.com/visualstudio/msbuild/lib-task).  
  
  
Esegue il wrapping dello strumento di gestione librerie Microsoft a 32 bit, lib.exe. Gestione librerie crea e gestisce una libreria di file oggetto COFF (Common Object File Format). Gestione librerie può inoltre creare file di esportazione e librerie di importazione per fare riferimento a definizioni esportate. Per altre informazioni, vedere [Riferimenti a LIB](http://msdn.microsoft.com/library/ecc7f643-bbd4-47a3-8dc6-b360f880db91) ed [Esecuzione di LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).  
  
## <a name="parameters"></a>Parametri  
 La tabella seguente descrive i parametri dell'attività **LIB**. La maggior parte dei parametri attività corrisponde a un'opzione della riga di comando.  
  
|Parametro|Descrizione|  
|---------------|-----------------|  
|**AdditionalDependencies**|Parametro **String[]** facoltativo.<br /><br /> Specifica altri elementi da aggiungere alla riga di comando.|  
|**AdditionalLibraryDirectories**|Parametro **String[]** facoltativo.<br /><br /> Esegue l'override del percorso delle librerie dell'ambiente. Specificare un nome di directory.<br /><br /> Per altre informazioni, vedere [/LIBPATH (Percorso LIB aggiuntivo)](http://msdn.microsoft.com/library/7240af0b-9a3d-4d53-8169-2a92cd6958ba).|  
|**AdditionalOptions**|Parametro **String** facoltativo.<br /><br /> Un elenco di opzioni lib.exe come specificato nella riga di comando. Ad esempio, * * "_/option1 opzione2 /opzione #_". Usare questo parametro per specificare le opzioni di lib.exe che non sono rappresentate da altri parametri dell'attività **LIB**.<br /><br /> Per altre informazioni, vedere [Esecuzione di LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**DisplayLibrary**|Parametro **String** facoltativo.<br /><br /> Visualizza le informazioni sulla libreria di output. Specificare un nome di file per reindirizzare le informazioni a un file. Specificare "CON" o niente per reindirizzare le informazioni alla console.<br /><br /> Questo parametro corrisponde all'opzione **/LIST** di lib.exe.|  
|**ErrorReporting**|Parametro **String** facoltativo.<br /><br /> Specifica come inviare a Microsoft informazioni sull'errore interno in caso di esito negativo di lib.exe in fase di esecuzione.<br /><br /> Specificare uno dei valori seguenti, ognuno dei quali corrisponde a un'opzione della riga di comando.<br /><br /> -   **NoErrorReport** - **/ERRORREPORT:NONE**<br />-   **PromptImmediately** - **/ERRORREPORT:PROMPT**<br />-   **QueueForNextLogin** - **/ERRORREPORT:QUEUE**<br />-   **SendErrorReport** - **/ERRORREPORT:SEND**<br /><br /> Per altre informazioni, vedere l'opzione della riga di comando **/ERRORREPORT** in [Esecuzione di LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**ExportNamedFunctions**|Parametro **String[]** facoltativo.<br /><br /> Specifica una o più funzioni da esportare.<br /><br /> Questo parametro corrisponde all'opzione **/EXPORT:** di lib.exe.|  
|**ForceSymbolReferences**|Parametro **String** facoltativo.<br /><br /> Impone a lib.exe di includere un riferimento al simbolo specificato.<br /><br /> Questo parametro corrisponde all'opzione **/INCLUDE:** di lib.exe.|  
|**IgnoreAllDefaultLibraries**|Parametro `Boolean` facoltativo.<br /><br /> Se `true`, vengono rimosse tutte le librerie predefinite dall'elenco di librerie che lib.exe cerca per risolvere i riferimenti esterni.<br /><br /> Questo parametro corrisponde alla forma senza parametri dell'opzione **/NODEFAULTLIB** di lib.exe.|  
|**IgnoreSpecificDefaultLibraries**|Parametro **String[]** facoltativo.<br /><br /> Rimuove tutte le librerie specificate dall'elenco di librerie che lib.exe cerca per risolvere i riferimenti esterni.<br /><br /> Questo parametro corrisponde all'opzione **/NODEFAULTLIB** di lib.exe che accetta un argomento `library`.|  
|**LinkLibraryDependencies**|Parametro `Boolean` facoltativo.<br /><br /> Se `true`, specifica che gli output della libreria dalle dipendenze del progetto vengono collegati automaticamente.|  
|**LinkTimeCodeGeneration**|Parametro `Boolean` facoltativo.<br /><br /> Se `true`, specifica la generazione del codice in fase di collegamento.<br /><br /> Questo parametro corrisponde all'opzione **/LCTG** di lib.exe.|  
|**MinimumRequiredVersion**|Parametro **String** facoltativo.<br /><br /> Specifica la versione minima richiesta del sottosistema. Specificare un elenco delimitato da virgole di numeri decimali nell'intervallo compreso tra 0 e 65535.|  
|**ModuleDefinitionFile**|Parametro **String** facoltativo.<br /><br /> Specifica il nome del file di definizione moduli (con estensione def).<br /><br /> Questo parametro corrisponde all'opzione **/DEF** di lib.exe che accetta un argomento `filename`.|  
|**Name**|Parametro **String** facoltativo.<br /><br /> Quando si compila una libreria di importazione, è necessario specificare il nome della DLL per la quale compilare la libreria di importazione.<br /><br /> Questo parametro corrisponde all'opzione **/NAME** di lib.exe che accetta un argomento `filename`.|  
|**OutputFile**|Parametro **String** facoltativo.<br /><br /> Sostituisce il nome e il percorso predefiniti del programma creato da lib.exe.<br /><br /> Questo parametro corrisponde all'opzione **/OUT** di lib.exe che accetta un argomento `filename`.|  
|**RemoveObjects**|Parametro **String[]** facoltativo.<br /><br /> Omette l'oggetto specificato dalla libreria di output. Lib.exe crea una libreria di output combinando tutti gli oggetti, siano essi in file oggetto o in librerie, quindi eliminando tutti gli oggetti specificati con questa opzione.<br /><br /> Questo parametro corrisponde all'opzione **/REMOVE** di lib.exe che accetta un argomento `membername`.|  
|**Sources**|Parametro `ITaskItem[]` obbligatorio.<br /><br /> Specifica un elenco dei file di origine separati da spazi.|  
|**SubSystem**|Parametro **String** facoltativo.<br /><br /> Specifica l'ambiente per il file eseguibile. La scelta del sottosistema riguarda il simbolo del punto di ingresso o la funzione di punto di ingresso.<br /><br /> Specificare uno dei valori seguenti, ognuno dei quali corrisponde a un'opzione della riga di comando.<br /><br /> -   **Console** - **/SUBSYSTEM:CONSOLE**<br />-   **Windows** - **/SUBSYSTEM:WINDOWS**<br />-   **Native** - **/SUBSYSTEM:NATIVE**<br />-   **Applicazione EFI** - **/SUBSYSTEM:EFI_APPLICATION**<br />-   **Driver servizio di avvio EFI** - **/SUBSYSTEM:EFI_BOOT_SERVICE_DRIVER**<br />-   **ROM EFI** - **/SUBSYSTEM:EFI_ROM**<br />-   **Runtime EFI** - **/SUBSYSTEM:EFI_RUNTIME_DRIVER**<br />-   **WindowsCE** - **/SUBSYSTEM:WINDOWSCE**ReplaceThisText<br />-   **POSIX** - **/SUBSYSTEM:POSIX**<br /><br /> Per altre informazioni, vedere [/SUBSYSTEM (Specifica il sottosistema)](http://msdn.microsoft.com/library/d7b133cf-cf22-4da8-ab46-6552702c0b9b).|  
|**SuppressStartupBanner**|Parametro **Boolean** facoltativo.<br /><br /> Se `true`, impedisce la visualizzazione del messaggio sul copyright e sul numero di versione all'avvio dell'attività.<br /><br /> Per altre informazioni, vedere l'opzione **/NOLOGO** in [Esecuzione di LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**TargetMachine**|Parametro **String** facoltativo.<br /><br /> Specifica la piattaforma di destinazione per il programma o DLL.<br /><br /> Specificare uno dei valori seguenti, ognuno dei quali corrisponde a un'opzione della riga di comando.<br /><br /> -   **MachineARM** - **/MACHINE:ARM**<br />-   **MachineEBC** - **/MACHINE:EBC**<br />-   **MachineIA64** - **/MACHINE:IA64**<br />-   **MachineMIPS** - **/MACHINE:MIPS**<br />-   **MachineMIPS16** - **/MACHINE:MIPS16**<br />-   **MachineMIPSFPU** -**/MACHINE:MIPSFPU**<br />-   **MachineMIPSFPU16** - **/MACHINE:MIPSFPU16**<br />-   **MachineSH4** - **/MACHINE:SH4**<br />-   **MachineTHUMB** - **/MACHINE:THUMB**<br />-   **MachineX64** - **/MACHINE:X64**<br />-   **MachineX86** - **/MACHINE:X86**<br /><br /> Per altre informazioni, vedere [/MACHINE (Specifica la piattaforma di destinazione)](http://msdn.microsoft.com/library/8d41bf4b-7e53-4ab9-9085-d852b08d31c2).|  
|**TrackerLogDirectory**|Parametro **String** facoltativo.<br /><br /> Specifica la directory del log di Tracker.|  
|**TreatLibWarningAsErrors**|Parametro **Boolean** facoltativo.<br /><br /> Se `true`, non consente all'attività **LIB** di generare un file di output se lib.exe genera un avviso. Se `false`, viene generato un file di output.<br /><br /> Per altre informazioni, vedere l'opzione **/WX** in [Esecuzione di LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**UseUnicodeResponseFiles**|Parametro **Boolean** facoltativo.<br /><br /> Se `true`, consente al sistema di progetto di generare file di risposta UNICODE quando viene generata la Gestione di librerie. Specificare `true` quando i percorsi dei file nel progetto sono UNICODE.|  
|**Verbose**|Parametro **Boolean** facoltativo.<br /><br /> Se `true`, vengono visualizzati i dettagli sullo stato di avanzamento della sessione, inclusi i nomi dei file con estensione obj da aggiungere. Le informazioni vengono inviate all'output standard e possono essere reindirizzate a un file.<br /><br /> Per altre informazioni, vedere l'opzione **/VERBOSE** in [Esecuzione di LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
  
## <a name="remarks"></a>Note  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimenti alle attività](../msbuild/msbuild-task-reference.md)


