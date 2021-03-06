---
title: 'Errore: Debug non è&#39;t possibili perché nel sistema è attivato un Debugger del Kernel | Microsoft Docs'
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
- vs.debug.error.kernel_dbg_enabled
dev_langs:
- FSharp
- VB
- CSharp
- C++
- VB
- CSharp
- C++
helpviewer_keywords:
- kernel debugger
ms.assetid: 630a7abd-3303-4aaa-888a-6de3de14bc01
caps.latest.revision: 26
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: eea2e7d8277bc67df75be3d05d907a8bd13c29c5
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51725283"
---
# <a name="error-debugging-isn39t-possible-because-a-kernel-debugger-is-enabled-on-the-system"></a>Errore: Debug non è&#39;t possibili perché nel sistema è attivato un Debugger del Kernel
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Quando si esegue il debug del codice gestito, è possibile che venga visualizzato il seguente messaggio di errore:  
  
```  
Debugging isn't possible because a kernel debugger is enabled on the system  
```  
  
 Questo messaggio viene visualizzato quando si tenta di eseguire il debug di codice gestito:  
  
-   in un sistema [!INCLUDE[win7](../includes/win7-md.md)] o [!INCLUDE[wiprlhext](../includes/wiprlhext-md.md)] avviato in modalità debug.  
  
-   l'applicazione utilizzare CLR versione CLR 2.0, 3.0 o 3.5.  
  
## <a name="solution"></a>Soluzione  
  
#### <a name="to-fix-this-problem"></a>Per risolvere il problema  
  
-   Aggiornare l'applicazione per utilizzare CLR versione 4.0 o 4.5  
  
     -oppure-  
  
-   Disabilitare il debug del kernel ed eseguire il debug in [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
     -oppure-  
  
-   Eseguire il debug con il debugger del kernel anziché [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
     -oppure-  
  
-   Nel debugger del kernel disabilitare le eccezioni in modalità utente.  
  
#### <a name="to-disable-kernel-debugging-in-the-current-session"></a>Per disabilitare il debug del kernel nella sessione corrente  
  
-   Al prompt dei comandi, digitare:  
  
    ```  
    Kdbgctrl.exe -d  
    ```  
  
#### <a name="to-disable-kernel-debugging-for-all-sessions-windows-vista-and-windows-7"></a>Per disabilitare il debug del kernel per tutte le sessioni (Windows Vista e Windows 7)  
  
1.  Al prompt dei comandi, digitare:  
  
    ```  
    bcdedit /debug off   
    ```  
  
2.  Riavviare il computer.  
  
#### <a name="to-disable-kernel-debugging-for-all-sessions-other-windows-operating-systems"></a>Per disabilitare il debug del kernel per tutte le sessioni (altri sistemi operativi Windows)  
  
1.  Individuare Boot. ini nell'unità di sistema (in genere c:\\). Il file boot.ini potrebbe essere nascosto e di sola lettura. Per visualizzarlo, è pertanto necessario utilizzare il seguente comando:  
  
    ```  
    dir /ASH  
    ```  
  
2.  Aprire boot.ini utilizzando Blocco note e rimuovere le seguenti opzioni:  
  
    ```  
    /debug  
    /debugport  
    /baudrate  
    ```  
  
3.  Riavviare il computer.  
  
#### <a name="to-debug-with-the-kernel-debugger"></a>Per eseguire il debug con il debugger del kernel  
  
1.  Se il debugger del kernel è collegato, verrà visualizzato un messaggio che chiede se si desidera continuare a eseguire il debug. Scegliere il pulsante per continuare.  
  
2.  È possibile che venga generata un'eccezione `User break exception(Int 3).`. In questo caso, digitare il seguente comando del debugger del kernel per continuare a eseguire il debug:  
  
     `gn`  
  
## <a name="see-also"></a>Vedere anche  
 [Sicurezza del debugger](../debugger/debugger-security.md)   
 [Debug di codice gestito](../debugger/debugging-managed-code.md)



