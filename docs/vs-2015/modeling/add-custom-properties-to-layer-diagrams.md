---
title: Aggiungere proprietà personalizzate ai diagrammi livello | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- layer diagrams, adding custom properties
ms.assetid: 52b3ac25-d10b-4507-a1fe-209ccb4d2777
caps.latest.revision: 23
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: 1fc9c3e67cbb10484c814acb0eedbfbae2729eb4
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47519682"
---
# <a name="add-custom-properties-to-layer-diagrams"></a>Aggiungere proprietà personalizzate ai diagrammi livello
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [aggiungere proprietà personalizzate ai diagrammi delle dipendenze](https://docs.microsoft.com/visualstudio/modeling/add-custom-properties-to-layer-diagrams).  
  
Quando si scrive un codice di estensione per i diagrammi livello, è possibile archiviare i valori con qualsiasi elemento in un diagramma livello. I valori saranno permanenti quando il diagramma viene salvato e riaperto. È inoltre possibile impostare queste proprietà vengono visualizzate nel **proprietà** finestra in modo che gli utenti possono vedere e modificarli. Ad esempio, è possibile consentire agli utenti di specificare un'espressione regolare per ogni livello e scrivere il codice di convalida per verificare che i nomi delle classi in ogni livello siano conformi al modello specificato dall'utente.  
  
## <a name="properties-not-visible-to-the-user"></a>Proprietà non visibili all'utente  
 Se si desidera solo che il codice associ i valori a un elemento in un diagramma livello, non è necessario definire un componente MEF. Esiste un dizionario denominato `Properties` in <xref:Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer.ILayerElement>. Aggiungere semplicemente i valori marshalable al dizionario di qualsiasi elemento del livello. I valori saranno salvati come parte del diagramma livello. Per altre informazioni, vedere [esplorare e aggiornare i modelli nel codice del programma di livello](../modeling/navigate-and-update-layer-models-in-program-code.md).  
  
## <a name="properties-that-the-user-can-edit"></a>Proprietà modificabili dall'utente  
 **Preparazione iniziale**  
  
> [!IMPORTANT]
>  Per fare in modo che le proprietà vengano visualizzate, è necessario apportare le seguenti modifiche in ogni computer in cui si desidera che le proprietà del livello siano visibili.  
>   
>  1.  Eseguire blocco note scegliendo **Esegui come amministratore**. Aprire `%ProgramFiles%\Microsoft Visual Studio [version]\Common7\IDE\Extensions\Microsoft\Architecture Tools\ExtensibilityRuntime\extension.vsixmanifest`  
> 2.  Nell'elemento `Content` aggiungere:  
>   
>     ```xml  
>     <MefComponent>Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer.Provider.dll</MefComponent>  
>     ```  
> 3.  Sotto il **strumenti di Visual Studio** sezione del menu start dell'applicazione di Visual Studio, aprire **prompt dei comandi sviluppatore**.  
>   
>      Immettere:  
>   
>      `devenv /rootSuffix /updateConfiguration`  
>   
>      `devenv /rootSuffix Exp /updateConfiguration`  
> 4.  Riavviare Visual Studio.  
  
 **Assicurarsi che il codice è in un progetto VSIX**  
  
 Se la proprietà fa parte di un comando, di un movimento o di un progetto di convalida, non è necessario aggiungere alcun valore. Il codice per la proprietà personalizzata deve essere specificato in un progetto Extensibility di Visual Studio definito come componente MEF. Per altre informazioni, vedere [aggiungere comandi e movimenti a diagrammi livelli](../modeling/add-commands-and-gestures-to-layer-diagrams.md) oppure [aggiungere la convalida architettura personalizzati a diagrammi livelli](../modeling/add-custom-architecture-validation-to-layer-diagrams.md).  
  
 **Definire la proprietà personalizzata**  
  
 Per creare una proprietà personalizzata, definire una classe come quella seguente:  
  
```  
[Export(typeof(IPropertyExtension))]  
public class MyProperty   
      : PropertyExtension<ILayerElement>  
{  
  // Implement the interface.  
}  
```  
  
 È possibile definire le proprietà in <xref:Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer.ILayerElement> o nelle relative classi derivate che includono:  
  
-   `ILayerModel` - il modello  
  
-   `ILayer` - ciascun livello  
  
-   `ILayerDependencyLink` - i collegamenti tra i livelli  
  
-   `ILayerComment`  
  
-   `ILayerCommentLink`  
  
## <a name="example"></a>Esempio  
 Il codice seguente è un descrittore di proprietà personalizzate tipico. Definisce una proprietà booleana nel modello di livello (`ILayerModel`) che consente all'utente di specificare i valori per un metodo di convalida personalizzata.  
  
```  
using System;  
using System.ComponentModel.Composition;  
using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer;  
  
namespace MyNamespace  
{  
  /// <summary>  
  /// Custom properties are added to the Layer Designer via a custom  
  /// Property Descriptor. We have to export this Property Descriptor  
  /// using MEF to make it available in the Layer Designer.  
  /// </summary>  
  [Export(typeof(IPropertyExtension))]  
  public class AllTypesMustBeReferencedProperty   
      : PropertyExtension<ILayerModel>  
  {  
    /// <summary>  
    /// Each custom property must have a unique name.   
    /// Usually we use the full name of this class.  
    /// </summary>  
    public static readonly string FullName =  
      typeof(AllTypesMustBeReferencedProperty).FullName;  
  
    /// <summary>  
    /// Construct the property. Notice the use of FullName.  
    /// </summary>  
    public AllTypesMustBeReferencedProperty()  
            : base(FullName)  
    {  }  
  
    /// <summary>  
    /// The display name is shown in the Properties window.  
    /// We therefore use a localizable resource.  
    /// </summary>  
    public override string DisplayName  
    {  
      get { return Strings.AllTypesMustBeReferencedDisplayName; }  
    }  
  
    /// <summary>  
    /// Description shown at the bottom of the Properties window.  
    /// We use a resource string for easier localization.  
    /// </summary>  
    public override string Description  
    {  
      get { return Strings.AllTypesMustBeReferencedDescription; }  
    }  
  
    /// <summary>  
    /// This is called to set a new value for this property. We must  
    /// throw an exception if the value is invalid.  
    /// </summary>  
    /// <param name="component">The target ILayerElement</param>  
    /// <param name="value">The new value</param>  
    public override void SetValue(object component, object value)  
    {  
      ValidateValue(value);  
      base.SetValue(component, value);  
    }  
    /// <summary>  
    /// Helper to validate the value.  
    /// </summary>  
    /// <param name="value">The value to validate</param>  
    private static void ValidateValue(object value)  
    {  }  
  
    public override Type PropertyType  
    { get { return typeof(bool); } }  
  
    /// <summary>  
    /// The segment label of the properties window.  
    /// </summary>  
    public override string Category  
    {   
      get  
      {  
        return Strings.AllTypesMustBeReferencedCategory;  
      }  
    }  
  }  
}  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Estendere i diagrammi livello](../modeling/extend-layer-diagrams.md)


