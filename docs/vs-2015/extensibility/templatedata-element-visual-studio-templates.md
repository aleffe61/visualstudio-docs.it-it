---
title: Elemento TemplateData (modelli di Visual Studio) | Microsoft Docs
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
- http://schemas.microsoft.com/developer/vstemplate/2005#TemplateData
helpviewer_keywords:
- TemplateData element [Visual Studio project templates]
ms.assetid: db17ec9b-bfdf-46b1-bbe7-5ccc140056e2
caps.latest.revision: 25
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 03825105f549030c05ac202f1e3601977adec7f9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519675"
---
# <a name="templatedata-element-visual-studio-templates"></a>Elemento TemplateData (modelli di Visual Studio)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [elemento TemplateData (modelli di Visual Studio)](https://docs.microsoft.com/visualstudio/extensibility/templatedata-element-visual-studio-templates).  
  
Classifica il modello in base alla categoria e definisce la modalità di visualizzazione nella finestra di dialogo **Nuovo progetto** o **Aggiungi nuovo elemento** .  
  
 \<VSTemplate >  
 \<TemplateData >  
  
## <a name="syntax"></a>Sintassi  
  
```  
<TemplateData>  
    <Name> ... </Name>  
    <Description> ... </Description>  
    <Icon> ... </Icon>  
    <ProjectType> ... </ProjectType>  
    ...  
</TemplateData>  
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
 Nessuno.  
  
### <a name="child-elements"></a>Elementi figlio  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[Nome](../extensibility/name-element-visual-studio-templates.md)|Elemento obbligatorio.<br /><br /> Specifica il nome del modello così come appare in entrambi i **nuovo progetto** o il **Aggiungi nuovo elemento** nella finestra di dialogo.|  
|[Descrizione](../extensibility/description-element-visual-studio-templates.md)|Elemento obbligatorio.<br /><br /> Specifica la descrizione del modello così come appare in entrambi i **nuovo progetto** o il **Aggiungi nuovo elemento** nella finestra di dialogo.|  
|[Icona](../extensibility/icon-element-visual-studio-templates.md)|Elemento obbligatorio.<br /><br /> Specifica il percorso e il nome del file del file di immagine che funge da icona, che viene visualizzata in uno il **nuovo progetto** o nella **Aggiungi nuovo elemento** della finestra di dialogo per il modello.|  
|[Tipoprogetto](../extensibility/projecttype-element-visual-studio-templates.md)|Elemento obbligatorio.<br /><br /> Classifica il modello di progetto in modo che venga visualizzata sotto il gruppo specificato di **nuovo progetto** nella finestra di dialogo.|  
|[ProjectSubType](../extensibility/projectsubtype-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Classifica il modello di progetto in modo che venga visualizzata sotto la sottocategoria specificata nella finestra di **nuovo progetto** nella finestra di dialogo.|  
|[TemplateID](../extensibility/templateid-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica l'ID del modello.|  
|[TemplateGroupID](../extensibility/templategroupid-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica l'ID del gruppo di modello.|  
|[SortOrder](../extensibility/sortorder-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica un valore che viene usato per disporre il modello, tra gli altri modelli della stessa categoria, così come appare in entrambi i **nuovo progetto** oppure **Aggiungi nuovo elemento** nella finestra di dialogo.|  
|[CreateNewFolder](../extensibility/createnewfolder-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se nella creazione di un'istanza del progetto viene creata una cartella che lo contiene.|  
|[DefaultName](../extensibility/defaultname-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica il nome che verrà generato il sistema di progetto di Visual Studio per il progetto o un elemento al momento della creazione.|  
|[ProvideDefaultName](../extensibility/providedefaultname-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se il sistema di progetto di Visual Studio genera il nome predefinito per un progetto o un elemento al momento della creazione.|  
|[PromptForSaveOnCreation](../extensibility/promptforsaveoncreation-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se è possibile creare il progetto come progetto temporaneo.|  
|[EnableLocationBrowseButton](../extensibility/enablelocationbrowsebutton-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se il **esplorare** pulsante è disponibile nel **nuovo progetto** finestra di dialogo, in modo che gli utenti possono facilmente modificare la directory predefinita in cui viene salvato un nuovo progetto.|  
|[Nascosta](../extensibility/hidden-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se il modello viene visualizzato in entrambi i **nuovo progetto** oppure **Aggiungi nuovo elemento** nella finestra di dialogo.|  
|[NumberOfParentCategoriesToRollUp](../extensibility/numberofparentcategoriestorollup-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica il numero di categorie principali che verrà visualizzato il modello nel **nuovo progetto** nella finestra di dialogo.|  
|[LocationFieldMRUPrefix](../extensibility/locationfieldmruprefix-element-visual-studio-templates.md)|Elemento facoltativo.|  
|[LocationField](../extensibility/locationfield-element-visual-studio-project-templates.md)|Elemento facoltativo.<br /><br /> Specifica o meno il **posizione** casella di testo il **nuovo progetto** nella finestra di dialogo è abilitata, disabilitata o nascosta per il modello di progetto.|  
|[RequiredFrameworkVersion](../extensibility/requiredframeworkversion-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Usare questo elemento se il modello supporta solo una versione minima specifica e versioni successive, se presente, di .NET Framework.|  
|[SupportsMasterPage](../extensibility/supportsmasterpage-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se il modello supporta una pagina master per i progetti web.|  
|[SupportsCodeSeparation](../extensibility/supportscodeseparation-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se il modello supporta la separazione del codice o il modello di pagina code-behind, per i progetti web.|  
|[SupportsLanguageDropDown](../extensibility/supportslanguagedropdown-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica se il modello è identico per più linguaggi e, se il **Language** opzione è disponibile il **nuovo progetto** nella finestra di dialogo.|  
|[TargetPlatformName](../extensibility/targetplatformname-element-visual-studio-templates.md)|Elemento facoltativo.<br /><br /> Specifica la piattaforma a cui è destinato il modello di progetto. Questo elemento specifica un modello di progetto viene utilizzato per creare [!INCLUDE[win8_appname_long](../includes/win8-appname-long-md.md)] app.|  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[VSTemplate](../extensibility/vstemplate-element-visual-studio-templates.md)|Elemento obbligatorio.<br /><br /> Contiene tutti i metadati per il modello di progetto, un modello di elemento o lo starter kit.|  
  
## <a name="remarks"></a>Note  
 `TemplateData` un elemento è obbligatorio.  
  
 Se non si include un elemento facoltativo, viene utilizzato il valore predefinito per tale elemento.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente mostra i metadati per un modello di progetto per un [!INCLUDE[csprcs](../includes/csprcs-md.md)] dell'applicazione.  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic starter kit</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <Project File="MyStarterKit.csproj">  
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
 [Riferimenti allo schema dei modelli di Visual Studio](../extensibility/visual-studio-template-schema-reference.md)   
 [Creazione di modelli di progetti e di elementi](../ide/creating-project-and-item-templates.md)
