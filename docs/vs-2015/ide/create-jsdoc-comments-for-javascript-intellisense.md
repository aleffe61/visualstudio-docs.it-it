---
title: Creare commenti JSDoc per IntelliSense per JavaScript | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: a0dadc81-3755-4a47-bcee-c1010819ff2a
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 9d338b2bece99f720670871a1b92c6b2a57c4280
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49908587"
---
# <a name="create-jsdoc-comments-for-javascript-intellisense"></a>Creare commenti JSDoc per IntelliSense per JavaScript
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

IntelliSense in Visual Studio visualizza le informazioni aggiunte a uno script tramite i commenti JSDoc standard. È possibile usare i commenti JSDoc per fornire informazioni sugli elementi di codice, come funzioni, campi e variabili.  

## <a name="jsdoc-comment-tags"></a>Tag di commento JSDoc  
 I tag di commento JSDoc standard elencati di seguito vengono usati da IntelliSense per visualizzare informazioni sul codice.  


|  Tag JSDoc   |                       Sintassi                        |                                                     Note                                                      |
|--------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| @deprecated  |              @deprecated *Descrizione*              |                                   Specifica una funzione o un metodo deprecato.                                   |
| @description |             @description *Descrizione*              |                              Specifica la descrizione di una funzione o di un metodo.                               |
|    @param    | @param {*tipo*} *parameterName*<em>descrizione</em> | Specifica le informazioni relative a un parametro in una funzione o un metodo.<br /><br /> TypeScript supporta anche @paramTag. |
|  @property   |          @property {*tipo*} *propertyName*          |   Specifica le informazioni, inclusa una descrizione, relative a un campo o a un membro definito per un oggetto.    |
|   @returns   |                  @returns {*tipo*}                  |           Specifica un valore restituito.<br /><br /> Per TypeScript, usare @returnType invece di @returns.           |
|   @summary   |               @summary *Descrizione*                |                   Specifica la descrizione di una funzione o metodo (uguale a @description).                   |
|    @type     |                   @type {*tipo*}                    |                                Specifica il tipo di una costante o di una variabile.                                |
|   @typedef   |         @typedef {*tipo*} *Nometipopersonalizzato*          |                                            Specifica un tipo personalizzato.                                            |

### <a name="examples"></a>Esempi  
 L'esempio seguente illustra l'uso del @description, @param, e @return tag JSDoc per una funzione denominata `getArea`.  

```javascript  
/** @description Determines the area of a circle that has the specified radius parameter.  
 * @param {number} radius The radius of the circle.  
 * @return {number}  
 */  
function getArea(radius) {  
    var areaVal;  
    areaVal = Math.PI * radius * radius;  
    return areaVal;  
}  
```  

 Nell'esempio precedente IntelliSense mostra le informazioni su descrizione, parametri e valori restituiti quando si digita la parentesi di apertura per `getArea`.  

 ![Informazioni di IntelliSense per una funzione](../ide/media/js-intellisense-jsdoc-comments.png "JS_IntelliSense_JSDoc_Comments")  

 Nell'esempio seguente viene illustrato come utilizzare il @typedef contrassegnare con il @property tag.  

```javascript  
/**  
  * @typedef {object} Weather  
  * @property {string} current The current weather.  
  */  
function getForecast(Weather) {  
}  

var w = new Weather();  
```  

 L'esempio seguente illustra l'uso del @type tag JSDoc. Come illustrato in questo esempio, l'accesso single asterischi (*) che seguono la coppia di asterischi iniziale (\*\*) non sono necessarie.  

```javascript  
/**  
    @type {string}  
*/  
const RED = 'FF0000';  

```  

 Nell'esempio seguente viene illustrato come utilizzare il @deprecated tag JSDoc.  

```javascript  
/**  
 * @deprecated since version 2.0  
 */  
function old() {  
}  
```



