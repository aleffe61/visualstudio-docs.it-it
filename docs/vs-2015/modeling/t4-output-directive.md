---
title: T4 Direttiva di Output | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 03a14993-47ad-4f2e-8032-57db28d5842a
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 2e2d30c5d1dee578da14608a4e272fea09184a76
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49198523"
---
# <a name="t4-output-directive"></a>Direttiva output T4
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nei modelli di testo di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] la direttiva `output` viene usata per definire l'estensione di file e la codifica del file trasformato.  
  
 Ad esempio, se il [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] progetto include un file di modello denominato **MyTemplate.tt** che contiene la direttiva seguente:  
  
 `<#@output extension=".cs"#>`  
  
 quindi [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] genererà un file denominato **MyTemplate.cs**  
  
 La direttiva `output` in un modello di testo (pre-elaborato) della fase di esecuzione non è necessaria. L'applicazione otterrà la stringa generata con una chiamata a `TextTransform()`. Per altre informazioni, vedere [generazione di testo in fase di esecuzione con modelli di testo T4](../modeling/run-time-text-generation-with-t4-text-templates.md).  
  
## <a name="using-the-output-directive"></a>Uso della direttiva output  
  
```  
<#@ output extension=".fileNameExtension" [encoding="encoding"] #>  
```  
  
 In ogni modello di testo non deve essere presente più di una direttiva `output`.  
  
## <a name="extension-attribute"></a>attributo di estensione  
 Specifica l'estensione di file del file di output di testo generato.  
  
 Il valore predefinito è **. cs**  
  
 Esempi:  
 `<#@ output extension=".txt" #>`  
  
 `<#@ output extension=".htm" #>`  
  
 `<#@ output extension=".cs" #>`  
  
 `<#@ output extension=".vb" #>`  
  
 Valori accettabili:  
 Qualsiasi estensione di file valida.  
  
## <a name="encoding-attribute"></a>attributo di codifica  
 Specifica la codifica da usare quando viene generato il file di output. Ad esempio:  
  
 `<#@ output encoding="utf-8"#>`  
  
 Il valore predefinito è la codifica usata dal file di modello di testo.  
  
 Valori accettabili:  
 `us-ascii`  
  
 `utf-16BE`  
  
 `utf-16`  
  
 `utf-8`  
  
 `utf-7`  
  
 `utf-32`  
  
 `0` (valore predefinito del sistema)  
  
 In generale, è possibile usare la stringa WebName o il numero CodePage di tutte le codifiche restituite da <xref:System.Text.Encoding.GetEncodings%2A?displayProperty=fullName>.



