---
title: "Procedura: Definire un'istanza del metodo | Microsoft Docs"
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], method instance
- BDC [SharePoint development in Visual Studio], method instance
- BDC [SharePoint development in Visual Studio], method
- Business Data Connectivity service [SharePoint development in Visual Studio], method
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 84a03fe6066911b12ba0e5a413ea3521033bc283
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53952563"
---
# <a name="how-to-define-a-method-instance"></a>Procedura: Definire un'istanza del metodo
  Nel modello, è necessario definire almeno un'istanza di metodo per ogni metodo.  
  
 Aggiungere un'istanza del metodo usando il **Dettagli metodo BDC** finestra. Quando si aggiunge l'istanza del metodo, Visual Studio aggiunge un `<MethodInstance>` elemento al codice XML del file modello nel progetto. Per altre informazioni sugli attributi di un `<MethodInstance>` elemento, vedere [MethodInstance](http://go.microsoft.com/fwlink/?LinkID=169282).  
  
### <a name="to-define-a-method-instance"></a>Per definire un'istanza del metodo  
  
1.  Nel **Dettagli metodo BDC** finestra, espandere il nodo di un metodo e quindi espandere il **istanze** nodo.  
  
2.  Nel **aggiungere un'istanza del metodo** casella di riepilogo **Crea istanza Finder**.  
  
     Verrà visualizzata una nuova istanza di metodo sotto il **istanze** nodo.  
  
3.  Nella barra dei menu, scegliere **View** > **finestra proprietà**.  
  
4.  Nel **proprietà** finestra, impostare le proprietà dell'istanza del metodo. Per altre informazioni su ogni proprietà, vedere [MethodInstance](http://go.microsoft.com/fwlink/?LinkID=169282).  
  
## <a name="see-also"></a>Vedere anche
 [Panoramica degli strumenti di progettazione modello di integrazione applicativa dei dati](../sharepoint/bdc-model-design-tools-overview.md)   
 [Procedura: Aggiungere un'entità a un modello](../sharepoint/how-to-add-an-entity-to-a-model.md)   
 [Procedura: Aggiungere un parametro a un metodo](../sharepoint/how-to-add-a-parameter-to-a-method.md)   
 [Procedura: Definire il descrittore di tipo di parametro](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md)   
 [Progettare un modello di integrazione applicativa dei dati business](../sharepoint/designing-a-business-data-connectivity-model.md)  
