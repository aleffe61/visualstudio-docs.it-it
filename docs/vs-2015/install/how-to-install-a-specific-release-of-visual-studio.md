---
title: 'Procedura: installare una versione specifica di Visual Studio | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-install
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- install a specific release, Visual Studio
ms.assetid: d69ad0f8-f0a0-438e-a0ef-777c4868f139
caps.latest.revision: 20
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 17d4d099bdbb36b715b8a4cbb02facafe41c261d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47527343"
---
# <a name="how-to-install-a-specific-release-of-visual-studio"></a>Procedura: Installare una versione specifica di Visual Studio
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Il programma di installazione di Visual Studio viene aggiornato spesso in modo da offrire la versione più recente e ottimizzata delle funzionalità facoltative.  Tuttavia, se si vuole installare una versione precedente di Visual Studio 2015, ad esempio una versione di Visual Studio precedente a Update 1 con supporto per iOS, è necessario forzare il programma di installazione di Visual Studio in modo che usi una versione precedente dei file manifesto delle funzionalità. Questo articolo illustra la procedura specifica.  
  
## <a name="installing-the-current-release"></a>Installazione della versione corrente  
 Dopo la versione iniziale di Visual Studio 2015, abbiamo aggiornato il motore di installazione e i file manifesto più volte.  Ciò significa che se si scarica il programma di installazione web di [download di Visual Studio](https://www.visualstudio.com/downloads/download-visual-studio-vs) sito Web in un computer pulito e connesso a internet, aggiornano le installazioni imposta la versione più recente di Visual Studio 2015, che include i miglioramenti più recenti del prodotto Oltre a versioni più recenti di strumenti e le funzionalità facoltative.  
  
## <a name="installing-earlier-releases"></a>Installazione di versioni precedenti  
 È possibile creare e montare un'immagine ISO, oppure è possibile scaricare e avviare il programma di installazione direttamente dal [My.VisualStudio.com](https://my.visualstudio.com/downloads?q=visual%20studio%20enterprise%202015) e quindi aggiungere il file .exe con parametri della riga di comando aggiuntivi (ad esempio /CustomInstallPath, / completo, / InstallSelectableItems, /NoRestart e così via.) Per controllare la modalità di installazione Visual Studio.  
  
 Nella tabella seguente include alcuni scenari punto temporizzato specifici e i parametri della riga di comando necessari, che è necessario passare al programma di installazione di Enterprise edition. Gli stessi parametri possono essere usati anche con i programmi di installazione delle edizioni Community o Professional.  
  
|Edizione Visual Studio 2015|Versione da eseguire|Riga di comando da usare|Comportamento dell'installazione|  
|--------------------------------|-----------------|--------------------------|---------------------|  
|Visual Studio Enterprise (versione pubblica più recente)|Visual Studio Enterprise con gli aggiornamenti (disponibile dal [My.VisualStudio.com](https://my.visualstudio.com/downloads?q=visual%20studio%20enterprise%202015))|`vs_enterprise.exe` **Nota:** il comportamento predefinito di questa installazione offre le funzionalità facoltative più recenti e di conseguenza, non richiede i parametri della riga di comando.|L'installazione di Visual Studio userà il file feed.xml più recente e installerà i file più recenti.|  
|Visual Studio Enterprise Update 3 (Update 3 originale senza ulteriori aggiornamenti Update 3-era)|Visual Studio Enterprise RTM (disponibile nella [pagina di download per i titolari di abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/downloads/))|`vs_enterprise.exe /OverrideFeedURI http://download.microsoft.com/download/6/B/B/6BBD3561-D764-4F39-AB8E-05356A122545/20160628.2/enu/feed.xml`|Installazione di Visual Studio userà il file feed. XML disponibile al rilascio di Update 3|  
|Visual Studio Enterprise Update 2 (originale l'aggiornamento 2, ma con aggiornamenti che pre-aggiornamento di Update 3)|Visual Studio Enterprise RTM (disponibile nella [pagina di download per i titolari di abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/downloads/))|`vs_enterprise.exe /OverrideFeedURI http://download.microsoft.com/download/6/B/B/6BBD3561-D764-4F39-AB8E-05356A122545/20160620.2/enu/feed.xml`|Installazione di Visual Studio userà il file feed. XML corrente prima del rilascio di Update 3|  
|Visual Studio Enterprise (2 senza ulteriori aggiornamenti Update 2-era con aggiornamento originale)|Visual Studio Enterprise RTM (disponibile nella [pagina di download per i titolari di abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/downloads/))|`vs_enterprise.exe /OverrideFeedURI http://download.microsoft.com/download/0/6/B/06BB0C5C-C767-4250-91DA-AB463377597E/20160405.3/enu/feed.xml`|Installazione di Visual Studio userà il file feed. XML disponibile al rilascio di Update 2|  
|Visual Studio Enterprise Update 1 (originale aggiornamento 1, ma con aggiornamenti che pre-aggiornamento di Update 2)|Visual Studio Enterprise RTM (disponibile nella [pagina di download per i titolari di abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/downloads/))|`vs_enterprise.exe /OverrideFeedURI http://download.microsoft.com/download/3/2/A/32A1974F-D236-43C1-8981-97DDCBAEF14A/20160225.3/enu/feed.xml`|Installazione di Visual Studio userà il file feed. XML corrente prima del rilascio dell'aggiornamento 2|  
|Visual Studio Enterprise Update 1 (Update 1 originale senza aggiornamenti aggiuntivi relativi a Update 1)|Visual Studio Enterprise RTM (disponibile nella [pagina di download per i titolari di abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/downloads/))|`vs_enterprise.exe /OverrideFeedURI https://download.microsoft.com/download/3/2/A/32A1974F-D236-43C1-8981-97DDCBAEF14A/20151201.1/enu/feed.xml`|Installazione di Visual Studio userà il file feed. XML disponibile al rilascio di Update 1|  
|Visual Studio Enterprise (RTM originale, ma con aggiornamenti precedenti a Update 1)|Visual Studio Enterprise RTM (disponibile nella  [pagina di download per i titolari di abbonamenti MSDN](https://msdn.microsoft.com/en-us/subscriptions/downloads/))|`vs_enterprise.exe /OverrideFeedURI https://download.microsoft.com/download/3/6/1/36188D5F-479F-4A46-BF55-6AE5928D1EBB/20151102.3/enu/feed.xml`|L'installazione di Visual Studio userà il file feed.xml corrente prima del rilascio di Update 1.|  
|Visual Studio Enterprise (RTM originale, senza aggiornamenti)|Visual Studio Enterprise RTM (disponibile nella [pagina di download per i titolari di abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/downloads/))|`vs_enterprise.exe /OverrideFeedURI https://download.microsoft.com/download/5/7/B/57BF5016-E4F0-4EB5-BE27-2BFA87E7723F/20150713.1/enu/feed.xml`|Installazione di Visual Studio userà il file feed. XML disponibile al rilascio RTM|  
  
> [!IMPORTANT]
>  In base alla lingua da usare, sostituire "enu" (per inglese) con uno dei valori seguenti:  
>   
>  -   chs (per cinese (semplificato))  
> -   cht (per cinese (tradizionale))  
> -   csy (per ceco)  
> -   deu (per tedesco)  
> -   esn (per spagnolo)  
> -   fra (per francese)  
> -   ita (per italiano)  
> -   jpa (per giapponese)  
> -   kor (per coreano)  
> -   plk (per polacco)  
> -   ptb (per portoghese)  
> -   rus (per russo)  
> -   trk (per turco)  
  
## <a name="see-also"></a>Vedere anche  
 [Guida di Visual Studio Administrator](../install/visual-studio-administrator-guide.md)