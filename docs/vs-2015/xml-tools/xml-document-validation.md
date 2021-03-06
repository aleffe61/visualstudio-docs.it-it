---
title: Convalida di documenti XML | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: abb353bd-6c4a-4978-b03b-a8c245bbfb55
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4b765efcfc01384a14bba6eb46cbaadd915e7752
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49914268"
---
# <a name="xml-document-validation"></a>Convalida di documenti XML
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
L'editor XML verifica la sintassi XML 1.0 ed esegue inoltre la convalida dei dati durante la digitazione. L'editor può eseguire la convalida tramite una DTD (Document Type Definition) o uno schema. Le sottolineature ondulate di colore rosso evidenziano gli errori di formato del codice XML 1.0. Le sottolineature ondulate di colore blu mostrano gli errori di semantica rilevati sulla base della DTD o della convalida dello schema. A ciascun errore è associata una voce nell'elenco degli errori. È possibile inoltre visualizzare il messaggio di errore posizionando per qualche istante il puntatore del mouse sulla sottolineatura ondulata.  
  
 Gli schemi usati nella convalida vengono individuati confrontando il `targetNamespace` di uno schema compilato con la dichiarazione xmlns dell'elemento. Gli schemi compilati vengono caricati da una delle seguenti posizioni, elencate in ordine di priorità:  
  
- Il nome del file specificato nella **schemi** campo della finestra delle proprietà del documento.  
  
- Schema inline o DTD.  
  
- Una DTD esterna o un attributo `xsd:schemaLocation` e `xsd:noNamespaceSchemaLocation`  
  
- Un URI dello spazio dei nomi dello schema XDR "x-schema".  
  
  Gli schemi possono essere rilevati anche nelle seguenti posizioni aggiuntive quando lo schema dispone di uno spazio dei nomi di destinazione non vuoto:  
  
- Un'altra finestra dell'editor contenente lo schema.  
  
- Uno schema nella soluzione corrente.  
  
- Uno schema dalla directory della cache degli schemi.  
  
## <a name="xslt-files"></a>File XSLT  
 Quando si modifica un file XSLT, viene usato per la convalida il file xslt.xsd che si trova nella cache degli schemi. Gli errori di convalida vengono visualizzati con una sottolineatura ondulata di colore blu. Gli errori del compilatore XSLT vengono visualizzati con una sottolineatura ondulata di colore rosso.  
  
## <a name="xml-schema-xsd-files"></a>File XSD (XML Schema)  
 Quando si modifica un file di schema XML, viene usato per la convalida il file xsdschema.xsd che si trova nella cache degli schemi. Gli errori di convalida vengono visualizzati con una sottolineatura ondulata di colore blu. Anche gli errori di compilazione vengono visualizzati con una sottolineatura ondulata di colore rosso.  
  
## <a name="see-also"></a>Vedere anche  
 [Editor XML](../xml-tools/xml-editor.md)



