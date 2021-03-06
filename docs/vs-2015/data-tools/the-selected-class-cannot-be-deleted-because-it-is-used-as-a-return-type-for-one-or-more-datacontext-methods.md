---
title: La classe selezionata non può essere eliminata perché è usato come tipo restituito per uno o più metodi DataContext | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: d68254a0-f3a1-47e2-aed3-a83471e1d711
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 084843636d62bd7d85c5bbc141aa0fe8ddf81462
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49236262"
---
# <a name="the-selected-class-cannot-be-deleted-because-it-is-used-as-a-return-type-for-one-or-more-datacontext-methods"></a>Impossibile eliminare la classe selezionata perché è utilizzata come tipo restituito per uno o più metodi DataContext
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Il tipo restituito di uno o più metodi <xref:System.Data.Linq.DataContext> rappresenta la classe di entità selezionata. L'eliminazione di una classe di entità usata come tipo restituito di un metodo <xref:System.Data.Linq.DataContext> determinerà l'esito negativo della compilazione del progetto. Per eliminare la classe di entità selezionata, identificare i metodi <xref:System.Data.Linq.DataContext> che l'usano e impostare i relativi tipi restituiti su una classe di entità diversa.  
  
 Per ripristinare i tipi restituiti dei <xref:System.Data.Linq.DataContext> metodi nei tipi generati automaticamente originali, eliminare prima il <xref:System.Data.Linq.DataContext> metodo dal riquadro dei metodi e quindi trascinare l'oggetto dalla **Esplora Server** / **Database Explorer** in nuovamente la finestra di Progettazione relazionale oggetti.  
  
### <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Identificare <xref:System.Data.Linq.DataContext> metodi che usano la classe di entità come tipo restituito selezionando un <xref:System.Data.Linq.DataContext> metodo nei metodi riquadro ed esaminando il **Return Type** proprietà nel **proprietà** finestra .  
  
2.  Impostare il **Return Type** a una classe di entità diverso o eliminare il <xref:System.Data.Linq.DataContext> metodo dal riquadro dei metodi.  
  
## <a name="see-also"></a>Vedere anche  
 [Strumenti LINQ to SQL in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [Procedura dettagliata: Creazione di classi LINQ to SQL (O-R Designer)](http://msdn.microsoft.com/library/35aad4a4-2e8a-46e2-ae09-5fbfd333c233)   
 [Metodi DataContext (O/R Designer)](../data-tools/datacontext-methods-o-r-designer.md)   
 [Procedura: Modificare il tipo restituito di un metodo DataContext (O/R Designer)](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md)

