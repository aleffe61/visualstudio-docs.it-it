---
title: '&lt;assemblyIdentity&gt; elemento (applicazione ClickOnce) | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#assemblyIdentity
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <assemblyIdentity> element [ClickOnce application manifest]
ms.assetid: f48e9531-efac-4d11-8166-f63a5ece1ac5
caps.latest.revision: 22
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 67ee803e18a1b098cd8e1bad2befd5a2d794766c
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47540683"
---
# <a name="ltassemblyidentitygt-element-clickonce-application"></a>&lt;assemblyIdentity&gt; elemento (applicazione ClickOnce)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [ &lt;assemblyIdentity&gt; elemento (applicazione ClickOnce)](https://docs.microsoft.com/visualstudio/deployment/assemblyidentity-element-clickonce-application).  
  
Identifica l'applicazione distribuita un [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] distribuzione.  
  
## <a name="syntax"></a>Sintassi  
  
```  
  
      <assemblyIdentity   
   name  
   version  
   publicKeyToken  
   processorArchitecture  
   language  
/>  
```  
  
## <a name="elements-and-attributes"></a>Elementi e attributi  
 Il `assemblyIdentity` elemento è obbligatorio. Non contiene alcun elemento figlio e ha gli attributi seguenti.  
  
|Attributo|Descrizione|  
|---------------|-----------------|  
|`Name`|Obbligatorio. Identifica il nome dell'applicazione.<br /><br /> Se `Name` contiene caratteri speciali, ad esempio le virgolette singole o doppie, l'applicazione potrebbe non riuscire per l'attivazione.|  
|`Version`|Obbligatorio. Specifica il numero di versione dell'applicazione nel formato seguente: `major.minor.build.revision`|  
|`publicKeyToken`|Facoltativo. Specifica una stringa esadecimale a 16 caratteri rappresentato dagli ultimi 8 byte del `SHA-1` valore della chiave pubblica utilizzata per firmare l'applicazione o assembly hash. La chiave pubblica utilizzato per firmare il catalogo deve essere 2048 bit o superiore.<br /><br /> Anche se la firma di un assembly è facoltativo ma consigliato, questo attributo è obbligatorio. Se un assembly è firmato, è necessario copiare un valore da un assembly autofirmato oppure utilizzare un valore "fittizio" di tutti gli zeri.|  
|`processorArchitecture`|Obbligatorio. Specifica il processore. I valori validi sono `msil` per tutti i processori `x86` per Windows, a 32 `IA64` per Windows a 64 bit, e `Itanium` per processori Itanium di Intel a 64 bit.|  
|`language`|Obbligatorio. Identifica i codici di lingua di due parti (ad esempio, `en-US`) dell'assembly. Questo elemento è presente il `asmv2` dello spazio dei nomi. Se non viene specificato, il valore predefinito è `neutral`.|  
  
## <a name="examples"></a>Esempi  
  
### <a name="description"></a>Descrizione  
 L'esempio di codice seguente illustra un' `assemblyIdentity` elemento in un [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] manifesto dell'applicazione. Questo esempio di codice è parte di un esempio più esaustivo disponibile nel [ClickOnce Application Manifest](../deployment/clickonce-application-manifest.md).  
  
### <a name="code"></a>Codice  
  
```  
<asmv1:assemblyIdentity   
  name="My Application Deployment.exe"   
  version="1.0.0.0"   
  publicKeyToken="43cb1e8e7a352766"   
  language="neutral"   
  processorArchitecture="x86"   
  type="win32" />  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Manifesto dell'applicazione ClickOnce](../deployment/clickonce-application-manifest.md)   
 [\<assemblyIdentity > elemento](../deployment/assemblyidentity-element-clickonce-deployment.md)


