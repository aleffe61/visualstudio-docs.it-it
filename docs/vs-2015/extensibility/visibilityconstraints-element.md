---
title: Elemento VisibilityConstraints | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VisibilityConstraints
helpviewer_keywords:
- VSCT XML schema elements, VisibilityConstraints
- VisibilityConstraints element (VSCT XML schema)
ms.assetid: d6dcd314-6fe4-4693-a189-91fa026c7b34
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9fd6d6968984f0640dd73067c286a4259ade6745
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47531874"
---
# <a name="visibilityconstraints-element"></a>Elemento VisibilityConstraints
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [elemento VisibilityConstraints](https://docs.microsoft.com/visualstudio/extensibility/visibilityconstraints-element).  
  
L'elemento VisibilityConstraints determina la visibilità statica dei gruppi di comandi e le barre degli strumenti. La visibilità prima di tutto è controllata dal [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] ambiente di sviluppo integrato (IDE) senza caricare il pacchetto VSPackage.  
  
## <a name="syntax"></a>Sintassi  
  
```  
<VisibilityConstraints>  
  <VisibilityConstraint>... </VisibilityConstraint>  
  <VisibilityConstraint>... </VisibilityConstraint>  
</VisibilityConstraint>  
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
  
|Attributo|Descrizione|  
|---------------|-----------------|  
|Condizione|Facoltativo. Visualizzare [attributi condizionali](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Elementi figlio  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[Elemento VisibilityItem](../extensibility/visibilityitem-element.md)|Determina la visibilità statica di comandi e le barre degli strumenti.|  
|[VisibilityConstraints](../extensibility/visibilityconstraints-element.md)|Determina la visibilità statica dei gruppi di comandi e le barre degli strumenti.|  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[Elemento CommandTable](../extensibility/commandtable-element.md)|Definisce tutti gli elementi che rappresentano i comandi (ad esempio, le voci di menu, menu, barre degli strumenti e caselle combinate) che un pacchetto VSPackage fornisce all'IDE.|  
  
## <a name="example"></a>Esempio  
  
```  
<VisibilityConstraints>  
  <VisibilityItem guid="cmdSetGuidMyProductCommands"     id="cmdidAddWidget"  
    context="guidNotViewSourceMode"/>  
</VisibilityConstraints>  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Elemento VisibilityItem](../extensibility/visibilityitem-element.md)   
 [File Visual Studio Command Table (VSCT)](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
