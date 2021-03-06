---
title: Distribuzione dei tipi di progetto | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], managed-code
- projects [Visual Studio SDK], aggregator
ms.assetid: 7f132f67-8589-464c-90dc-0d57ae02aa8f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 358ab66ecf1f3602ce37f85de803bd8953771858
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53892137"
---
# <a name="deploy-project-types"></a>Distribuire i tipi di progetto
[!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] Installa un nuovo Sil aggregator tipo di progetto (*ProjectAggregator2. dll*) e anche un pacchetto Windows Installer per la ridistribuzione (*ProjectAggregator2.msi*). È necessario usare il nuovo Sil aggregator per i tipi di progetto di codice gestito. ProjectAggregator2 consente di ovviare ai limiti di [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] progetto Sil aggregator che impedisce che i tipi di progetto di codice gestito funziona correttamente. I passaggi seguenti descrivono come modificare il pacchetto VSPackage per usare al nuovo Sil aggregator.  
  
1.  Rimuovere il progetto NativeHierarchyWrapper dalla soluzione.  
  
2.  Rimuovere eventuali file binari NativeHierarchyWrapper dalla configurazione.  
  
3.  Aggiungere *ProjectAggregator2.msi* alla propria configurazione.