---
title: 'Estensione Excel di esempio: classe ExtensionPackage | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6e45410a-1819-4d54-ac21-7280152f7e3a
caps.latest.revision: 11
ms.author: gewarren
manager: douge
ms.openlocfilehash: 64e6d838172325bb00cdd8a28ef6adb6d1a345b5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49286013"
---
# <a name="sample-excel-extension-extensionpackage-class"></a>Estensione Excel di esempio: classe ExtensionPackage
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Questa classe estende la classe <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage> e offre il punto di ingresso per un test codificato dell'interfaccia utente per un foglio di lavoro di [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)].  
  
## <a name="assembly-attribute"></a>Attributo Assembly  
 Il file inizia con un attributo Assembly che identifica l'assembly come un'estensione di test dell'interfaccia utente.  
  
```  
[assembly: Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage(  
    "ExcelExtensionPackage",  
    typeof(  
     Microsoft.VisualStudio.Test.Sample.UI.ExtensionPackage))]  
```  
  
 Questo attributo dichiara il nome della classe di base, il nome della classe del pacchetto e il nome completo della classe per la classe del pacchetto di estensione personalizzato.  
  
## <a name="simple-properties"></a>Proprietà semplici  
 Questa classe dispone di proprietà che forniscono i valori usati dal framework dei test codificati dell'interfaccia utente per identificare e descrivere l'estensione e l'assembly. Per altre informazioni, vedere i commenti del codice.  
  
## <a name="getservice-method"></a>Metodo GetService  
 Il metodo <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage.GetService%2A> è il singolo punto di ingresso usato dal framework dei test codificati dell'interfaccia utente per accedere al gestore della tecnologia, al provider di proprietà e al filtro delle azioni, come identificato dalla classe di base per ogni oggetto.  
  
## <a name="see-also"></a>Vedere anche  
 <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage>   
 [Estensione di test codificati dell'interfaccia utente e registrazioni delle azioni per supportare Microsoft Excel](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)



