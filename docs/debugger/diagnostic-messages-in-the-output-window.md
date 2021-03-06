---
title: Inviare messaggi alla finestra di Output | Microsoft Docs
ms.custom: ''
ms.date: 11/08/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- diagnostic messages [C#]
- System.Diagnostics.Debug class, Output window
- messages, diagnostic
- Debug.Print replacements
- diagnosis
- Output window, diagnostic messages
- System.Diagnostics.Trace class, Output window
- Trace class, diagnostic messages
- diagnostics
- debugger, Output window
- debugging [Visual Studio], diagnostic messages in Output window
- Debug class
ms.assetid: 386e9524-be17-4573-83fb-4f7c5cae0be0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 02bdd2c6d83e13887a8051ab4101627ba14220fa
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51724477"
---
# <a name="send-messages-to-the-output-window"></a>Inviare messaggi alla finestra di Output

È possibile scrivere messaggi in fase di esecuzione per il **Output** finestra utilizzando il <xref:System.Diagnostics.Debug> classe o il <xref:System.Diagnostics.Trace> classe, che fanno parte del <xref:System.Diagnostics> libreria di classi. Usare la <xref:System.Diagnostics.Debug> se si desidera solo output classe la *Debug* versione del programma. Usare la <xref:System.Diagnostics.Trace> classe se si desidera che l'output in entrambi il *eseguire il Debug* e *versione* versioni.  
  
## <a name="output-methods"></a>Metodi di output  
 Le classi <xref:System.Diagnostics.Trace> e <xref:System.Diagnostics.Debug> forniscono i seguenti metodi di output:  
  
- Diversi metodi `Write`, che generano informazioni senza interrompere l'esecuzione. Questi metodi sostituiscono il metodo `Debug.Print` utilizzato nelle versioni precedenti di Visual Basic.  
  
- <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=fullName> e <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=fullName> metodi, che interrompono l'esecuzione e l'output informazioni se si verifica un errore di una condizione specificata. Per impostazione predefinita, il metodo `Assert` visualizza le informazioni in una finestra di dialogo. Per altre informazioni, vedere [asserzioni nel codice gestito](../debugger/assertions-in-managed-code.md).  
  
- Il <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=fullName> e <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=fullName> metodi, che interrompono sempre le informazioni di esecuzione e l'output. Per impostazione predefinita, i metodi `Fail` visualizzano le informazioni in una finestra di dialogo.  
  
Il **Output** finestra può anche visualizzare le informazioni su:  
  
- I moduli caricati o scaricati dal debugger.  
  
- Le eccezioni generate.  
  
- I processi chiusi.  
  
- I thread chiusi.  
  
## <a name="see-also"></a>Vedere anche  
 [Sicurezza del debugger](../debugger/debugger-security.md)   
 [Finestra di output](../ide/reference/output-window.md)   
 [Traccia e strumentazione di applicazioni](/dotnet/framework/debug-trace-profile/tracing-and-instrumenting-applications)  
 [C#, F#e tipi di progetto Visual Basic](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [Debug del codice gestito](../debugger/debugging-managed-code.md)
