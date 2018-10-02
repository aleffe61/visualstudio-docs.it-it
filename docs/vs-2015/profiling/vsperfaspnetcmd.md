---
title: VSPerfASPNetCmd | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- profiling tools,VSPerfASPNETCmd
- VSPerfASPNETCmd
ms.assetid: f9e9f895-57bb-41e8-8bd1-cdaa738ec220
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a074edba64f9742f9761754279be35f5c621be2b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519189"
---
# <a name="vsperfaspnetcmd"></a>VSPerfASPNetCmd
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [VSPerfASPNetCmd](https://docs.microsoft.com/visualstudio/profiling/vsperfaspnetcmd).  
  
Lo strumento della riga di comando **VSPerfASPNetCmd.exe** consente di profilare i siti Web ASP.Net senza la necessità di impostare le variabili di ambiente o di riavviare il computer. Uso **VSPerfASPNetCmd.exe** invece di [VSPerfCmd](../profiling/vsperfcmd.md) quando si esegue la profilatura siti Web ASP.NET e non è necessaria la funzionalità aggiuntiva fornita da **VSPerCmd**. Per altre informazioni su **VSPerfASPNetCmd**, vedere [Profilatura rapida di sito Web con VSPerfASPNETCmd](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md). **VSPerfASPNetCmd** è lo strumento della riga di comando preferito da usare quando si usa il profiler autonomo per profilare un sito Web ASP.NET.  
  
## <a name="syntax"></a>Sintassi  
 **vsperfaspnetcmd** [*/Options*] *Website*  
  
## <a name="options"></a>Opzioni  
  
|Opzione|Descrizione|  
|------------|-----------------|  
|**/Sample** o **/s**|Esegue la profilatura del sito Web tramite il metodo di campionamento. **/Sample** è il metodo predefinito. /Sample non può essere usato con **/Trace**.|  
|**/Trace** o **/t**|Sottoporre a profilatura il sito Web tramite il metodo di strumentazione. /Trace non può essere usato con **/Sample**.|  
|**/Memory**[**:**`Type`] o **/m**[**:**{**un**& #124; **l**}]|I profili di allocazione della memoria e, facoltativamente, i profili della durata degli oggetti (garbage collection). **/Memory** può essere usato con il metodo di campionamento o di strumentazione.<br /><br /> *Tipo* può essere uno dei seguenti:<br /><br /> -   **allocazione** (o **a**) raccoglie solo i dati sull'allocazione della memoria.<br />-   **durata** (o **l**) raccoglie i dati sull'allocazione della memoria e quelli sulla durata dell'oggetto.<br /><br /> Il valore predefinito `Type` è **allocazione**.|  
|**/Tip** o   **/i**|Aggiunge una richiesta ASP.NET dettagliata e informazioni sulla chiamata ADO.NET ai dati relativi alla profilatura. **/ Tip** può essere usato con il metodo campionamento o di strumentazione e può essere usato con l'opzione **/Memory**.|  
|**/ Output:** `File` o **/o:**`File`|Specifica il percorso e il nome del file dei dati di profilatura (con estensione vsp).|  
|**/NoWait** o   **/n**|Restituisce il prompt dei comandi immediatamente in modo che i comandi aggiuntivi possano essere usati nella finestra del prompt dei comandi. È necessario digitare **VSPerfASPNETCmd /Shutdown** su una riga di comando separata per disattivare la profilatura.|  
|**/PackSymbols**[:{**on**&#124;**off**}o   **/p**[:{**on**&#124;**off**}|Incorpora simboli (nomi di funzione e di parametro e così via) nel file di dati di profilatura (con estensione .vsp).|  
|**/Shutdown:** `Website`o   **/d:**`Website`|Disattiva la profilatura. Usare come unica opzione in una riga di comando dopo aver usato l'opzione **/NoWait** per avviare la profilatura, o se il profiler termina in modo imprevisto. Specificare lo stesso url usato nel comando originale **VSPerfASPNETCmd**.|  
|`Website`|L'url del sito Web da profilare.|  
  
## <a name="see-also"></a>Vedere anche  
 [Profilatura rapida del sito Web con VSPerfASPNETCmd](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md)   
 [Profilatura di applicazioni Web ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)


