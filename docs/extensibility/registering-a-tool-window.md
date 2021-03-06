---
title: La registrazione di una finestra degli strumenti | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- tool windows, registering managed
- tool windows, registering
ms.assetid: 8c8c4a24-3da4-497b-9db2-0ddd7cfbfdd2
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 0ae73dec5b494e4f9d78949224a34bcdbc66361f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53884957"
---
# <a name="register-a-tool-window"></a>Registrare una finestra degli strumenti
È possibile registrare le finestre degli strumenti usando <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowAttribute> e <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowVisibilityAttribute>.  
  
## <a name="example"></a>Esempio  
  
```csharp
  
[ProvideToolWindow(typeof(PersistedWindowPane), Style = MsVsShell.VsDockStyle.Tabbed, Window = "3ae79031-e1bc-11d0-8f78-00a0c9110057")]
[ProvideToolWindow(typeof(DynamicWindowPane), PositionX=250, PositionY=250, Width=160, Height=180, Transient=true)]
[ProvideToolWindowVisibility(typeof(DynamicWindowPane), /*UICONTEXT_SolutionExists*/"f1536ef8-92ec-443c-9ed7-fdadf150da82")]  
[ProvideMenuResource(1000, 1)]  
[PackageRegistration(UseManagedResourcesOnly = true)]  
[Guid("01069CDD-95CE-4620-AC21-DDFF6C57F012")]  
public class PackageToolWindow : Package  
{  
```
  
 Nel codice precedente, il <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowAttribute> registra il `PersistedWindowPane` e `DynamicWindowPane` strumento windows con Visual Studio. La finestra degli strumenti persistente viene ancorata e a schede con **Esplora soluzioni**, e la finestra dinamica è stata assegnata un valore predefinito a partire da posizione e dimensioni. La finestra dinamica viene resa temporanea, che indica che non è stato creato all'avvio. Scrive un `DontForceCreate` valore di `ToolWindows` chiave nel Registro di sistema. Per altre informazioni, vedere [configurazione visualizzazione della finestra degli strumenti](../extensibility/tool-window-display-configuration.md).
