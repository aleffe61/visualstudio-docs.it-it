---
title: '&lt;postActionData&gt; elemento (sviluppo per Office in Visual Studio)'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- <postActionData> element
- application manifests [Office development in Visual Studio], <postActionData> element
- postActionData element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: f27cf59f157c0760ea0c204a8c079dd4616777da
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947270"
---
# <a name="ltpostactiondatagt-element-office-development-in-visual-studio"></a>&lt;postActionData&gt; elemento (sviluppo per Office in Visual Studio)
  L'elemento `postActionData` dello spazio dei nomi `vstav3` specifica i dati associati a qualsiasi azione post-distribuzione che viene eseguita dopo l'installazione di soluzioni Office.

## <a name="syntax"></a>Sintassi

```xml
<postActionData>
</postActionData>
```

## <a name="elements-and-attributes"></a>Gli elementi e attributi
 L'elemento `postActionData` è facoltativo e si trova nello spazio dei nomi `vstav3` . Per ogni azione post-distribuzione è definito un elemento `postActionData` in un manifesto dell'applicazione.

 L'elemento `postActions` non ha attributi.

 `postActions` è privo di elementi figlio.

## <a name="post-deployment-action-example"></a>Esempio di azione post-distribuzione

### <a name="description"></a>Descrizione
 L'esempio di codice seguente illustra l'elemento `postAction` in un manifesto dell'applicazione per una soluzione Office distribuita con [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Questo esempio di codice è parte di un esempio più esaustivo disponibile nel [manifesti dell'applicazione per le soluzioni Office](../vsto/application-manifests-for-office-solutions.md).

### <a name="code"></a>Codice

```xml
<vstav3:postActionData>
  data in any format
</vstav3:postActionData>
```

## <a name="see-also"></a>Vedere anche

- [Manifesti dell'applicazione per le soluzioni Office](../vsto/application-manifests-for-office-solutions.md)
- [Manifesti della distribuzione per le soluzioni Office](../vsto/deployment-manifests-for-office-solutions.md)
- [Manifesto dell'applicazione ClickOnce](../deployment/clickonce-application-manifest.md)
