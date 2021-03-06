---
title: Convalida dei Frame di grafica | Microsoft Docs
ms.custom: ''
ms.date: 03/02/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.graphics.FrameValidation
ms.assetid: 1e639182-1301-4e28-9c1e-b5df732f3f1b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 0cdfdee83a9c78069b3f086ef84b280ba9328e4f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49850880"
---
# <a name="graphics-frame-validation"></a>Convalida Frame di grafica
<!-- VERSIONLESS --> Visual Studio 2017 e il supporto maggiore di **convalida Frame** dello strumento.  Consente di visualizzare la finestra di convalida Frame errori e avvisi associati con l'elenco di eventi.  Per visualizzare questa finestra, selezionare la **Visualizza > convalida Frame** menu.

![Convalida frame](media/gfx_diag_frame_validation.png)

Scegliere il **Esegui convalida** pulsante nell'angolo superiore sinistro per avviare l'analisi.  Potrebbero occorrere alcuni minuti a seconda della complessità del frame.  I dati che viene visualizzata di seguito è una combinazione di due origini: i messaggi di tale D3D se stessa quando emette [livelli SDK](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) è abilitata e i dati raccolti dallo stato interno dello strumento di rilevamento. Al termine dell'operazione, si noterà diverse colonne di dati:


| **Colonna** | **Descrizione** |
|------------| - |
| ID evento | ID che viene eseguito il mapping a una voce nella [elenco eventi](graphics-event-list.md) finestra. |
| Gravità | Danneggiamento, errore, avviso, informazioni o messaggio. |
| Category | Applicazione esterni, definita, l'inizializzazione, pulizia, compilazione, creazione stato, impostazione dello stato, recupero dello stato, l'esecuzione, modifica delle risorse, Shader, ridondanti e inutilizzate. |
| Messaggio | Il messaggio associato all'evento. |
| event | L'evento associato all'errore o avviso. |

## <a name="see-also"></a>Vedere anche  
[Diagnostica della grafica (debug grafica DirectX)](visual-studio-graphics-diagnostics.md)   
<!-- /VERSIONLESS -->