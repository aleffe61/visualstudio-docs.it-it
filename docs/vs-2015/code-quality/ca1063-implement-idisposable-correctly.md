---
title: 'CA1063: Implementare IDisposable correttamente | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- ImplementIDisposableCorrectly
- CA1063
helpviewer_keywords:
- CA1063
- ImplementIDisposableCorrectly
ms.assetid: 12afb1ea-3a17-4a3f-a1f0-fcdb853e2359
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 94d13514800bac80723031c6bba7920d28ac83e6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2018
ms.locfileid: "49877296"
---
# <a name="ca1063-implement-idisposable-correctly"></a>CA1063: Implementare IDisposable correttamente
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ImplementIDisposableCorrectly|
|CheckId|CA1063|
|Category|Microsoft.Design|
|Modifica importante|Non sostanziale|

## <a name="cause"></a>Causa
 `IDisposable` non è implementata correttamente. Di seguito sono elencati alcuni dei motivi per questo problema:

- IDisposable è nuovamente implementate nella classe.

- Completare nuovamente sottoposto a override.

- Viene eseguito l'override di Dispose.

- Dispose () non è pubblico, sealed o denominato Dispose.

- Dispose (bool) non è protetto, virtuale o non sealed.

- Nei tipi non sealed, Dispose () devono chiamare Dispose (true).

- Per i tipi unsealed, l'implementazione di Finalize non chiama Dispose (bool) o il finalizzatore della classe base.

  Violazione di uno di questi modelli attiverà questo avviso.

  Ogni radice non sealed Tipo IDisposable debba fornire il proprio metodo Dispose (bool) di void virtuale protetto. Dispose () devono chiamare Dispose (true) e Finalize deve chiamare Dispose (false). Se si sta creando un tipo IDisposable radice non bloccato, è necessario definire Dispose (bool) e chiamarlo. Per altre informazioni, vedere [pulizia di risorse non gestite](http://msdn.microsoft.com/library/a17b0066-71c2-4ba4-9822-8e19332fc213) nel [linee guida di progettazione di Framework](http://msdn.microsoft.com/library/5fbcaf4f-ea2a-4d20-b0d6-e61dee202b4b) sezione della documentazione di .NET Framework.

## <a name="rule-description"></a>Descrizione della regola
 È necessario che tutti i tipi IDisposable implementino correttamente il modello Dispose.

## <a name="how-to-fix-violations"></a>Come correggere le violazioni
 Esaminare il codice e determinare quale delle seguenti soluzioni risolverà questa violazione.

-   Rimuovere IDisposable dall'elenco delle interfacce implementate da {0} ed eseguire l'override dell'implementazione Dispose della classe base.

-   Rimuovere il finalizzatore dal tipo {0}, eseguire l'override di Dispose (bool disposing) e inserire la logica di finalizzazione nel percorso del codice dove 'disposing' è false.

-   Rimuovere {0}, eseguire l'override di Dispose (bool disposing) e inserire la logica di dispose nel percorso del codice dove 'disposing' è true.

-   Assicurarsi che {0} viene dichiarato come pubblico e sealed.

-   Rinominare {0} in 'Dispose' e assicurarsi che sia dichiarato public e sealed.

-   Verificare che l'opzione {0} è dichiarato come protected, virtual e unsealed.

-   Modificare {0} in modo che chiami Dispose (true), quindi chiama GC. SuppressFinalize nell'istanza dell'oggetto corrente ('this' o 'Me' in [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]) e poi restituisce.

-   Modificare {0} in modo che chiami Dispose (false) e quindi restituisce.

-   Se si sta scrivendo una classe di IDisposable radice non bloccato, assicurarsi che l'implementazione di IDisposable segue il modello che è descritti in precedenza in questa sezione.

## <a name="when-to-suppress-warnings"></a>Esclusione di avvisi
 Non escludere un avviso da questa regola.

## <a name="pseudo-code-example"></a>Esempio di pseudocodice
 Il pseudo-codice seguente viene fornito un esempio generale di come Dispose (bool) deve essere implementata in una classe che usa gestita e le risorse native.

```
public class Resource : IDisposable
{
    private IntPtr nativeResource = Marshal.AllocHGlobal(100);
    private AnotherResource managedResource = new AnotherResource();

// Dispose() calls Dispose(true)
    public void Dispose()
    {
        Dispose(true);
        GC.SuppressFinalize(this);
    }
    // NOTE: Leave out the finalizer altogether if this class doesn't
    // own unmanaged resources itself, but leave the other methods
    // exactly as they are.
    ~Resource()
    {
        // Finalizer calls Dispose(false)
        Dispose(false);
    }
    // The bulk of the clean-up code is implemented in Dispose(bool)
    protected virtual void Dispose(bool disposing)
    {
        if (disposing)
        {
            // free managed resources
            if (managedResource != null)
            {
                managedResource.Dispose();
                managedResource = null;
            }
        }
        // free native resources if there are any.
        if (nativeResource != IntPtr.Zero)
        {
            Marshal.FreeHGlobal(nativeResource);
            nativeResource = IntPtr.Zero;
        }
    }
}
```



