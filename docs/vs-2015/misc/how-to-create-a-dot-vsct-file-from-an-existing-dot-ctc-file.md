---
title: 'Procedura: creare una. File Vsct da un oggetto esistente. File CTC | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- VSCT files, creating based on a .ctc file
ms.assetid: 700e80a4-c1e1-4178-af53-45e86dd2c08b
caps.latest.revision: 9
manager: douge
ms.openlocfilehash: e159fea34dc395ce2d7bded813f2d8feaa453006
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49303485"
---
# <a name="how-to-create-a-vsct-file-from-an-existing-ctc-file"></a>Procedura: Creare un file con estensione vsct da un file CTC esistente
È possibile creare un file con estensione vsct basato su XML da un file di origine CTC esistente della tabella comandi. In questo modo, si può sfruttare il nuovo formato basato su XML del compilatore della tabella comandi di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] (VSCT).  
  
### <a name="to-create-a-vsct-file-from-a-ctc-file"></a>Per creare un file con estensione vsct da un file CTC  
  
1.  Ottenere una copia del linguaggio Perl.  
  
2.  Ottenere una copia dello script Perl ConvertCTCToVSCT.pl, in genere si trova nel  *\<percorso di installazione di Visual Studio SDK >* \visualstudiointegration\tools\bin. cartella.  
  
3.  Ottenere una copia del file di origine CTC da convertire.  
  
4.  Inserire i file nella stessa directory.  
  
5.  Nella finestra del prompt dei comandi di [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] spostarsi nella directory.  
  
6.  Digitare  
  
    ```  
    perl.exe ConvertCTCtoVSCT.pl PkgCmd.ctc PkgCmd.vsct  
    ```  
  
     dove PkgCmd.ctc è il nome del file CTC e PkgCmd.vsct è il nome del file con estensione vsct da creare.  
  
     Verrà creato un nuovo file di origine XML della tabella comandi con estensione vsct. È possibile compilare il file con Vsct.exe, il compilatore VSCT, come si farebbe con qualsiasi altro file con estensione vsct.  
  
    > [!NOTE]
    >  È possibile migliorare la leggibilità del file con estensione vsct riformattando i commenti XML.  
  
## <a name="see-also"></a>Vedere anche  
 [Procedura: creare una. File Vsct](../extensibility/internals/how-to-create-a-dot-vsct-file.md)   
 [File Visual Studio Command Table (VSCT)](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)