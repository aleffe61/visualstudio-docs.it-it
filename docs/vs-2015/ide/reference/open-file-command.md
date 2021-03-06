---
title: Comando Apri file | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- file.openfile
helpviewer_keywords:
- Open File command
- File.OpenFile command
- of command
ms.assetid: a51a83fc-e3c6-4fa2-8882-8b7b6c0a6406
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 0b519d8defcdc4b43dd7ca84552536ca655bb348
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2018
ms.locfileid: "49247936"
---
# <a name="open-file-command"></a>Comando Apri file
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Apre un file esistente e consente di specificare un editor.  
  
## <a name="syntax"></a>Sintassi  
  
```  
File.OpenFile filename [/e:editorname]  
```  
  
## <a name="arguments"></a>Argomenti  
 `filename`  
 Obbligatorio. Percorso completo o parziale e nome file del file da aprire. I percorsi contenenti spazi devo devono essere racchiusi tra virgolette.  
  
## <a name="switches"></a>Opzioni  
 /e:`editorname`  
 Facoltativo. Nome dell'editor in cui verrà aperto il file. Se viene specificato l'argomento ma non viene fornito il nome di un editor, verrà visualizzata la finestra di dialogo **Apri con**.  
  
 La sintassi dell'argomento /e:`editorname` usa i nomi degli editor così come visualizzati nella finestra di dialogo Apri con, racchiusi tra virgolette.  
  
 Ad esempio, per aprire un file nell'editor del codice sorgente, per l'argomento /e:`editorname` è necessario immettere quanto segue.  
  
```  
/e:"Source Code (text) Editor"  
```  
  
## <a name="remarks"></a>Note  
 Quando si immette un percorso, il completamento automatico tenta di individuare il percorso e il nome file corretti.  
  
## <a name="example"></a>Esempio  
 In questo esempio viene aperto il file di stile "Test1.css" nell'editor del codice sorgente.  
  
```  
>File.OpenFile "C:\My Projects\project1\Test1.css" /e:"Source Code (text) Editor"  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Visual Studio Commands](../../ide/reference/visual-studio-commands.md)  (Comandi di Visual Studio)  
 [Command Window](../../ide/reference/command-window.md)  (Finestra di comando)  
 [Finestra di controllo immediato](../../ide/reference/immediate-window.md)   
 [Find/Command Box](../../ide/find-command-box.md)  (Casella Trova/Comando)  
 [Visual Studio Command Aliases](../../ide/reference/visual-studio-command-aliases.md)



