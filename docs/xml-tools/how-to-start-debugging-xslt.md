---
title: 'Procedura: del debug di XSLT'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: 170d4d3d0c952e13a5fefb74b23536f50be1e9a6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53925131"
---
# <a name="how-to-start-debugging-xslt"></a>Procedura: Avvio del debug XSLT

Il debugger XSLT può essere usato per eseguire il debug di un foglio di stile o di un'applicazione XSLT. Durante il debug è possibile eseguire il codice una riga alla volta eseguendo le istruzioni, ignorandole o eseguendole al di fuori del codice. I comandi per usare la funzionalità di esecuzione del codice riga per riga sono uguali a quelli del debugger XSLT e degli altri debugger di Visual Studio. Una volta avviato il debug, nel debugger XSLT vengono aperte finestre di visualizzazione del documento di input e dell'output XSLT.

## <a name="xml-editor"></a>Editor XML

È possibile avviare il debugger dall'editor XML. Questo consente di eseguire il debug durante la progettazione di un foglio di stile.

### <a name="to-start-debugging-from-a-style-sheet"></a>Per avviare il debug da un foglio di stile

1. Aprire il foglio di stile nell'editor XML.

1. Selezionare **Debug XSLT** dalle **XML** menu.

### <a name="to-start-debugging-from-an-xml-input-document"></a>Per avviare il debug da un documento di input XML

1. Aprire il documento XML nell'editor XML.

1. Selezionare **Debug XSLT** dalle **XML** menu.

## <a name="xslt-from-other-languages"></a>XSLT di altre lingue

È possibile inoltre eseguire le istruzioni XSLT durante il debug di un'applicazione. Se si preme F11 su una chiamata <xref:System.Xml.Xsl.XslCompiledTransform.Transform%2A?displayProperty=fullName>, il debugger sarà in grado di eseguire il codice XSLT.

> [!NOTE]
> Non è supportata l'esecuzione di istruzioni XSLT dalla classe <xref:System.Xml.Xsl.XslTransform>. La classe <xref:System.Xml.Xsl.XslCompiledTransform> è l'unico processore XSLT in grado di supportare l'esecuzione di istruzioni XSLT durante il debug.

### <a name="to-start-debugging-an-xslt-application"></a>Per avviare il debug di un'applicazione XSLT

1. Durante la creazione dell'istanza dell'oggetto <xref:System.Xml.Xsl.XslCompiledTransform>, impostare il parametro `enableDebug` su `true` nel codice.

     In questo modo viene indicato al processore XSLT di creare le informazioni di debug dopo la compilazione del codice.

1. Premere F11 per eseguire il codice XSLT.

     Il foglio di stile XSLT viene caricato in una nuova finestra di documento e il debugger XSLT viene avviato.

     In alternativa, è possibile aggiungere un punto di interruzione al foglio di stile ed eseguire l'applicazione.

### <a name="example"></a>Esempio

Di seguito è riportato un esempio di programma XSLT in C#. Viene illustrato come abilitare il debug di XSLT.

```csharp
using System;
using System.IO;
using System.Xml;
using System.Xml.Xsl;

namespace ConsoleApplication
{
  class Program
  {
    private const string sourceFile = @"c:\data\xsl_files\books.xml";
    private const string stylesheet = @"c:\data\xsl_files\belowAvg.xsl";
    private const string outputFile = @"c:\data\xsl_files\output.xml";

    static void Main(string[] args)
    {
      // Enable XSLT debugging.
      XslCompiledTransform xslt = new XslCompiledTransform(true);

      // Compile the style sheet.
      xslt.Load(stylesheet)

      // Execute the XSLT transform.
      FileStream outputStream = new FileStream(outputFile, FileMode.Append);
      xslt.Transform(sourceFile, null, outputStream);
    }
  }
}
```

## <a name="see-also"></a>Vedere anche

- [Procedura dettagliata: Eseguire il debug di un foglio di stile XSLT](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md)
- [Presentazione del debugger](../debugger/debugger-feature-tour.md)   