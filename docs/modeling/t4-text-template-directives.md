---
title: Direttive di modello di testo T4
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- text templates, import directive
- text templates, include directive
- text templates, assembly directive
- text templates, output directive
- text templates, directives
- text templates, template directive
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 3bf8248a7a68b914d6276e3e6f37261fb6137efc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53939252"
---
# <a name="t4-text-template-directives"></a>Direttive di modello di testo T4
Le direttive forniscono istruzioni al motore di trasformazione del modello di testo.

 La sintassi per le direttive è la seguente:

```
<#@ DirectiveName [AttributeName = "AttributeValue"] ... #>
```

 Tutti i valori di attributo devono essere racchiusi tra virgolette doppie. Se il valore stesso contiene virgolette, è necessario applicare loro il carattere di escape \.

 Le direttive sono in genere i primi elementi di un file modello o di un file incluso. Tali elementi non devono essere inseriti in un blocco di codice `<#...#>`, né dopo un blocco della funzionalità di classe `<#+...#>`.

 [Direttiva template T4](../modeling/t4-template-directive.md)
 ```
<#@ template [language="VB"] [hostspecific="true|TrueFromBase"] [debug="true"] [inherits="templateBaseClass"] [culture="code"] [compilerOptions="options"] [visibility="internal"] [linePragmas="false"] #>
```

 [Direttiva parameter T4](../modeling/t4-parameter-directive.md)
 ```
<#@ parameter type="Full.TypeName" name="ParameterName" #>
```

 [Direttiva output T4](../modeling/t4-output-directive.md)
 ```
<#@ output extension=".fileNameExtension" [encoding="encoding"] #>
```

 [Direttiva assembly T4](../modeling/t4-assembly-directive.md)
 ```
<#@ assembly name="[assembly strong name|assembly file name]" #>
```

 [Direttiva import T4](../modeling/t4-import-directive.md)
 ```
<#@ import namespace="namespace" #>
```

 [Direttiva include T4](../modeling/t4-include-directive.md)
 ```
<#@ include file="filePath" #>
```

 [Direttiva T4 CleanUpBehavior](../modeling/t4-cleanupbehavior-directive.md)
 ```
<#@ CleanupBehavior processor="T4VSHost" CleanupAfterProcessingtemplate="true" #>
```

 È inoltre possibile creare direttive personalizzate. Per altre informazioni, vedere [creazione di processori direttiva di modelli di Custom T4 testo](../modeling/creating-custom-t4-text-template-directive-processors.md). Se si utilizza l'SDK di visualizzazione e modellazione per creare un linguaggio DSL, verrà generato un processore di direttiva come parte di tale linguaggio DSL.