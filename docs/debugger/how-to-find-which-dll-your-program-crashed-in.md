---
title: 'Procedura: individuare la DLL del programma arrestato in modo anomalo | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.dll
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, DLL crashes
- Module List dialog box
- errors [debugger], DLL crashes
- Modules window
- debugging [Visual Studio], DLL crashes
- DLLs, load order of
ms.assetid: ecf62568-8b65-4a41-b8a4-e962ff2dfb71
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 40f27e0bec20e1dd037beaa5f60ea648c0ccb171
ms.sourcegitcommit: a7de99f36e9ead7ea9e9bac23c88d05ddfc38b00
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2018
ms.locfileid: "52257097"
---
# <a name="how-to-find-which-dll-your-program-crashed-in-c-c-visual-basic-f"></a>Procedura: individuare la DLL del programma arrestato in modo anomalo (C#, C++, Visual Basic, F#)
  
 Se l'applicazione si arresta in modo anomalo durante la chiamata a una DLL di sistema o al codice di un altro utente, è necessario identificare la DLL attiva al momento dell'arresto. Se si verifica un arresto anomalo del sistema in una DLL esterna al programma, è possibile identificare il percorso usando il **moduli** finestra.  
  
### <a name="to-find-where-a-crash-occurred-using-the-modules-window"></a>Per stabilire la posizione in cui si è verificato un arresto anomalo mediante la finestra Moduli  
  
1.  Annotare l'indirizzo in cui si è verificato l'arresto.

    Se l'indirizzo non viene visualizzato nel messaggio di errore, si potrebbe essere necessario utilizzare metodi alternativi per identificare la DLL. Se si sospetta che una DLL di sistema, è possibile [caricare i simboli](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md) dai server dei simboli Microsoft durante il debug. In caso contrario, potrebbe essere necessario [creare un file di dump](../debugger/using-dump-files.md) con heap invece informazioni. Vari [strumenti](https://blogs.msdn.microsoft.com/andrehal/2009/12/31/what-is-a-dump-and-how-do-i-create-one/) sono disponibili per creare file dump.
  
2.  Nel **eseguire il Debug** menu, scegliere **Windows**, fare clic su **moduli**.  
  
3.  Nel **moduli** finestra, trovare il **indirizzo** colonna. Per visualizzarla potrebbe essere necessario utilizzare la barra di scorrimento.  
  
4.  Scegliere il **indirizzo** nella parte superiore della colonna per ordinare le DLL in base all'indirizzo.  
  
5.  Cercare nell'elenco ordinato la DLL il cui intervallo di indirizzi contenga la posizione in cui si è verificato l'arresto anomalo.  
  
6.  Esaminare i **Name** e **percorso** colonne per visualizzare il nome della DLL e il percorso.  
  
## <a name="see-also"></a>Vedere anche  
 [Debug di progetti di DLL](../debugger/debugging-dll-projects.md)   
 [Procedura: Usare la finestra Moduli](../debugger/how-to-use-the-modules-window.md)