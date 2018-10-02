---
title: '&lt;compatibleFrameworks&gt; elemento (distribuzione ClickOnce) | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <compatibleFrameworks> element [ClickOnce deployment manifest]
ms.assetid: f6c3ee55-9e65-403d-8664-3ebde872c7d4
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: c5abcc6e7c4308cf0d60c78cd4ef0f052403bb1f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47528385"
---
# <a name="ltcompatibleframeworksgt-element-clickonce-deployment"></a>&lt;compatibleFrameworks&gt; elemento (distribuzione ClickOnce)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [ &lt;compatibleFrameworks&gt; elemento (distribuzione ClickOnce)](https://docs.microsoft.com/visualstudio/deployment/compatibleframeworks-element-clickonce-deployment).  
  
Identifica le versioni di .NET Framework in cui è possibile installare ed eseguire questa applicazione.  
  
> [!NOTE]
>  [MageUI.exe](http://msdn.microsoft.com/library/f9e130a6-8117-49c4-839c-c988f641dc14) non supporta la `compatibleFrameworks` elemento durante il salvataggio di un manifesto dell'applicazione che è già stato firmato con un certificato usando [MageUI.exe](http://msdn.microsoft.com/library/f9e130a6-8117-49c4-839c-c988f641dc14). È invece necessario usare [Mage.exe](http://msdn.microsoft.com/library/77dfe576-2962-407e-af13-82255df725a1).  
  
## <a name="syntax"></a>Sintassi  
  
```  
<compatibleFrameworks  
      SupportUrl>   
   <framework  
      targetVersion  
      profile  
      supportedRuntime  
   />   
</ compatibleFrameworks>  
```  
  
## <a name="elements-and-attributes"></a>Elementi e attributi  
 Il `compatibleFrameworks` elemento è obbligatorio per manifesti della distribuzione che hanno come destinazione il [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] fornita dal runtime [!INCLUDE[net_v40_short](../includes/net-v40-short-md.md)] o versione successiva. Il `compatibleFrameworks` elemento contiene uno o più `framework` gli elementi che specificano le versioni di .NET Framework in cui è possibile eseguire questa applicazione. Il [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] runtime verrà eseguita l'applicazione in corrispondenza del primo disponibile `framework` in questo elenco.  
  
 La tabella seguente elenca l'attributo che la `compatibleFrameworks` supportato dall'elemento.  
  
|Attributo|Descrizione|  
|---------------|-----------------|  
|`S` `upportUrl`|Facoltativo. Specifica un URL in cui può essere scaricata la versione di .NET Framework compatibile preferita.|  
  
## <a name="framework"></a>framework  
 Obbligatorio. Nella tabella seguente elenca gli attributi che il `framework` supportato dall'elemento.  
  
|Attributo|Descrizione|  
|---------------|-----------------|  
|`targetVersion`|Obbligatorio. Specifica il numero di versione di .NET Framework di destinazione.|  
|`profile`|Obbligatorio. Specifica il profilo di .NET Framework di destinazione.|  
|`supportedRuntime`|Obbligatorio. Specifica il numero di versione del runtime associato alla destinazione .NET Framework.|  
  
## <a name="remarks"></a>Note  
  
## <a name="example"></a>Esempio  
 Nell'esempio di codice riportato di seguito viene illustrato un `compatibleFrameworks` elemento in un [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] manifesto della distribuzione. Questa distribuzione può essere eseguita di [!INCLUDE[net_client_v40_long](../includes/net-client-v40-long-md.md)]. Anche possibile eseguire nel [!INCLUDE[net_v40_short](../includes/net-v40-short-md.md)] perché è un superset del [!INCLUDE[net_client_v40_long](../includes/net-client-v40-long-md.md)].  
  
```  
<compatibleFrameworks xmlns="urn:schemas-microsoft-com:clickonce.v2">  
  <framework   
      targetVersion="4.0"   
      profile="Client"   
      supportedRuntime="4.0.30319" />  
</compatibleFrameworks>  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Manifesto di distribuzione ClickOnce](../deployment/clickonce-deployment-manifest.md)


