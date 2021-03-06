---
title: Salvataggio permanente della proprietà di un elemento di progetto | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- properties, adding to a project item
- project items, adding properties
ms.assetid: d7a0f2b0-d427-4d49-9536-54edfb37c0f3
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 149ffa4fd0f4847cffbba915fc1d2714234ce792
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2018
ms.locfileid: "51745260"
---
# <a name="persisting-the-property-of-a-project-item"></a>Salvataggio permanente della proprietà di un elemento di progetto
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

È possibile mantenere una proprietà che è aggiungere a un elemento del progetto, ad esempio l'autore di un file di origine. Questo scopo, è possibile archiviare la proprietà nel file di progetto.  
  
 Il primo passaggio per rendere persistente di una proprietà in un file di progetto è per ottenere la gerarchia del progetto come un <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> interfaccia. È possibile ottenere questa interfaccia con l'automazione oppure usando <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection>. Dopo avere ottenuto l'interfaccia, è possibile usarlo per determinare quale elemento di progetto è attualmente selezionato. Dopo aver creato l'ID di elemento di progetto, è possibile usare <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> aggiungere la proprietà.  
  
 Nelle procedure seguenti, rendere permanente la proprietà VsPkg.cs `Author` con il valore `Tom` nel file di progetto.  
  
### <a name="to-obtain-the-project-hierarchy-with-the-dte-object"></a>Per ottenere la gerarchia del progetto con l'oggetto DTE  
  
1.  Per il pacchetto VSPackage, aggiungere il codice seguente:  
  
    ```csharp  
    EnvDTE.DTE dte = (EnvDTE.DTE)Package.GetGlobalService(typeof(EnvDTE.DTE));  
    EnvDTE.Project project = dte.Solution.Projects.Item(1);  
  
    string uniqueName = project.UniqueName;  
    IVsSolution solution = (IVsSolution)Package.GetGlobalService(typeof(SVsSolution));  
    IVsHierarchy hierarchy;  
    solution.GetProjectOfUniqueName(uniqueName, out hierarchy);  
    ```  
  
### <a name="to-persist-the-project-item-property-with-the-dte-object"></a>Per rendere permanente la proprietà di elemento di progetto con l'oggetto DTE  
  
1.  Aggiungere il codice seguente al codice fornito nel metodo nella procedura precedente:  
  
    ```csharp  
    IVsBuildPropertyStorage buildPropertyStorage =   
        hierarchy as IVsBuildPropertyStorage;  
    if (buildPropertyStorage != null)  
    {  
        uint itemId;  
        string fullPath = (string)project.ProjectItems.Item(  
            "VsPkg.cs").Properties.Item("FullPath").Value;  
        hierarchy.ParseCanonicalName(fullPath, out itemId);  
        buildPropertyStorage.SetItemAttribute(itemId, "Author", "Tom");  
    }  
    ```  
  
### <a name="to-obtain-the-project-hierarchy-using-ivsmonitorselection"></a>Per ottenere la gerarchia del progetto usando IVsMonitorSelection  
  
1.  Per il pacchetto VSPackage, aggiungere il codice seguente:  
  
    ```csharp  
    IVsHierarchy hierarchy = null;  
    IntPtr hierarchyPtr = IntPtr.Zero;  
    IntPtr selectionContainer = IntPtr.Zero;  
    uint itemid;  
  
    // Retrieve shell interface in order to get current selection  
    IVsMonitorSelection monitorSelection =     Package.GetGlobalService(typeof(SVsShellMonitorSelection)) as     IVsMonitorSelection;  
    if (monitorSelection == null)  
        throw new InvalidOperationException();  
  
    try  
    {  
        // Get the current project hierarchy, project item, and selection container for the current selection  
        // If the selection spans multiple hierachies, hierarchyPtr is Zero  
        IVsMultiItemSelect multiItemSelect = null;  
        ErrorHandler.ThrowOnFailure(  
            monitorSelection.GetCurrentSelection(  
                out hierarchyPtr, out itemid,   
                out multiItemSelect, out selectionContainer));  
  
        // We only care if there is only one node selected in the tree  
        if (!(itemid == VSConstants.VSITEMID_NIL ||   
            hierarchyPtr == IntPtr.Zero ||  
            multiItemSelect != null ||  
            itemid == VSConstants.VSITEMID_SELECTION))  
        {  
            hierarchy = Marshal.GetObjectForIUnknown(hierarchyPtr)  
                as IVsHierarchy;  
        }  
    }  
    finally  
    {  
        if (hierarchyPtr != IntPtr.Zero)  
            Marshal.Release(hierarchyPtr);  
        if (selectionContainer != IntPtr.Zero)  
            Marshal.Release(selectionContainer);  
    }  
    ```  
  
2.  
  
### <a name="to-persist-the-selected-project-item-property-given-the-project-hierarchy"></a>Per rendere persistente la proprietà di elemento di progetto selezionato, assegnato alla gerarchia del progetto  
  
1.  Aggiungere il codice seguente al codice fornito nel metodo nella procedura precedente:  
  
    ```  
    IVsBuildPropertyStorage buildPropertyStorage =   
        hierarchy as IVsBuildPropertyStorage;  
    if (buildPropertyStorage != null)  
    {  
        buildPropertyStorage.SetItemAttribute(itemId, "Author", "Tom");  
    }  
    ```  
  
### <a name="to-verify-that-the-property-is-persisted"></a>Per verificare che la proprietà viene mantenuta  
  
1.  Avviare [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] e quindi aprire o creare una soluzione.  
  
2.  Selezionare il progetto elemento VsPkg.cs nelle **Esplora soluzioni**.  
  
3.  Usare un punto di interruzione o altrimenti determinare che il VSPackage viene caricato e che venga eseguito SetItemAttribute.  
  
    > [!NOTE]
    >  È possibile caricare automaticamente un VSPackage nel contesto dell'interfaccia utente <xref:Microsoft.VisualStudio.VSConstants.UICONTEXT.SolutionExists_guid>. Per altre informazioni, vedere [caricamento di VSPackage](../extensibility/loading-vspackages.md).  
  
4.  Chiudi [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] e quindi aprire il file di progetto nel blocco note. Verrà visualizzato il \<Author > tag con il valore di Tom, come indicato di seguito:  
  
    ```  
    <Compile Include="VsPkg.cs">  
        <Author>Tom</Author>  
    </Compile>  
    ```  
  
## <a name="see-also"></a>Vedere anche  
 [Strumenti personalizzati](../extensibility/internals/custom-tools.md)

