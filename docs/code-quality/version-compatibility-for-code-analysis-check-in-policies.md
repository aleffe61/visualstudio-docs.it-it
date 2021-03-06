---
title: Criteri di archiviazione relativi alla compatibilità delle versioni per l'analisi del codice
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- version compatibility, code analysis check-in policy
- check-in policies, version compatibility for code analysis
ms.assetid: 1af376e3-3be7-4445-803b-76a858567a5b
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d9c57b9e0afb443c8ec808dbd2908c1b8b7031aa
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53892508"
---
# <a name="version-compatibility-for-code-analysis-check-in-policies"></a>Criteri di archiviazione relativi alla compatibilità delle versioni per l'analisi del codice

Se è necessario valutare e creare codice check-in Criteri di analisi usino versioni diverse di [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)], è necessario conoscere le differenze nella procedura [!INCLUDE[vstsTfsOrcasLong](../code-quality/includes/vststfsorcaslong_md.md)] e [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] valutare i criteri di controllo.

## <a name="version-compatibility-for-evaluating-check-in-policies"></a>Compatibilità delle versioni di valutazione di criteri di archiviazione

- Quando i criteri di controllo dell'analisi del codice vengono valutati [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], eventuali regole presenti in [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] ma non esistono nel [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] vengono ignorati.

- Quando i criteri di controllo dell'analisi del codice vengono valutati [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)], tutte le regole sono esclusive di [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] vengono ignorati.

- Se i criteri di controllo dell'analisi codice specificano gli assembly di regole, [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] Ignora tutte le regole che vengono specificate dagli assembly che non riconosce.

- Se i criteri di controllo dell'analisi codice specificano gli assembly di regole che [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] non riconosce, viene visualizzato un messaggio.

## <a name="version-compatibility-for-authoring-check-in-policies"></a>Compatibilità delle versioni per la creazione di criteri di archiviazione

- Se è stato creato un criterio di controllo dell'analisi codice usando il [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] versione di [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)], non è possibile utilizzare il [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] versione di [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] per modificarlo. E inoltre [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] non è possibile valutare i criteri.

- Se è stato creato un criterio di controllo dell'analisi codice usando [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] nel [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)], è possibile usare [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] nelle [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] per modificarlo, quindi i criteri possa anche essere valutato [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)]. Dopo aver modificato i criteri usando [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] nel [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], è non possibile modificare i criteri non sono più usando [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] in [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)]. [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] può valutare i criteri senza problemi con i nomi sicuri non corrispondenti.

- Per creare un criterio di controllo dell'analisi codice con impostazioni delle regole valide per entrambi [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] e [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], è necessario creare i criteri in [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)], apportare tutte le modifiche necessarie e salvare il criterio. Se le modifiche alle regole sono disponibili solo nel [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], modificare e salvare i criteri in [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)].

   Dopo aver salvato i criteri in [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], non è più è possibile modificare le impostazioni per le regole esistenti in [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] solo.