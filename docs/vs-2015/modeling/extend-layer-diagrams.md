---
title: Estendere i diagrammi livello | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-techdebt
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- layer diagrams, creating extensions
- layer models
ms.assetid: 83fca301-b008-485a-87eb-218050e71451
caps.latest.revision: 41
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 20d84c91ef30ae549b8fa59893d439a06467ed33
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51766921"
---
# <a name="extend-layer-diagrams"></a>Extend layer diagrams
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

È possibile scrivere codice per creare e aggiornare i diagrammi livello e per convalidare la struttura del codice programma in base ai diagrammi livello in Visual Studio. È possibile aggiungere comandi da visualizzare nel menu di scelta rapida (contestuale) dei diagrammi, personalizzare i movimenti di trascinamento della selezione e accedere al modello di livello dai modelli di testo. È possibile creare un pacchetto di queste estensioni in un progetto VSIX (Visual Studio Integration Extension) e distribuirle ad altri utenti di Visual Studio.  
  
 Per altre informazioni sui diagrammi livello, vedere:  
  
-   [Diagrammi livello: riferimento](../modeling/layer-diagrams-reference.md)  
  
-   [Diagrammi livello: linee guida](../modeling/layer-diagrams-guidelines.md)  
  
-   [Creare diagrammi livello dal codice](../modeling/create-layer-diagrams-from-your-code.md)  
  
-   [Convalidare il codice con diagrammi livello](../modeling/validate-code-with-layer-diagrams.md)  
  
##  <a name="prereqs"></a> Requisiti  
 È necessario verificare che nel computer in cui si vogliono sviluppare le estensioni del livello sia installato quanto segue:  
  
- Visual Studio  
  
- [Visual Studio SDK](../extensibility/visual-studio-sdk.md)  
  
- [Modeling SDK per Visual Studio 2015](http://www.microsoft.com/download/details.aspx?id=48148)  
  
  È necessario avere installato una versione appropriata di Visual Studio nel computer in cui si vogliono eseguire le estensioni del livello. Per altre informazioni, vedere [distribuire un'estensione del modello di livello](../modeling/deploy-a-layer-model-extension.md).  
  
  Per individuare le versioni di Visual Studio che supportano i diagrammi livello, vedere [Version support for architecture and modeling tools](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).  
  
## <a name="in-this-section"></a>In questa sezione  
 [Aggiunta di comandi e movimenti a diagrammi livello](../modeling/add-commands-and-gestures-to-layer-diagrams.md)  
  
 [Aggiungere strumenti di convalida dell'architettura personalizzati a diagrammi livello](../modeling/add-custom-architecture-validation-to-layer-diagrams.md)  
  
 [Aggiungere proprietà personalizzate ai diagrammi livello](../modeling/add-custom-properties-to-layer-diagrams.md)  
  
 [Esplorare e aggiornare i modelli di livello nel codice del programma](../modeling/navigate-and-update-layer-models-in-program-code.md)  
  
 [Distribuire un'estensione del modello di livello](../modeling/deploy-a-layer-model-extension.md)  
  
 [Risoluzione dei problemi relativi a estensioni per diagrammi livello](../modeling/troubleshoot-extensions-for-layer-diagrams.md)  
  
## <a name="see-also"></a>Vedere anche  
 [Definire e installare un'estensione di modellazione](../modeling/define-and-install-a-modeling-extension.md)   
 [Diagrammi livello: riferimento](../modeling/layer-diagrams-reference.md)   
 [Diagrammi livello: linee guida](../modeling/layer-diagrams-guidelines.md)   
 [Creare diagrammi livello dal codice](../modeling/create-layer-diagrams-from-your-code.md)   
 [Convalidare il codice con diagrammi livello](../modeling/validate-code-with-layer-diagrams.md)   
 [Generare file da un modello UML](../modeling/generate-files-from-a-uml-model.md)   
 [Aprire un modello UML tramite l'API di Visual Studio](../modeling/open-a-uml-model-by-using-the-visual-studio-api.md)



