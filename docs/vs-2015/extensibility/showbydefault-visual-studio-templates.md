---
title: ShowByDefault (modelli di Visual Studio) | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#ShowByDefault
helpviewer_keywords:
- <ShowByDefault> element [Visual Studio Templates]
- ShowByDefault element [Visual Studio Templates]
ms.assetid: 7be783f6-0ef6-42bc-924a-df9a2eba7781
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 063836d07931456d99bce31c793866e7d5421c91
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519118"
---
# <a name="showbydefault-visual-studio-templates"></a>ShowByDefault (modelli di Visual Studio)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [ShowByDefault (modelli di Visual Studio)](https://docs.microsoft.com/visualstudio/extensibility/showbydefault-visual-studio-templates).  
  
Se `false`, specifica che il modello verrà visualizzato solo con il nome specificato [TemplateGroupID](../extensibility/templategroupid-element-visual-studio-templates.md).  
  
 \<VSTemplate >  
 \<TemplateData >  
 \<ShowByDefault >  
  
## <a name="syntax"></a>Sintassi  
  
```  
<ShowByDefault> true/false </ShowByDefault>  
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
 Nessuno.  
  
### <a name="child-elements"></a>Elementi figlio  
 Nessuno.  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Classifica il modello in base alla categoria e definisce la modalità di visualizzazione nella finestra di dialogo **Nuovo progetto** o **Aggiungi nuovo elemento** .|  
  
## <a name="text-value"></a>Valore di testo  
 È necessario specificare un valore di testo.  
  
 Questo testo deve essere `true` o `false`. Se true, specifica che il modello verrà visualizzato per tutti i tipi di progetto. Se false, il modello verrà visualizzato solo nel `TemplateGroupID` specificato.  
  
## <a name="remarks"></a>Note  
 `ShowByDefault` è un elemento facoltativo. Il valore predefinito è `true`.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente vengono illustrati i metadati per un modello [!INCLUDE[csprcs](../includes/csprcs-md.md)].  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic template</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <ShowByDefault>false</ShowByDefault>  
    </TemplateData>  
    <TemplateContent>  
        <Project File="MyTemplate.csproj">  
            <ProjectItem>Form1.cs<ProjectItem>  
            <ProjectItem>Form1.Designer.cs</ProjectItem>  
            <ProjectItem>Program.cs</ProjectItem>  
            <ProjectItem>Properties\AssemblyInfo.cs</ProjectItem>  
            <ProjectItem>Properties\Resources.resx</ProjectItem>  
            <ProjectItem>Properties\Resources.Designer.cs</ProjectItem>  
            <ProjectItem>Properties\Settings.settings</ProjectItem>  
            <ProjectItem>Properties\Settings.Designer.cs</ProjectItem>  
        </Project>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Creazione di modelli di progetti e di elementi](../ide/creating-project-and-item-templates.md)   
 [Riferimenti allo schema dei modelli di Visual Studio](../extensibility/visual-studio-template-schema-reference.md)   
 [Elemento TemplateGroupID (modelli di Visual Studio)](../extensibility/templategroupid-element-visual-studio-templates.md)
