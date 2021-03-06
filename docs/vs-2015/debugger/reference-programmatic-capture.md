---
title: Riferimento (acquisizione a livello di codice) | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ef60eb8d-1ac2-4e3a-9b4b-f6da0bdd9da8
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 66e80d02ac41d78f2c79e7b2accb11388d456ad8
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51744267"
---
# <a name="reference-programmatic-capture"></a>Riferimento (acquisizione a livello di codice)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Diagnostica grafica supporta il controllo a livello di programmazione sulle funzionalità di acquisizione, tramite l'API di acquisizione a livello di programmazione. È possibile utilizzare questa API per attivare o disattivare e aggiungere messaggi alla diagnostica grafica HUD (Head-Up Display), inizializzare e creare file di log di grafica e acquisire informazioni grafiche.  
  
## <a name="programmatic-capture-apis"></a>API di acquisizione a livello di programmazione  
  
### <a name="classes"></a>Classi  
  
|Nome|Descrizione|  
|----------|-----------------|  
|[VsgDbg Class](../debugger/vsgdbg-class.md)|Rappresenta l'interfaccia attraverso cui il componente in-app di diagnostica della grafica è controllato a livello di programmazione.|  
  
### <a name="preprocessor-symbols"></a>Simboli del preprocessore  
  
|nome|Descrizione|  
|----------|-----------------|  
|[DONT_SAVE_VSGLOG_TO_TEMP](../debugger/dont-save-vsglog-to-temp.md)|Quando presente, definisce se il file di log di grafica viene salvato nella directory dei file temporanei dell'utente.|  
|[VSG_DEFAULT_RUN_FILENAME](../debugger/vsg-default-run-filename.md)|Definisce il nome file predefinito del file di log di grafica.|  
|[VSG_NODEFAULT_INSTANCE](../debugger/vsg-nodefault-instance.md)|Quando presente, definisce se viene fornita un'istanza predefinita della classe `VsgDbg`.|  
  
## <a name="related-articles"></a>Articoli correlati  
  
|Titolo|Descrizione|  
|-----------|-----------------|  
|[Capturing Graphics Information](../debugger/capturing-graphics-information.md)|Viene indicato come acquisire informazioni grafiche dall'app basata su DirectX per poter usare gli strumenti di diagnostica della grafica [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] per diagnosticare problemi di rendering.|  
|[Panoramica](../debugger/overview-of-visual-studio-graphics-diagnostics.md)|Viene indicato come la diagnostica della grafica consente di eseguire il debug degli errori di rendering nei giochi e nelle app DirectX.|



