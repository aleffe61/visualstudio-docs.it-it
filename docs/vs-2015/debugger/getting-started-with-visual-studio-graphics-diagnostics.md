---
title: Guida introduttiva a diagnostica della grafica di Visual Studio | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 59131181-1caa-4b7f-be4b-e84709634edf
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 08cff13bedd8a53ec5172acd6866a912a38b620c
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47532976"
---
# <a name="getting-started-with-visual-studio-graphics-diagnostics"></a>Guida introduttiva a Diagnostica della grafica di Visual Studio
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [Introduzione a Visual Studio Graphics Diagnostics](https://docs.microsoft.com/visualstudio/debugger/graphics/getting-started-with-visual-studio-graphics-diagnostics).  
  
In questa sezione ci si prepara al primo utilizzo di Diagnostica della grafica, quindi si acquisisce un frame da un'app Direct3D e lo si esamina in Analizzatore grafica.  
  
## <a name="requirements"></a>Requisiti  
 Per usare Diagnostica della grafica in Visual Studio 2015 è necessario disporre di una di queste edizioni:  
  
-   Visual Studio 2015 Enterprise  
  
-   Visual Studio 2015 Professional  
  
-   Visual Studio 2015 Community  
  
 [!INCLUDE[downloadvs](../includes/downloadvs-md.md)]  
  
### <a name="windows-10-prerequisites"></a>Prerequisiti di Windows 10  
 La funzionalità Windows facoltativa *strumenti di grafica* fornisce l'infrastruttura di acquisizione e riproduzione richiesti dalla diagnostica grafica in Windows 10.  
  
 Per informazioni sull'installazione di strumenti di grafica, vedere [installare strumenti di grafica per Windows 10](#InstallGraphicsTools).  
  
### <a name="windows-81-prerequisites"></a>Prerequisiti di Windows 8.1  
 Windows Software Development Kit (SDK) per Windows 8.1 fornisce l'infrastruttura di acquisizione e riproduzione richiesti dalla diagnostica della grafica in Windows 8.1 e supporta lo sviluppo per Windows 8.1 e Windows 8.  
  
 [Scaricare Windows Software Development Kit (SDK) per Windows 8.1](https://msdn.microsoft.com/windows/desktop/bg162891.aspx)  
  
 Per usare un computer di riproduzione remoto che esegue Windows 10 da un computer di sviluppo con Windows 8.1, è necessario installare Windows 10 SDK nel computer di sviluppo e la funzionalità opzionale Strumenti di grafica nel computer di riproduzione.  
  
##  <a name="InstallGraphicsTools"></a> Installare strumenti di grafica per Windows 10  
 In Windows 10, l'infrastruttura di diagnostica della grafica è fornita da una funzionalità facoltativa di Windows denominato *strumenti di grafica*. Questa funzionalità è necessaria per acquisire e riprodurre le informazioni di grafica in Windows 10 indipendentemente dal fatto che l'app acquisita abbia come destinazione una versione precedente di Windows e dalla versione di Direct3D in uso. Si può scegliere di installare la funzionalità di Strumenti di grafica in anticipo; in caso contrario, sarà installata su richiesta al primo avvio di una sessione di Diagnostica grafica da Visual Studio.  
  
#### <a name="to-install-graphics-tools-for-windows-10"></a>Per installare Strumenti di grafica per Windows 10  
  
1.  Nel **avviare** menu, scegliere **impostazioni**. Il **impostazioni** viene visualizzata la finestra.  
  
2.  Nel **le impostazioni** finestra di dialogo, scegliere **System**, quindi selezionare **le app installate** dall'elenco di impostazioni di sistema.  
  
3.  Sul lato destro del **le impostazioni** finestra di dialogo scegliere **Gestisci funzionalità facoltative** sotto **installata l'App e funzionalità**. Il **Gestisci funzionalità facoltative** viene visualizzata la finestra.  
  
4.  Nel **Gestisci funzionalità facoltative** finestra di dialogo, scegliere **aggiungere una funzionalità**. Viene visualizzato un elenco di funzionalità facoltative che è possibile installare.  
  
5.  Selezionare **strumenti di grafica** nell'elenco delle funzionalità, quindi scegliere **installare**.  
  
 La funzionalità Strumenti di grafica viene inoltre installata automaticamente quando si installa Windows SDK 10.  
  
> [!TIP]
>  La funzionalità facoltativa strumenti di grafica di Windows 10 fornisce la funzionalità caricamento leggero di acquisizione e riproduzione, ad esempio il programma di acquisizione da riga di comando **dxcap.exe**, che può essere utilizzato nel supporto, test e scenari di diagnostica in macchine virtuali in cui non sono installati gli strumenti di sviluppo. Per altre informazioni, vedere la [strumento di acquisizione da riga di comando](../debugger/command-line-capture-tool.md) argomento.  
  
## <a name="using-graphics-diagnostics-for-the-first-time"></a>Primo utilizzo di Diagnostica della grafica  
 Ora che si dispone di tutto il necessario, è possibile iniziare a usare Diagnostica della grafica eseguendo le operazioni descritte nei passaggi seguenti.  
  
### <a name="1---create-a-direct3d-app"></a>1 - Creare un'app Direct3D  
 Se si dispone già di un'app Direct3D con cui esplorare Diagnostica della grafica, passare al punto successivo. In caso contrario, si può usare uno degli esempi di Direct3D disponibili in Code Gallery.  
  
-   Per provare diagnostica della grafica con Direct3D 12 su Windows 10 usando Visual Studio 2015, provare il [esempio Direct3D 12 UAP](https://code.msdn.microsoft.com/Direct3D-12-UAP-Sample-ecb1779f) per Windows 10.  
  
-   Per provare diagnostica della grafica con Direct3D 11 su Windows 10 o Windows 8.1, è possibile usare la **App DirectX (Windows universale)** oppure **App DirectX (Windows 8.1)** modelli di progetto. O, per operazioni più complesse, provare il [esempio di gioco marble maze DirectX](https://code.msdn.microsoft.com/windowsapps/DirectX-Marble-Maze-Game-e4806345) per Windows 8.1.  
  
 Verificare che sia possibile compilare l'applicazione prima di andare avanti.  
  
### <a name="2---start-a-graphics-diagnostics-session"></a>2 - Avviare una sessione di Diagnostica della grafica  
 A questo punto si è pronti per avviare la prima sessione di diagnostica della grafica. In Visual Studio, nel menu principale, scegliere **eseguire il Debug, grafica, avvia diagnostica**, oppure premere **ALT+F5**. L'app viene avviata in Diagnostica della grafica e in Visual Studio vengono visualizzate le finestre della sessione di diagnostica.  
  
> [!IMPORTANT]
>  Se si esegue l'app in Windows 10 e non si è ancora installata la funzionalità facoltativa Strumenti di grafica, verrà richiesto di farlo ora. La funzionalità deve essere installata per poter usare Diagnostica della grafica in Windows 10.  
  
### <a name="3---capture-frames"></a>3 - Acquisire frame  
 Non appena l'app si avvia, è possibile iniziare ad acquisire frame.  
  
##### <a name="to-capture-single-frames"></a>Per acquisire singoli frame  
  
-   In Visual Studio, scegliere il **Acquisisci Frame** della finestra di sessione della barra degli strumenti o alla diagnostica della grafica. Oppure, se l'app ha lo stato attivo, premere **Stamp**.  
  
##### <a name="to-capture-a-sequence-of-frames"></a>Per acquisire una sequenza di frame  
  
-   In Visual Studio, nella finestra della sessione di diagnostica, impostare **frame da acquisire** sul numero di frame da acquisire in sequenza, quindi acquisire la sequenza usando uno dei metodi descritti in precedenza per acquisire singoli frame.  
  
     Per acquisire nuovamente singoli frame, impostare **frame da acquisire** a `1`.  
  
 Al termine dell'acquisizione dei frame sufficiente uscire dall'app o scegliere il **arrestare** pulsante dalla barra degli strumenti grafica o finestra sessione di diagnostica.  
  
### <a name="4--examine-captured-frames-in-the-graphics-analyzer"></a>4 - Esaminare i frame acquisiti in Analizzatore grafica  
 A questo punto si è pronti per esaminare i frame acquisiti. Per iniziare ad analizzare un frame, scegliere il numero del frame da esaminare nella finestra della sessione di diagnostica. Verrà aperto il frame nel **analizzatore grafica**, dove è possibile usare gli strumenti di diagnostica della grafica per esaminare come l'app Usa Direct3D per tenere traccia dei problemi di rendering oppure usare il **analisi dei Frame** dello strumento comprendere le prestazioni.  
  
 Se è stato selezionato frame errato nella finestra della sessione di diagnostica oppure si vuole esaminare un frame diverso, è possibile selezionare un altro da Analizzatore grafica. Nel **destinazione rendering** della scheda della finestra del log di grafica, sotto l'immagine di destinazione di rendering, espandere il **elenco Frame** e quindi scegliere un altro frame da esaminare.  
  
 Per altre informazioni su come usare gli strumenti di Analizzatore grafica tra loro, vedere la [esempi](../debugger/graphics-diagnostics-examples.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Direct3D 12 grafica](http://msdn.microsoft.com/en-us/52094ae3-3b44-4689-9ee7-1ba1b3a779cb)





