---
title: Creazione di un'estensione con una finestra degli strumenti | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 585b0a3a-f85b-4f92-81bb-9ca499bb8a89
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7e21c49971660f32abef3a47e436d01e5af05543
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53838992"
---
# <a name="create-an-extension-with-a-tool-window"></a>Creare un'estensione con una finestra degli strumenti
In questa procedura descrive come usare il modello di progetto VSIX e il **finestra degli strumenti personalizzata** modello di elemento per creare un'estensione con una finestra degli strumenti.  
  
## <a name="prerequisites"></a>Prerequisiti  
 A partire da Visual Studio 2015, non installare Visual Studio SDK dall'area download. È incluso come funzionalità facoltativa nel programma di installazione di Visual Studio. È anche possibile installare il SDK di Visual Studio in un secondo momento. Per altre informazioni, vedere [installare Visual Studio SDK](../extensibility/installing-the-visual-studio-sdk.md).  
  
### <a name="create-a-tool-window"></a>Creare una finestra degli strumenti  
  
1.  Creare un progetto VSIX denominato **FirstWindow**. È possibile trovare il modello di progetto VSIX nel **nuovo progetto** nella finestra di dialogo **Visual c#** > **estendibilità**.  
  
2.  Quando si apre il progetto, aggiungere un modello di elemento di finestra degli strumenti denominato **MyWindow**. Nel **Esplora soluzioni**, fare doppio clic sul nodo del progetto e selezionare **Add** > **nuovo elemento**. Nel **Aggiungi nuovo elemento** finestra di dialogo passa alla **Visual c#** > **Extensibility** e selezionare **finestra degli strumenti personalizzata**. Nel **Name** campo nella parte inferiore della finestra, modificare il nome file della finestra degli strumenti per *MyWindow.cs*.  
  
3.  Compilare il progetto e avviare il debug.  
  
     Viene visualizzata l'istanza sperimentale di Visual Studio. Per altre informazioni sull'istanza sperimentale, vedere [l'istanza sperimentale](../extensibility/the-experimental-instance.md).  
  
4.  Nell'istanza sperimentale, passare a **View** > **Other Windows**.  
  
     Una voce di menu per dovrebbe **MyWindow**. Fare clic.  
  
     Si dovrebbe essere una finestra degli strumenti con il titolo **MyWindow** che indica che un pulsante e **Click Me!.**