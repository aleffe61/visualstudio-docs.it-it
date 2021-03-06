---
title: 'Errore: Autenticazione Kerberos non riesce. | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.callback_kerberos_auth_failed
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 0cf34885ee715a5685e4c2ced8b5a116e5c33e8d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49857664"
---
# <a name="error-kerberos-authentication-failed"></a>Errore: autenticazione Kerberos non riuscita
Quando si tenta di eseguire il debug remoto, è possibile che venga visualizzato il messaggio di errore seguente:  
  
```cmd
Error: The Visual Studio Remote Debugger on the target computer cannot connect back to this computer. Kerberos authentication failed.  
```  
  
 L'errore si verifica quando Visual Studio Remote Debugging Monitor è in esecuzione con l'account di sistema locale o l'account del servizio di rete. Utilizzando uno di questi account, il debugger remoto deve stabilire una connessione di autenticazione Kerberos allo scopo di inviare comunicazioni al computer host del debugger Visual Studio.  
  
 L'autenticazione Kerberos non è disponibile nei seguenti casi:  
  
- Il computer di destinazione o il computer host del debugger si trova in un gruppo di lavoro anziché in un dominio.  
  
   \- oppure -  
  
- Kerberos è stato disabilitato sul controller di dominio.  
  
  Se l'autenticazione Kerberos non è disponibile, modificare l'account utilizzato per l'esecuzione di Visual Studio Remote Debugging Monitor. Per istruzioni, vedere [errori: servizio di Visual Studio Remote Debugger nel computer di destinazione non può connettersi al computer](../debugger/error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer.md).  
  
  Se il messaggio di errore viene visualizzato nonostante entrambi i computer siano connessi allo stesso dominio, verificare che il nome del computer host del debugger venga risolto correttamente dal DNS del computer di destinazione. Attenersi alla procedura indicata di seguito.  
  
### <a name="to-verify-that-dns-on-the-target-computer-is-correctly-resolving-the-debugger-host-computer-name"></a>Per verificare la corretta risoluzione del nome del computer host del debugger da parte del DNS del computer di destinazione  
  
1.  Nel computer di destinazione, aprire il **avviare** dal menu **Accessori** e quindi fare clic su **prompt dei comandi**.  
  
2.  Nel **prompt dei comandi** finestra, digitare:  
  
    ```cmd
    ping <debugger_host_computer_name>  
    ```  
  
3.  Nella prima riga della risposta `ping` viene indicato il nome completo del computer e l'indirizzo IP restituito dal DNS per il computer specificato.  
  
4.  Nel computer host del debugger, aprire una **prompt dei comandi** finestra ed eseguire `ipconfig`.  
  
5.  Confrontare i valori degli indirizzi IP.  
  
## <a name="see-also"></a>Vedere anche  
 [Risoluzione dei problemi e gli errori di debug remoto](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Remote Debugging](../debugger/remote-debugging.md)
