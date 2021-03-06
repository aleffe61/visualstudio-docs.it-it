---
title: 'Procedura: Creare una Web Part di SharePoint | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Web Parts [SharePoint development in Visual Studio], adding
- Web Parts [SharePoint development in Visual Studio], creating
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 43d776a4031cabfd027c96105f3e71a93ea1c07f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53858423"
---
# <a name="how-to-create-a-sharepoint-web-part"></a>Procedura: Creare una web part di SharePoint
  È possibile creare e personalizzare una web part aggiungendo un **Web Part** voce a qualsiasi progetto SharePoint e quindi modificando il file di codice per la web part o tramite una finestra di progettazione. Per altre informazioni, vedere [Procedura: Creare una web part di SharePoint usando una finestra di progettazione](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md).  
  
### <a name="to-create-a-sharepoint-web-part"></a>Per creare una web part di SharePoint
  
1.  Creare o aprire un progetto SharePoint.  
  
     Per altre informazioni, vedere [SharePoint modelli di elemento di progetto e progetto](../sharepoint/sharepoint-project-and-project-item-templates.md).  
  
2.  Scegliere il nodo del progetto SharePoint in **Esplora soluzioni** e quindi scegliere **Project** > **Aggiungi nuovo elemento**.  
  
3.  Nel **Aggiungi nuovo elemento** finestra di dialogo espandere il **SharePoint** nodo e quindi scegliere il **2010** nodo.  
  
4.  Nell'elenco dei modelli di SharePoint, scegliere **Web Part**.  
  
5.  Nel **Name** casella, specificare un nome per la web part e quindi scegliere il **Add** pulsante.  
  
     La web part viene visualizzata **Esplora soluzioni**. Per altre informazioni sui file che include una web part, vedere [creazione di web part per SharePoint](../sharepoint/creating-web-parts-for-sharepoint.md).  
  
6.  Nelle **Esplora soluzioni**, aprire il file di codice per la web part appena creata.  
  
     Ad esempio, se il nome della web part *WebPart1*aprire *WebPart1.vb* (in Visual Basic) o *WebPart1.cs* (in c#).  
  
7.  Nel file di codice aggiungere controlli al metodo <xref:System.Web.UI.Control.CreateChildControls%2A>.  
  
     Per un esempio, vedere [procedura dettagliata: Creare una web part per SharePoint](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint.md).  
  
## <a name="see-also"></a>Vedere anche
 [Creazione di web part per SharePoint](../sharepoint/creating-web-parts-for-sharepoint.md)   
 [Procedura: Creare una web part di SharePoint usando una finestra di progettazione](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md)   
 [Procedura dettagliata: Creare una web part per SharePoint](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint.md)   
 [Procedura dettagliata: Creare una web part per SharePoint tramite una finestra di progettazione](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint-by-using-a-designer.md)  
