---
title: Proprietà dei connettori | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Domain-Specific Language, connectors
ms.assetid: b1f24e8d-cdd7-4a5d-af37-1038f43b45c7
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: b78858b14674eafeb044b168a8bb8927af9f5769
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49171847"
---
# <a name="properties-of-connectors"></a>Proprietà dei connettori
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

I connettori rappresentano le relazioni di dominio in una finestra di progettazione generata.  
  
 Per altre informazioni, vedere [come definire un linguaggio specifico di dominio](../modeling/how-to-define-a-domain-specific-language.md). Per altre informazioni su come usare queste proprietà, vedere [personalizzare ed estendere un linguaggio specifico di dominio](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
 I connettori hanno le proprietà elencate nella tabella seguente.  
  
|Proprietà|Descrizione|Impostazione predefinita|  
|--------------|-----------------|-------------|  
|Colore|Il colore di questo connettore.|Nero|  
|Visualizzazione dello stile tratteggiato|Lo stile di tratteggio per la riga per questo connettore (tinta unita, Dash, Dot, Trattopunto, Trattopuntopunto o personalizzato).|Tinta unita|  
|Stile dell'estremità di origine|Stile finale di origine per questo connettore (HollowArrow, EmptyArrow, FilledArrow, EmptyDiamond, FilledDiamond o None).|nessuno|  
|Stile dell'estremità di destinazione|Stile finale di destinazione per questo connettore (HollowArrow, EmptyArrow, FilledArrow, EmptyDiamond, FilledDiamond o None).|nessuno|  
|Colore del testo|Colore utilizzato per gli elementi Decorator di testo associati a questo connettore.|Nero|  
|Thickness|Lo spessore della linea per questo connettore, misurata in pollici.|0.03125|  
|Modificatore di accesso|Il livello di accesso della classe (`public` o `internal`).|Public|  
|Attributi personalizzati|Consente di aggiungere attributi alla classe di codice sorgente generato da questo connettore.|\<Nessuno >|  
|Genera l'errore doppia derivati|Se `True`, verrà generate una classe di base sia una classe parziale (per supportare la personalizzazione tramite override). Per altre informazioni, vedere [override ed estensione delle classi generate](../modeling/overriding-and-extending-the-generated-classes.md).|False|  
|Ha un costruttore personalizzato|Se `True`, verrà fornito un costruttore personalizzato nel codice sorgente. Per altre informazioni, vedere [override ed estensione delle classi generate](../modeling/overriding-and-extending-the-generated-classes.md).|False|  
|Modificatore di ereditarietà|Descrive il tipo di ereditarietà della classe di codice sorgente generato dal connettore (`none`, `abstract` o `sealed`).|none|  
|Connettore di base|Classe di base di questo connettore.|(nessuno)|  
|nome|Il nome di questo connettore.|Nome corrente|  
|Spazio dei nomi|Lo spazio dei nomi che è associato a questo connettore.|Spazio dei nomi corrente|  
|Tipo della descrizione comando|Modalità la descrizione comando viene definito (fisso, variabile o none). Se viene risolto, quindi il valore della `Fixed Tooltip Text` proprietà viene usata come descrizione comando; se la variabile, la descrizione comando è definito nel codice personalizzato.|\<Nessuno >|  
|Note|Note informali associate a questo connettore.|\<Nessuno >|  
|Stile di routing|Stile utilizzato per il routing del connettore. Oggetto `Rectilinear` connettore consente ad angolo retto turns come richiesto; un `Straight` retti.|Rectilinear|  
|Colore esposte come proprietà<br /><br /> Visualizzazione dello stile tratteggiato esposte come proprietà<br /><br /> Spessore esposto come proprietà<br /><br /> Espone il colore del testo|Se `True`, l'utente può impostare la proprietà specificata di una forma. Per procedere, fare doppio clic la definizione della forma e fare clic su **Aggiungi esposta**.|False|  
|Descrizione|Consente di documentare la finestra di progettazione generata.|\<Nessuno >|  
|Nome visualizzato|Il nome che verrà visualizzato nella finestra di progettazione generata per questo connettore.|\<Nessuno >|  
|Testo della descrizione comando fissa|Testo che viene usato per una descrizione comando fissa.|\<Nessuno >|  
|Parola chiave della Guida|La parola chiave utilizzata per indicizzare la Guida F1 per questo elemento.|\<Nessuno >|  
  
## <a name="see-also"></a>Vedere anche  
 [Glossario sugli strumenti Domain-Specific Language](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)



