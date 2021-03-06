---
title: Scheda spazio, finestra di dialogo Proprietà processo | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: c4de1866-7447-48f7-aa88-28ad92c0b930
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2cab2263da44ba46d7fbbe301f61e51b5308ba73
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51767436"
---
# <a name="space-tab-process-properties-dialog-box"></a>Scheda Spazio, finestra di dialogo Proprietà processo
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Usare la **spazio** pressione di tab per esaminare lo spazio degli indirizzi di un processo. Per visualizzare il [finestra di dialogo Proprietà processo](../debugger/process-properties-dialog-box.md), spostare lo stato attivo su un [visualizzazione processi](../debugger/processes-view.md) finestra. Selezionare qualsiasi nodo del processo nell'albero e quindi scegliere **delle proprietà** dalle **visualizzazione** menu.  
  
 Le impostazioni seguenti sono disponibili sul **spazio** scheda:  
  
|Voce|Descrizione|  
|-----------|-----------------|  
|**Mostra per lo spazio di memoria**|Utilizzare questa casella di riepilogo per selezionare la categoria di spazio (immagine, il mapping, riservati o non assegnati).|  
|**Byte eseguibili**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi che usa questo processo. File eseguibile è la memoria che possono essere eseguita da programmi, ma potrebbe non essere letto o scritta.|  
|**Exec-byte sola lettura**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi in uso con le proprietà di sola lettura che utilizza questo processo. Exec-sola lettura è la memoria che può essere eseguita, nonché leggere.|  
|**Byte Exec-lettura-scrittura**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi in uso con le proprietà di lettura / scrittura che usa questo processo. Exec-lettura-scrittura è la memoria che può essere eseguita dai programmi, nonché leggere e modificata.|  
|**Byte copia / scrittura Exec**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi che può essere l'esecuzione dei programmi, nonché leggere e scritta. Questo tipo di protezione viene utilizzato quando la memoria deve essere condivisa tra processi. Se i processi di condivisione lettura solo la memoria, quindi tutti usino la stessa memoria. Se dei processi richiede l'accesso in scrittura, verrà creata una copia di tale memoria per il processo.|  
|**Byte senza accesso**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi che impedisce l'uso di un processo. Se la scrittura, viene generata una violazione di accesso o si tenta di leggere.|  
|**Byte sola lettura**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi che può essere eseguita, nonché leggere.|  
|**Byte lettura / scrittura**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi che consente la lettura e scrittura.|  
|**Byte copia / scrittura**|Per la categoria selezionata, la somma di tutto lo spazio di indirizzi che consente la condivisione della memoria per la lettura, ma non per la scrittura. Quando si leggono questa memoria processi, possono condividere la stessa memoria. Tuttavia, quando un processo di condivisione deve avere accesso in lettura/scrittura alla memoria condivisa, viene creata una copia di tale memoria per la scrittura.|



