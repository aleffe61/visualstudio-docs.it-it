---
title: Attributi condizionali dello Schema XML VSCT | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, conditional attributes
- conditional attributes (VSCT XML schema)
ms.assetid: 754d4f32-319b-44c9-915f-f7c60e53222e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: fae45cde013615cd0363f1a97158a178e4b0348c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53943434"
---
# <a name="vsct-xml-schema-conditional-attributes"></a>Attributi condizionali dello schema XML VSCT
È possibile applicare attributi condizionali per tutti gli elementi e gli elenchi. Simboli espansione espressioni e operatori logici restituiscono true o false. Se true, l'elenco associato o elemento è incluso nell'output risultante.  
  
 È possibile testare le espansioni token con altri token espansioni o costanti. La funzione `Defined()` verifica se è stato definito un determinato nome, anche se non ha alcun valore.  
  
 Quando un attributo Condition è applicato a un elenco, la condizione viene applicata a ogni elemento figlio nell'elenco. Se un elemento figlio contiene un attributo Condition, quindi la condizione viene combinata con l'espressione padre mediante un'operazione con AND.  
  
 I valori 1, '1' e 'true' vengono valutati come true e 0, '0' e 'false' vengono valutate come false.  
  
## <a name="operators"></a>Operatori  
 Usare gli operatori seguenti per valutare le espressioni condizionali.  
  
|Operatore|Definizione|  
|--------------|----------------|  
|(,)|Raggruppamento|  
|!|NOT logico|  
|\<, >, \<=, >=, ==, !=|Relazionale e uguaglianza|  
|e|Booleano|  
|oppure|Booleano|  
  
## <a name="examples"></a>Esempi  
  
```xml  
<Menu Condition="Defined(DEBUG)" ...  
</Menu>  
  
<Menu Condition="%(SKU_MODE) = 'Demo'" ...  
</Menu>  
  
<Menus Condition="Defined(DEBUG)">  
    <Menu ...  
    </Menu>  
</Menus>  
  
<Menus Condition="Defined(DEMO_SKU)">  
    <Menus Condition="!Defined(DEBUG)">  
        <Menu ...  
        </Menu>  
    </Menus>  
  
    <Menu ...  
    </Menu>  
</Menus>  
  
<Menus Condition="(Defined(DEMO_SKU) or Defined(SAMPLE_SKU))   
and !Defined(DEBUG)">  
    <Menu ...  
    </Menu>  
</Menus>  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Tabella di comandi Visual Studio (. File Vsct)](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)