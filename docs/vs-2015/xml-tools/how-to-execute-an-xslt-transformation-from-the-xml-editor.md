---
title: "Procedura: eseguire una trasformazione XSLT dall'Editor XML | Microsoft Docs"
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 56a0fe82-5231-487d-8b6e-a08a9b04e0fc
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7899c2c7816d926185958acc1eb9fb2e066a9a16
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47531277"
---
# <a name="how-to-execute-an-xslt-transformation-from-the-xml-editor"></a>Procedura: eseguire una trasformazione XSLT dall'editor XML
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [procedura: eseguire una trasformazione XSLT dall'Editor XML](https://docs.microsoft.com/visualstudio/xml-tools/how-to-execute-an-xslt-transformation-from-the-xml-editor).  
  
  
L'editor XML consente di associare un foglio di stile XSLT a un documento XML, eseguire la trasformazione e visualizzare l'output. L'output risultante dalla trasformazione XSLT viene visualizzato in una nuova finestra del documento.  
  
 Il **Output** proprietà specifica il nome del file per l'output. Se il **Output** proprietà è vuota, viene generato un nome di file nella directory temporanea. L'estensione del file è basata sull'elemento `xsl:output` del foglio di stile e può essere .xml, .txt o .htm.  
  
 Se il **Output** proprietà specifica un nome di file con un file. htm o viene visualizzato in anteprima di estensione. HTML, l'output XSLT usando [!INCLUDE[msCoName](../includes/msconame-md.md)] Internet Explorer. Tutte le altre estensioni di file vengono aperte usando l'editor predefinito scelto da [!INCLUDE[msCoName](../includes/msconame-md.md)] Visual Studio. Ad esempio, se l'estensione del file è .xml, Visual Studio utilizzerà l'editor XML.  
  
### <a name="to-execute-an-xslt-transformation-from-an-xml-document"></a>Per eseguire una trasformazione XSLT da un documento XML  
  
1.  Aprire un documento XML nell'editor XML.  
  
2.  Associare un foglio di stile XSLT al documento XML.  
  
    -   Aggiungere un'istruzione di elaborazione `xml-stylesheet` al documento XML. Ad esempio, aggiungere la seguente riga `<?xml-stylesheet type='text/xsl' href='filename.xsl'?>` al prologo del documento.  
  
         oppure  
  
    -   Aggiungere il foglio di stile XSLT usando la **proprietà** finestra. Nel documento **finestra delle proprietà**, fare clic sul **Sfoglia** pulsante per il **Stylesheet** campo, selezionare il foglio di stile XSLT e fare clic su **aprire**.  
  
3.  Fare clic sul **ShowXSL Output** pulsante il **Editor XML** sulla barra degli strumenti.  
  
    > [!NOTE]
    >  Se al documento XML non è associato alcun foglio di stile, viene visualizzata una finestra di dialogo con la richiesta di specificare il foglio di stile da usare.  
    >   
    >  L'output risultante dalla trasformazione XSLT viene visualizzato in una nuova finestra del documento.  
  
### <a name="to-execute-an-xslt-transformation-from-an-xslt-style-sheet"></a>Per eseguire una trasformazione XSLT da un foglio di stile XSLT  
  
1.  Aprire il foglio di stile XSLT nell'editor XML.  
  
2.  Specificare un documento XML nel **Input** campo del documento **proprietà** finestra.  
  
    > [!NOTE]
    >  Il documento XML è il documento di input usato per la trasformazione. Se un documento non viene specificato quando la trasformazione XSLT viene avviata, il **Apri File** verrà visualizzata la finestra di dialogo, ed è possibile specificare un documento in quel momento.  
  
3.  Fare clic sul **ShowXSLT Output** pulsante il **Editor XML** sulla barra degli strumenti.  
  
     L'output risultante dalla trasformazione XSLT viene visualizzato in una nuova finestra del documento.  
  
### <a name="to-provide-a-different-output-file-name"></a>Per fornire un nome di file di output diverso  
  
1.  Specificare un nome file tra il **Output** campo del documento **proprietà** finestra.  
  
2.  Fare clic sul **ShowXSLT Output** pulsante il **Editor XML** sulla barra degli strumenti.  
  
     L'output risultante dalla trasformazione XSLT viene visualizzato in una nuova finestra del documento e l'editor usato nella finestra di output dipende dall'estensione del file di **Output** proprietà del documento.  
  
## <a name="see-also"></a>Vedere anche  
 [Editor XML](../xml-tools/xml-editor.md)


