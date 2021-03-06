---
title: "Errore: Debug non è riuscita perché non è abilitata l'autenticazione integrata di Windows | Microsoft Docs"
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.webdbg_ntlm_authn_not_enabled
dev_langs:
- FSharp
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- debugger, Web application errors
ms.assetid: 6027cd94-74cf-470f-b7ce-6f6b68bc56ba
caps.latest.revision: 22
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0b922e8e8fde8b185207810d107afb9a9c5a6e05
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51757256"
---
# <a name="error-debugging-failed-because-integrated-windows-authentication-is-not-enabled"></a>Errore: debug non riuscito. Non è attivata l'autenticazione di Windows integrata
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

L'autenticazione dell'utente che ha richiesto il debug non è stata possibile a causa di un errore di autenticazione. Questo errore può verificarsi quando si tenta di eseguire un'applicazione Web o un servizio Web XML. Una causa di questo errore è la mancata attivazione dell'autenticazione di Windows integrata. Per attivarla, seguire i passaggi della procedura relativa all'attivazione dell'autenticazione integrata di Windows.  
  
 Se è stata abilitata l'autenticazione integrata di Windows e viene ancora visualizzato questo errore, è possibile che questo errore sia dovuto **all'attivazione dell'autenticazione del Digest per i server di dominio Windows** è abilitata. In questa situazione è necessario consultare l'amministratore di rete.  
  
### <a name="to-enable-integrated-windows-authentication"></a>Per attivare l'autenticazione di Windows integrata  
  
1.  Accedere al server Web mediante un account amministratore.  
  
2.  Fare clic su **avviare** e quindi fare clic su **Pannello di controllo**.  
  
3.  Nelle **Pannello di controllo**, fare doppio clic su **strumenti di amministrazione**.  
  
4.  Fare doppio clic su **Internet Information Services**.  
  
5.  Fare clic sul nodo del server Web.  
  
     Oggetto **siti Web** verrà visualizzata la cartella sotto il nome del server.  
  
6.  È possibile configurare l'autenticazione per tutti i siti Web complessivamente o singolarmente. Per configurare l'autenticazione per tutti i siti Web, fare doppio clic il **siti Web** cartella e quindi fare clic su **proprietà**. Per configurare l'autenticazione per un singolo sito Web, aprire il **siti Web** cartella, fare doppio clic su singolo sito Web e quindi fare clic su **proprietà**.  
  
     Il **proprietà** verrà visualizzata la finestra di dialogo.  
  
7.  Scegliere il **sicurezza Directory** scheda.  
  
8.  Nel **controllo autenticazione e accesso anonimo** fare clic su **modificare**.  
  
     Il **metodi di autenticazione** verrà visualizzata la finestra di dialogo.  
  
9. Sotto **l'accesso autenticato**, selezionare **autenticazione Windows integrata**.  
  
10. Fare clic su **OK** per chiudere la **metodi di autenticazione** nella finestra di dialogo.  
  
11. Fare clic su **OK** per chiudere la **proprietà** nella finestra di dialogo.  
  
12. Chiudi il **Internet Information Services** finestra.  
  
### <a name="to-enable-integrated-windows-authentication-in-windows-vistaiis-7"></a>Per attivare l'autenticazione integrata di Windows in Windows Vista/IIS 7  
  
1.  Accedere al server Web mediante un account amministratore.  
  
2.  Attivare Autenticazione di Windows e Compatibilità di gestione con IIS 6, se tale operazione non è stata già effettuata, seguendo questi passaggi:  
  
    1.  Fare clic su **avviare**, fare clic su **Pannello di controllo** e quindi fare clic su **programmi**.  
  
    2.  Sotto **programmi e funzionalità**, fare clic su **o disattivazione delle funzionalità Windows attivare**.  
  
         Verrà visualizzata la finestra di dialogo Controllo di accesso utente e verrà richiesto di immettere l'autorizzazione per continuare.  
  
    3.  Scegliere **Continua**.  
  
         Verrà visualizzata la finestra di dialogo Funzionalità Windows.  
  
    4.  Nell'elenco delle funzionalità, espandere la **Internet Information Services** nodo.  
  
    5.  Sotto **Internet Information Services**, espandere il **servizi World Wide Web** nodo.  
  
    6.  Sotto **servizi World Wide Web**, fare clic su **sicurezza**.  
  
    7.  Fare clic su **Windows autenticazione**.  
  
    8.  Sotto **Internet Information Services**, espandere il **strumenti di gestione Web** nodo.  
  
    9. Sotto **strumenti di gestione Web**, espandere il **compatibilità Gestione IIS 6** nodo e selezionare il **IIS 6 Metabase and IIS 6 Configuration Compatibility** casella di controllo.  
  
    10. Sotto **strumenti di gestione Web**, selezionare **Console di gestione IIS** e fare clic su **OK.**  
  
    11. Per rendere effettive queste modifiche, riavviare il computer.  
  
3.  Fare clic su **avviare** e quindi fare clic su **Pannello di controllo**.  
  
4.  Fare clic su **visualizzazione classica**, quindi fare doppio clic su **strumenti di amministrazione**.  
  
5.  Nel **Name** colonna e fare doppio clic su **Internet Information Services (IIS) Manager**.  
  
6.  Nel **connessioni** colonna, espandere il nodo per il server.  
  
     Oggetto **siti Web** verrà visualizzata la cartella sotto il nome del server.  
  
7.  Espandere la **siti Web** nodo e fare clic sul sito Web per il quale si desidera abilitare l'autenticazione integrata di Windows.  
  
8.  Il titolo del riquadro centrale viene sostituito con il nome del sito Web selezionato. In questo riquadro, sotto il **IIS** intestazione, fare doppio clic su **autenticazione**.  
  
     Il titolo del riquadro viene sostituito con **autenticazione**.  
  
9. Nel **Authentication** riquadro, nella **nome** colonna, fare doppio clic su **l'autenticazione di Windows** e quindi fare clic su **abilitare**.  
  
10. Chiudi il **Internet Information Services (IIS) Manager** finestra.  
  
## <a name="see-also"></a>Vedere anche  
 [Debug di applicazioni Web: Errori e risoluzione dei problemi](../debugger/debugging-web-applications-errors-and-troubleshooting.md)   
 [Autenticazione Digest Microsoft](http://go.microsoft.com/fwlink/?LinkId=77938)   
 [Esecuzione di applicazioni Web in Windows Vista con IIS 7.0 e Visual Studio](http://msdn.microsoft.com/library/262a82ac-dd0e-4096-86c6-fb463e88be66)



