---
title: 'Procedura: Eseguire la ricerca a livello di codice per un indirizzo di posta elettronica nei contatti'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- e-mail [Office development in Visual Studio], searching
- contacts [Office development in Visual Studio], searching
- searching contacts
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 767c75bff42bc19b70d4b6dcd35da16c4bb4c099
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53893354"
---
# <a name="how-to-programmatically-search-for-an-email-address-in-contacts"></a>Procedura: Eseguire la ricerca a livello di codice per un indirizzo di posta elettronica nei contatti
  Questo esempio cerca una cartella Contatti per i contatti con il nome dominio **example.com** nei relativi indirizzi di posta elettronica.  
  
 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]  
  
## <a name="example"></a>Esempio  
 [!code-csharp[Trin_OL_SearchEmail#1](../vsto/codesnippet/CSharp/Trin_OL_SearchEmail/thisaddin.cs#1)]  
  
## <a name="compile-the-code"></a>Compilare il codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Contatti con il nome dominio **example.com** nei relativi indirizzi di posta elettronica (ad esempio, `somebody@example.com`) e con il nome e il cognome.  
  
## <a name="see-also"></a>Vedere anche  
 [Lavorare con gli elementi di contatto](../vsto/working-with-contact-items.md)   
 [Procedura: A livello di codice Invia messaggio di posta elettronica](../vsto/how-to-programmatically-send-e-mail-programmatically.md)   
 [Procedura: Accedere a livello di codice ai contatti di Outlook](../vsto/how-to-programmatically-access-outlook-contacts.md)   
 [Procedura: A livello di codice aggiungere una voce ai contatti di Outlook](../vsto/how-to-programmatically-add-an-entry-to-outlook-contacts.md)  
