---
title: Esclusione da Windows Information Protection
ms.date: 06/01/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 665a4e893b8b146555dd35caad5cc521e1630dd9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53891505"
---
# <a name="configure-visual-studio-as-a-wip-exempt-app"></a>Configurare Visual Studio come app esclusa da WIP

[Windows Information Protection](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip) (WIP) consente di proteggere i dati aziendali dalla divulgazione per mezzo di app come posta elettronica, social media e cloud pubblico, che sono esclusi dal controllo dell'azienda. WIP consente di proteggere i dati da perdite accidentali nei dispositivi di proprietà dell'azienda e nei dispositivi personali, senza dover apportare modifiche all'ambiente o ad altre app.

Le app *con supporto predefinito per* WIP sono progettate in modo da impedire che i dati aziendali passino a percorsi di rete non protetti ed evitare che i dati personali vengano crittografati. Visual Studio non è un'app con supporto predefinito, quindi non funziona in ambienti abilitati per WIP a meno che non venga esclusa. Seguire i passaggi descritti in questo articolo per consentire a Visual Studio di funzionare in un computer abilitato per WIP.

## <a name="configure-vs-as-a-wip-exempt-app"></a>Configurare Visual Studio come app esclusa da WIP

È possibile escludere Visual Studio dalle restrizioni WIP consentendo però l'uso dei dati aziendali. Le app escluse da WIP possono connettersi alle risorse cloud aziendali usando un indirizzo IP o un nome host. Non viene applicata alcuna crittografia e l'app può accedere ai file locali.

Per escludere Visual Studio da WIP, seguire i [passaggi necessari per escludere un'applicazione desktop](/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure#exempt-apps-from-a-wip-policy).

## <a name="create-a-wip-exempt-applocker-policy-file"></a>Creare un file dei criteri di AppLocker escluso da WIP

Poiché Visual Studio include più file binari, [creare un file dei criteri di AppLocker escluso da WIP](/windows/security/threat-protection/windows-defender-application-control/applocker/run-the-automatically-generate-rules-wizard). AppLocker consente di generare automaticamente regole per tutti i file all'interno di una cartella.

## <a name="add-appcompat-to-the-enterprise-cloud-resource-policy"></a>Aggiungere AppCompat ai criteri delle risorse cloud aziendali

Per specificare dove Visual Studio può accedere ai dati aziendali nella rete, seguire questi [passaggi per definire la posizione in cui le app protette possono individuare e inviare i dati aziendali](/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure#choose-where-apps-can-access-enterprise-data). Per impedire a Windows di bloccare le connessioni alle risorse cloud attraverso un indirizzo IP, assicurarsi di aggiungere la stringa /\*AppCompat\*/ all'impostazione.

## <a name="see-also"></a>Vedere anche

- Articolo sul [comportamento delle app con WIP](/windows/security/information-protection/windows-information-protection/app-behavior-with-wip)