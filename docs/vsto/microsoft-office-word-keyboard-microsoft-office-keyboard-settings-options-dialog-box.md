---
title: Finestra di dialogo Opzioni di tastiera di Microsoft Office Word, impostazioni tastiera Microsoft Office,
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.ToolsOptionsPages.Microsoft_Office_Tools.Microsoft_Office_Word.Keyboard
- VS.ToolsOptionsPages.Microsoft_Office_Keyboard_Settings.Microsoft_Office_Word_Keyboard
- VST.WordOptions.KeyboardMappingScheme
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- keyboard shortcuts, Office development in Visual Studio
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: fd493a1448276dcf151a862771546a31f201c761
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53909281"
---
# <a name="microsoft-office-word-keyboard-microsoft-office-keyboard-settings-options-dialog-box"></a>Finestra di dialogo Opzioni di tastiera di Microsoft Office Word, impostazioni tastiera Microsoft Office,
  Sia Microsoft Office Word e Visual Studio consentono di gestire i tasti di scelta rapida. La stessa combinazione di tasti di scelta rapida può attivare diversi comandi di Word e in Visual Studio. Quando è aperto in un progetto a livello di documento in Visual Studio, solo un'applicazione in un momento riceve i comandi dei tasti di scelta rapida. Per impostazione predefinita, Visual Studio riceve tutti i comandi dei tasti di scelta rapida, ma è possibile apportare Word riceverli quando il documento dispone dello stato attivo selezionando **schema della tastiera dinamico**.  
  
 Se si usa un tasto di scelta rapida che non è assegnato a un comando nell'applicazione che sta gestendo i tasti di scelta rapida, il tasto di scelta rapida viene passato a altra applicazione.  
  
 L'opzione selezionata rimarranno in vigore per i progetti Word fino alla successiva modifica. La selezione non influenza i progetti di Microsoft Office Excel. Per apportare qualsiasi modifica apportata per Excel è necessario utilizzare le opzioni della tastiera di Microsoft Office Excel.  
  
## <a name="uielement-list"></a>Elenco UIElement  
 **Schema della tastiera di Visual Studio**  
 Visual Studio riceve tutti i comandi dei tasti di scelta rapida, anche se il documento di Word ha lo stato attivo. Ad esempio, se si preme il tasto funzione **F5** mentre il documento dispone dello stato attivo, Visual Studio avvia il debug della soluzione.  
  
 **Schema della tastiera dinamico**  
 Visual Studio riceve i comandi dei tasti di scelta rapida solo quando lo stato attivo. Quando il documento di Word ha lo stato attivo, Word riceve tutti i comandi dei tasti di scelta rapida. Ad esempio, se si preme il tasto funzione **F5** mentre il documento di Word è attivo, verrà aperto il **Trova e sostituisci** finestra di dialogo con il **Vai a** selezionato della scheda. Se si preme **F5** mentre Visual Studio ha lo stato attivo, Visual Studio avvia il debug della soluzione.  
  
## <a name="see-also"></a>Vedere anche  
 [Finestra di dialogo Opzioni di tastiera di Microsoft Office Excel, impostazioni tastiera Microsoft Office,](../vsto/microsoft-office-excel-keyboard-microsoft-office-keyboard-settings-options-dialog-box.md)  
