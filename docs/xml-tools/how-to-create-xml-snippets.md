---
title: 'Procedura: di frammenti di codice XML'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: d8556dd7-1382-4af7-ba80-3e873c9416be
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ec6332f52e732e99cc6d81512c9b3c469e99e18e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53829102"
---
# <a name="how-to-create-xml-snippets"></a>Procedura: Creare frammenti XML

L'editor XML può essere usato per creare nuovi frammenti di codice XML. L'editor comprende un frammento di codice XML, denominato "Snippet", ovvero un frammento standard per la creazione di nuovi frammenti di codice XML.

## <a name="to-create-a-new-xml-snippet"></a>Per creare un nuovo frammento di codice XML

 Per creare un nuovo codice XML frammento di codice, creare un nuovo file XML e usare la **Inserisci frammento di codice** funzionalità.

1.  Nel **File** menu, fare clic su **New** e quindi fare clic su **File**.

2.  Fare clic su **File XML** e quindi fare clic su **Open**.

3.  Nel riquadro dell'editor e scegliere **Inserisci frammento di codice**.

4.  Selezionare **frammento** dall'elenco e premere **invio**.

5.  Se necessario, apportare modifiche al nuovo frammento.

6.  Dal **File** dal menu **Salva XMLFile**.

     Il **Salva File con nome** verrà visualizzata la finestra di dialogo.

7.  Immettere un nome per il nuovo frammento di codice e selezionare **file di frammenti** dal **Salva come tipo** finestra elenco a discesa.

8.  Usare la **salvare nel** elenco a discesa per modificare il percorso del file del *Documenti\Visual Studio 2005\Code Snippets\XML\My XML Snippets* cartella e quindi premere **Salva**.

## <a name="snippet-description"></a>Descrizione di frammento di codice

 Contenuto della sezione vengono descritti alcuni elementi chiave del frammento di codice standard. Per altre informazioni sugli elementi dello schema usati per i frammenti di codice XML, vedere [riferimenti allo schema dei frammenti di codice](../ide/code-snippets-schema-reference.md).

### <a name="snippettype-element"></a>SnippetType, elemento

 L'editor supporta due tipi di frammento di codice:

```xml
<SnippetTypes>
  <SnippetType>SurroundsWith</SnippetType>
  <SnippetType>Expansion</SnippetType>
</SnippetTypes>
```

 Il `Expansion` tipo determina se il frammento di codice viene visualizzato quando si richiama il **Inserisci frammento di codice** comando. Il `SurroundsWith` tipo determina se il frammento di codice viene visualizzato quando si richiama il **Racchiudi** comando.

### <a name="code-element"></a>Elemento del codice

 L'elemento `Code` definisce il testo XML che verrà inserito quando viene richiamato il frammento di codice.

> [!NOTE]
> Il testo del frammento di codice XML deve essere racchiuso in una sezione `<![CDATA[...]]>`.


 Di seguito viene riportato l'elemento `Code` creato dal frammento standard.

```xml
<Code Language="XML">
  <![CDATA[<test>
  <name>$name$</name>
  $selected$ $end$</test>]]>
</Code>
```

 L'elemento `Code` comprende tre variabili.

- $name$ è la variabile definita dall'utente e consente di creare un elemento `name`, che presenta un valore modificabile il cui valore predefinito è "name". Le variabili definite dall'utente vengono definite usando l'elemento `Literal`.

- $selected$ è una variabile predefinita e rappresenta il testo che era stato selezionato nell'editor XML prima di richiamare il frammento di codice. La posizione di questa variabile determina la posizione del testo selezionato nel frammento di codice che racchiude la selezione.

- $end$ è una variabile predefinita. Quando l'utente preme **invio** per completare la modifica dei campi di frammento di codice, questa variabile determina in cui verrà spostato l'accento circonflesso (^).

  L'elemento `Code` consente l'inserimento del testo XML seguente:

```xml
<test>
  <name>name</name>
</test>
```

 Il valore dell'elemento nome viene contrassegnato come area modificabile.

### <a name="literal-element"></a>Literal, elemento

 L'elemento `Literal` viene usato per identificare il testo di sostituzione che è possibile personalizzare dopo che è stato inserito nel file. Ad esempio, le stringhe letterali, i valori numerici e alcuni nomi di variabili possono essere dichiarati come letterali. È possibile definire un qualsiasi numero di valori formali nel frammento di codice XML e farvi riferimento più volte dall'interno del frammento. Di seguito viene riportato un esempio di elemento `Literal` che definisce una variabile $name$ il cui valore predefinito è "name."

```xml
<Literal>
  <ID>name</ID>
  <Default>name</Default>
</Literal
```

 I valori formali possono anche fare riferimento a funzioni. L'Editor XML include una funzione denominata **LookupPrefix**. Il **LookupPrefix** funzione Cerca l'URI dello spazio dei nomi specificato dalla posizione nel documento XML che questo frammento di codice viene richiamato dal e restituisce il prefisso dello spazio dei nomi definito per tale spazio dei nomi, se presente, e include i due punti (:) in tale nome. Di seguito è riportato un esempio di un `Literal` elemento che utilizza il **LookupPrefix** (funzione).

```xml
<Literal Editable="false">
   <ID>prefix</ID>
   <Function>LookupPrefix("namespaceURI")</Function>
</Literal>
```

 La variabile $prefix$ può quindi essere usata in altri punti all'interno del frammento di codice XML.

## <a name="see-also"></a>Vedere anche

- [Frammenti di codice XML](../xml-tools/xml-snippets.md)
- [Procedura: Usare frammenti XML](../xml-tools/how-to-use-xml-snippets.md)
- [Procedura: Generare un frammento XML da uno schema XML](../xml-tools/how-to-generate-an-xml-snippet-from-an-xml-schema.md)