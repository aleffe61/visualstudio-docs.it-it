---
title: IDebugProgramNode2::GetHostName | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugProgramNode2::GetHostName
helpviewer_keywords:
- IDebugProgramNode2::GetHostName
ms.assetid: 16aad1ff-ad34-4394-a2e4-5621374a7729
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f90e4d2db358cae62be74941b01afd49537cce26
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47531152"
---
# <a name="idebugprogramnode2gethostname"></a>IDebugProgramNode2::GetHostName
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [IDebugProgramNode2::GetHostName](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprogramnode2-gethostname).  
  
Ottiene il nome del processo che ospita il programma.  
  
## <a name="syntax"></a>Sintassi  
  
```cpp#  
HRESULT GetHostName (   
   GETHOSTNAME_TYPE dwHostNameType,  
   BSTR*            pbstrHostName  
);  
```  
  
```csharp  
int GetHostName (   
   enum_GETHOSTNAME_TYPE dwHostNameType,  
   out string            pbstrHostName  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `dwHostNameType`  
 [in] Un valore compreso il [GETHOSTNAME_TYPE](../../../extensibility/debugger/reference/gethostname-type.md) enumerazione che specifica il tipo del nome da restituire.  
  
 `pbstrHostName`  
 [out] Restituisce il nome del processo di hosting.  
  
## <a name="return-value"></a>Valore restituito  
 Se ha esito positivo, restituisce `S_OK`; in caso contrario, restituisce un codice di errore.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente viene illustrato come implementare questo metodo per un semplice `CProgram` oggetto che espone il [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) interfaccia. In questo esempio ignora il `dwHostNameType` parametro e restituisce solo il nome del programma come tratto dal nome di base del percorso del file del modulo.  
  
```cpp#  
HRESULT CProgram::GetHostName(DWORD dwHostNameType, BSTR* pbstrHostName) {    
   // Check for valid argument.    
   if (pbstrHostName)    
   {    
      char szModule[_MAX_PATH];    
  
      // Attempt to assign to szModule the path for the file used  
      // to create the calling process.    
      if (GetModuleFileName(NULL, szModule, sizeof (szModule)))    
      {    
         // If successful then declare several char arrays    
         char  szDrive[_MAX_DRIVE];    
         char  szDir[_MAX_DIR];    
         char  szName[_MAX_FNAME];    
         char  szExt[_MAX_EXT];    
         char  szFilename[_MAX_FNAME + _MAX_EXT];    
         WCHAR wszFilename[_MAX_FNAME + _MAX_EXT];    
  
         // Break the szModule path name into components.    
         _splitpath(szModule, szDrive, szDir, szName, szExt);    
  
         // Copy the base file name szName into szFilename.    
         lstrcpy(szFilename, szName);    
         // Append the field extension szExt into szFilename.    
         lstrcat(szFilename, szExt);    
  
         // Convert the szFilename sequence of multibyte characters    
         // to the wszFilename sequence of wide characters.    
         mbstowcs(wszFilename, szFilename, sizeof (wszFilename) / 2);    
  
         // Assign the wszFilename to the value at *pbstrHostName.    
         *pbstrHostName = SysAllocString(wszFilename);    
  
          return S_OK;    
      }    
   }    
  
    return E_INVALIDARG;    
}    
```  
  
## <a name="see-also"></a>Vedere anche  
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [GETHOSTNAME_TYPE](../../../extensibility/debugger/reference/gethostname-type.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
