---
title: 'Procedura: Impostare le informazioni di configurazione per una soluzione Office'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- solutions [Office development in Visual Studio], configuration files
- configuration files [Office development in Visual Studio]
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: a97ad1147a109723ffcededf485ed7865e0697f9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53916640"
---
# <a name="how-to-set-up-configuration-information-for-an-office-solution"></a>Procedura: Impostare le informazioni di configurazione per una soluzione Office
  È possibile utilizzare i file di configurazione per configurare le impostazioni specifiche per le soluzioni Office. È possibile specificare le impostazioni come criteri di associazione degli assembly, gli oggetti di .NET remoting, debug e le impostazioni di traccia.  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]  
  
### <a name="to-add-a-configuration-file-to-your-office-project"></a>Per aggiungere un file di configurazione al progetto di Office  
  
1. Nel menu **Progetto** fare clic su **Aggiungi nuovo elemento**.  
  
2. Nel **categorie** riquadro, fare clic su **generali**.  
  
3. Nel **modelli** riquadro, selezionare **File di configurazione dell'applicazione**.  
  
4. Nel **Name** , digitare lo stesso nome dell'assembly con l'estensione *config*. Ad esempio, un file di configurazione per assembly di un progetto denominato *ExcelWorkbook1.dll* verrebbe denominata *Excelworkbook1*.  
  
5. Fare clic su **Aggiungi**.  
  
6. Creare il file di configurazione in base allo schema di file di configurazione dell'applicazione. Per altre informazioni, vedere [schema di file di configurazione per .NET Framework](/dotnet/framework/configure-apps/file-schema/index).  
  
   Non esistono considerazioni speciali per l'uso di file di configurazione con i progetti di Office.  
  
## <a name="see-also"></a>Vedere anche  
 [Schema di file di configurazione per .NET Framework](/dotnet/framework/configure-apps/file-schema/index)   
 [Progettare e creare soluzioni Office](../vsto/designing-and-creating-office-solutions.md)   
 [Distribuire una soluzione Office](../vsto/deploying-an-office-solution.md)  
