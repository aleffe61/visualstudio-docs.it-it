---
title: Panoramica (Debug Interface Access SDK) | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- user-defined types
- .dbg files
- modules
- interfaces [DIA SDK]
- DBG files
- procedures [DIA SDK]
- executable files
- COM objects, in DIA SDK
- compilands
- executable images
ms.assetid: 720b4479-a8bc-4fec-860e-80c1a0780405
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5076ea7eee1c762ac42d92482e20ef43e5c224a0
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51767796"
---
# <a name="overview-debug-interface-access-sdk"></a>Panoramica (Debug Interface Access SDK)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Usare il DIA SDK per accedere alle informazioni di debug di Microsoft. Il DIA SDK fornisce una COM basati su set di API che elimina la necessità di riscrivere il codice ogni volta che Microsoft cambia il formato delle informazioni di debug. Il DIA SDK consente anche di leggere da un set selezionato di versioni precedenti di informazioni di debug, che si trova nel file DBG e PDB generati da [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)] 5.0 e versioni successive.  
  
 Ogni interfaccia in DIA SDK rappresenta un oggetto COM diverso, ad eccezione di dove indicato. Interfacce aggiuntive e pertanto gli oggetti aggiuntivi, vengono creati tramite query esplicita, ad esempio [Idiadatasource](../../debugger/debug-interface-access/idiadatasource-opensession.md) oppure [Findchildren](../../debugger/debug-interface-access/idiasession-findchildren.md), piuttosto che dalla chiamata `QueryInterface` sui puntatori di interfaccia esistente.  
  
## <a name="see-also"></a>Vedere anche  
 [Idiadatasource](../../debugger/debug-interface-access/idiadatasource-opensession.md)   
 [IDiaSession::findChildren](../../debugger/debug-interface-access/idiasession-findchildren.md)



