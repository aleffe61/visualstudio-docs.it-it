---
title: Download di Remote debugger
description: I collegamenti di download per il debugger remoto
services: ''
author: mikejo5000
ms.service: ''
ms.topic: include
ms.date: 05/23/2018
ms.author: mikejo
ms.custom: include file
ms.openlocfilehash: 6c429614a094ceefc4f9a1e358ebc8ee26c40773
ms.sourcegitcommit: 1df0ae74af03bcf0244129a29fd6bd605efc9f61
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/01/2018
ms.locfileid: "50915188"
---
Nel dispositivo remoto o server che si desidera eseguire il debug su, anziché il computer di Visual Studio, scaricare e installare la versione corretta di remote tools usando i collegamenti disponibili nella tabella seguente.

- Scaricare remote tools per la versione di Visual Studio più recente. La versione più recente di remote tools è compatibile con le versioni precedenti di Visual Studio, ma le versioni precedenti di strumenti remoti non sono compatibili con versioni più recenti di Visual Studio. 
- Scaricare gli strumenti remoti con la stessa architettura del computer in che si li installa. Ad esempio, se si desidera eseguire il debug di un'app a 32 bit in un computer remoto che esegue un sistema operativo a 64 bit, installare gli strumenti remoti a 64 bit. 

|Versione|Collegamento|Note|
|-|-|-|
|Visual Studio 2017 (versione più recente)|[Remote tools](https://visualstudio.microsoft.com/downloads/?q=remote+tools#remote-tools-for-visual-studio-2017)|È compatibile con tutte le versioni di Visual Studio 2017. Scaricare la versione corrispondente del sistema operativo del dispositivo (x x86, x64 o ARM64). In Windows Server, vedere [sbloccare il download del file](../../debugger/remote-debugging-unblock-file-download.md) per download di remote tools.|
|Visual Studio 2015|[Remote tools](https://my.visualstudio.com/Downloads?q=remote%20tools%20visual%20studio%202015)|Remote tools per Visual Studio 2015 sono disponibili da My.VisualStudio.com. Se richiesto, aggiungere il prodotto gratuito [Visual Studio Dev Essentials](https://visualstudio.microsoft.com/dev-essentials/) programma oppure accedere con l'ID sottoscrizione di Visual Studio. In Windows Server, vedere [sbloccare il download del file](../../debugger/remote-debugging-unblock-file-download.md) per download di remote tools.|
|Visual Studio 2013|[Remote tools](/previous-versions/visualstudio/visual-studio-2013/bt727f1t(v=vs.120)#Installing_the_Remote_Tools)|2000A nella documentazione di Visual Studio 2013|
|Visual Studio 2012|[Remote tools](/previous-versions/visualstudio/visual-studio-2012/bt727f1t(v=vs.110)#BKMK_Installing_the_Remote_Tools)|2000A nella documentazione di Visual Studio 2012|

È possibile eseguire il debugger remoto copiando *msvsmon.exe* al computer remoto, anziché di installazione di remote tools. Tuttavia, la configurazione guidata Debugger remoto (*rdbgwiz.exe*) è disponibile solo quando si installa remote tools. Potrebbe essere necessario usare la procedura guidata per la configurazione se si desidera eseguire il debugger remoto come servizio. Per altre informazioni, vedere [(facoltativo) configurare il debugger remoto come servizio](../../debugger/remote-debugging.md#bkmk_configureService).

>[!NOTE]
>- Per eseguire il debug delle app di Windows 10 nei dispositivi ARM, usare ARM64, che è disponibile con la versione più recente di remote tools.  
>- Per eseguire il debug delle app di Windows 10 nei dispositivi Windows RT, utilizzare ARM, che è disponibile solo in Visual Studio 2015 download di remote tools.

