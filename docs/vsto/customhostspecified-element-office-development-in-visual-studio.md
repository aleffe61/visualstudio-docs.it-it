---
title: '&lt;customHostSpecified&gt; elemento (sviluppo per Office in Visual Studio)'
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <customHostSpecified> element
- <customHostSpecified> element
- customHostSpecified element
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 0880e0ddf4763cf2c67c10871992a24b76f59ef2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53896643"
---
# <a name="ltcustomhostspecifiedgt-element-office-development-in-visual-studio"></a>&lt;customHostSpecified&gt; elemento (sviluppo per Office in Visual Studio)
  Il `customHostSpecified` elemento indica che questa soluzione non è un'applicazione autonoma. Le soluzioni Office contengono componenti che sono ospitati all'interno delle applicazioni Microsoft Office.

## <a name="syntax"></a>Sintassi

```xml
<customHostSpecified />
```

## <a name="elements-and-attributes"></a>Gli elementi e attributi
 Il `customHostSpecified` elemento è obbligatorio per le soluzioni Office. Questo elemento è presente il `co.v1` dello spazio dei nomi e specifica che la distribuzione contiene un componente che verrà distribuito all'interno di un host personalizzato e non è un'applicazione autonoma.

 Questo elemento è figlio del primo `<entrypoint>` elemento nel manifesto dell'applicazione. Non può esistere alcun altri elementi figlio in quanto `<entrypoint>` elemento o [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] genererà un errore di convalida durante l'installazione.

 Questo elemento è non sono presenti attributi ed elementi figlio.

## <a name="example"></a>Esempio
 L'esempio di codice seguente illustra il `customHostSpecified` elemento in un manifesto dell'applicazione per una soluzione Office. Questo esempio di codice è parte di un esempio più esaustivo disponibile nel [manifesti dell'applicazione per le soluzioni Office](../vsto/application-manifests-for-office-solutions.md).

```xml
<entryPoint>
    <co.v1:customHostSpecified />
</entryPoint>
```

## <a name="see-also"></a>Vedere anche

- [Manifesti dell'applicazione per le soluzioni Office](../vsto/application-manifests-for-office-solutions.md)
- [Manifesti della distribuzione per le soluzioni Office](../vsto/deployment-manifests-for-office-solutions.md)
- [Manifesto dell'applicazione ClickOnce](../deployment/clickonce-application-manifest.md)