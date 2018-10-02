---
title: Debug di un modello di testo T4 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- text templates, troubleshooting
- text templates, debugging
ms.assetid: 0877fdf2-20bf-42da-b3cc-4c5856b80821
caps.latest.revision: 30
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: d04fe451a752c5132a376fd63091aeb6b1ee1f49
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47517452"
---
# <a name="debugging-a-t4-text-template"></a>Debug di un modello di testo T4
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [debug di un modello di testo T4](https://docs.microsoft.com/visualstudio/modeling/debugging-a-t4-text-template).  
  
È possibile impostare i punti di interruzione nei modelli di testo. Per eseguire il debug di un modello di testo in fase di progettazione, salvare il file di modello di testo e quindi scegliere **Debug modello T4** menu di scelta rapida del file in Esplora soluzioni. Per eseguire il debug di un modello di testo in fase di esecuzione, è sufficiente eseguire il debug dell'applicazione a cui appartiene.  
  
 Per eseguire il debug di un modello di testo, è necessario comprendere i passaggi per il processo di trasformazione del modello. Diversi tipi di errori possono verificarsi all'interno di ogni passaggio. I passaggi sono i seguenti.  
  
|Passaggio|Modello in fase di progettazione: quando si verifica|Modello di runtime: quando si verifica|  
|----------|--------------------------------------------|-----------------------------------------|  
|Codice viene generato dal modello di testo.<br /><br /> Errori nelle direttive, o disallineati o soggetti disordered `<#…#>` tag.|Quando si salva il modello o richiama trasformazione del testo.|Quando si salva il modello o richiama trasformazione del testo.|  
|Viene compilato il codice generato.<br /><br /> Errori di compilazione nel codice del modello.|Immediatamente dopo il passaggio precedente.|Con il codice dell'applicazione.|  
|Il codice viene eseguito.<br /><br /> Errori di run-time nel codice del modello.|Immediatamente dopo il passaggio precedente.|Quando l'applicazione viene eseguita e richiama il codice del modello.|  
  
 Nella maggior parte dei casi, i numeri di riga nel codice del modello sono espressi in segnalazione errori. Quando il report di errore fa riferimento a un nome del file temporaneo, la causa è una parentesi non corrispondente nel codice del modello di testo.  
  
 È possibile impostare punti di interruzione nei modelli di testo e il debug nel modo consueto.  
  
## <a name="common-errors-and-fixes"></a>Errori comuni e correzioni  
 Nella tabella seguente sono elencati gli errori più comuni e le relative correzioni.  
  
|Messaggio di errore|Descrizione|Soluzione|  
|-------------------|-----------------|--------------|  
|Non è stato possibile caricare la classe base{0}' da cui trasformazione classe eredita.|Si verifica se non è possibile trovare la classe base specificata nel `inherits` parametro in una direttiva del modello. Il messaggio include il numero di riga della direttiva template.|Assicurarsi che la classe specificata esista e che sia specificato l'assembly cui si trova in una direttiva assembly.|  
|Non è riuscito a risolvere includere testo per il file:{0}|Si verifica quando non è possibile trovare un modello incluso. Il messaggio include il nome del file di inclusione richiesto.|Assicurarsi che il percorso del file è relativo al percorso del modello originale, o che il file sia in un percorso a cui è registrato con l'host o che vi sia un percorso completo del file.|  
|Sono stati generati errori durante l'inizializzazione dell'oggetto trasformazione. La trasformazione non verrà eseguita.|Si verifica quando 'Initialize ()' della classe di trasformazione non è riuscito o ha restituito false.|Il codice nella funzione Initialize () deriva dalla classe di base di trasformazione specificata nella \<&@template& > direttiva e dai processori di direttiva. L'errore che ha causato initialize probabilmente esito negativo è in elenco errori. Esaminare il motivo dell'errore. È possibile esaminare il codice generato effettivo per Initialize (), seguire le procedure per eseguire il debug di un modello.|  
|L'assembly '{0}'per il processore di direttiva'{1}' non è stato concesso il set di autorizzazioni FullTrust. Sono consentiti solo gli assembly attendibili per fornire i processori di direttiva. Questo processore di direttiva non verrà caricato.|Si verifica quando il sistema non concede le autorizzazioni FullTrust per un assembly che contiene un processore di direttiva. Il messaggio include il nome dell'assembly e il nome del processore di direttiva.|Assicurarsi di utilizzare solo assembly attendibili nel computer locale.|  
|Il percorso '{0}' deve essere locale in questo computer o parte dell'area attendibile.|Si verifica quando una direttiva o una direttiva dell'assembly fa riferimento a un file non disponibile nel computer locale o in area attendibile della rete.|Assicurarsi che la directory in cui si trovano la direttiva o direttive dell'assembly sia nell'area attendibile. È possibile aggiungere una directory di rete all'area attendibile tramite Internet Explorer.|  
|Più errori di sintassi come "Non valido token ' catch'" o "uno spazio dei nomi non può contenere direttamente membri"|Troppe parentesi graffe di chiusura nel codice del modello. Il compilatore confonde con il codice di generazione a standard.|Verificare il numero della chiusura di parentesi graffe e parentesi quadre all'interno di delimitatori di codice.|  
|Cicli o istruzioni condizionali non compilato o eseguito correttamente. Ad esempio: `<#if (i>10)#> Number is: <#= i #>`.<br /><br /> Questo codice restituisce sempre il valore della ho. Solo "numero è:" è di tipo condizionale.|In c#, usare sempre le parentesi graffe per racchiudere i blocchi di testo incorporati nelle istruzioni del controllo.|Aggiungi parentesi graffe: `<#if (i>10) { #>    Number is: <#= i #><# } #>`.|  
|"Espressione troppo complesso" durante l'elaborazione di un modello in fase di progettazione o la compilazione di un modello di runtime (pre-elaborato).<br /><br /> [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] smette di funzionare quando si tenta di esaminare il codice generato da un modello di runtime.|Blocco di testo è troppo lungo. Blocchi di testo T4 converte un'espressione di concatenazione di stringa, con un'unica stringa letterale per ogni riga del modello. Blocchi di testo molto lunghi possono oltrepassare i limiti di dimensioni del compilatore.|Suddividere il blocco di testo lungo con un blocco di espressione, ad esempio:<br /><br /> `<#= "" #>`|  
  
## <a name="warning-descriptions-and-fixes"></a>Correzioni e le descrizioni di avviso  
 Nella tabella seguente elenca gli avvisi più comuni insieme alle correzioni, se disponibile.  
  
|Messaggio di avviso|Descrizione|Soluzione|  
|---------------------|-----------------|--------------|  
|Il caricamento del file di inclusione '{0}' ha restituito una stringa null o vuota.|Si verifica se un file di modello testo incluso è vuoto. Il messaggio include il nome del file del file incluso.|Rimuovere la direttiva include oppure assicurarsi che il file sia parte del contenuto.|  
|Compilazione della trasformazione:|Antepone la stringa a tutti gli errori o avvisi provenienti dal compilatore durante la compilazione della trasformazione. Questa stringa indica che il compilatore ha generato un errore o avviso.|Se si dispone di un problema durante la ricerca della DLL, si potrebbe dover fornire il percorso completo o un nome completo sicuro se la DLL si trovi nella Global Assembly Cache.|  
|Il parametro '{0}' esiste già nella direttiva. Il parametro duplicato verrà ignorato.|Si verifica quando un parametro è specificato più volte in una direttiva. Il messaggio include il nome del parametro e il numero di riga della direttiva.|Rimuovere la specifica del parametro duplicato.|  
|Si è verificato un errore durante il caricamento del file di inclusione '{0}'. La direttiva include verrà ignorata.|Si verifica quando non è possibile trovare un file specificato un `include` direttiva. Il messaggio include il nome del file e il numero di riga della direttiva.|Assicurarsi che il file di inclusione è presente nella stessa directory del file di modello testo originale o in una delle directory di inclusione che sono registrate con l'host.|  
|Una classe di base non valida specificata per la classe Transformation. La classe di base deve derivare da TextTransformation.|Si verifica quando la `inherits` parametro in una direttiva del modello specifica una classe che eredita da `TextTransformation`. Il messaggio include il numero di riga della direttiva template.|Specificare una classe che deriva da `TextTransformation`.|  
|È stata specificata una lingua non valida nella direttiva 'template'. Le impostazioni cultura deve essere nel formato "xx-XX". Verrà utilizzata la lingua inglese.|Si verifica quando il parametro delle impostazioni cultura in una direttiva template è stato specificato correttamente. Il messaggio include il numero di riga della direttiva template.|Modificare il parametro delle impostazioni cultura per una lingua valida nel formato "xx-XX".|  
|Un valore di debug non valido '{0}' è stata specificata nella direttiva del modello. Il valore di debug deve essere "true" o "false". Verrà utilizzato il valore predefinito è "false".|Si verifica quando il `debug` parametro in una direttiva template è stato specificato correttamente. Il messaggio include il numero di riga della direttiva template.|Il parametro di debug impostato su "true" o "false".|  
|Un valore di HostSpecific non valido '{0}' è stata specificata nella direttiva del modello. Il valore di HostSpecific deve essere "true" o "false". Verrà utilizzato il valore predefinito è "false".|Si verifica quando il parametro specifica dell'host in un `template` direttiva è stata specificata correttamente. Il messaggio include il numero di riga della direttiva template.|Il parametro specifica dell'host può essere impostato su "true" o "false".|  
|Un linguaggio non valido '{0}' è stata specificata nella direttiva 'template'. La lingua deve essere "C#" o "VB". Verrà utilizzato il valore predefinito "C#".|Si verifica quando viene specificata una lingua non supportata nel `template` direttiva. Sono consentiti solo "C#" o "VB" (maiuscole e minuscole). Il messaggio include il numero di riga della direttiva template.|Impostare il `language` parametro nella direttiva del modello a "C#" o "VB".|  
|Nel modello sono state trovate più direttive output. Tutti tranne il primo verranno ignorati.|Si verifica quando più `output` direttive sono specificate in un file di modello. Il messaggio include il numero di riga della direttiva output duplicati.|Rimuovere duplicato `output` direttive.|  
|Nel modello sono state trovate più direttive di modello. Tutti tranne il primo verranno ignorati. All'interno di un'unica direttiva template, è necessario specificare più parametri della direttiva template.|Si verifica se si specificano più `template` direttive all'interno di un file di modello di testo (inclusi i file inclusi). Il messaggio include il numero di riga della direttiva template duplicati.|Aggregare i diversi `template` direttive in un unico `template` direttiva.|  
|È stato specificato alcun processore per la direttiva denominata '{0}'. La direttiva verrà ignorata.|Si verifica se si specifica un `custom` direttiva, ma non forniscono un `processor` attributo. Il messaggio include il nome della direttiva e il numero di riga.|Fornire una `processor` con il nome dell'attributo il `directive` processore per la direttiva.|  
|Un processore denominato '{0}'non è stato trovato per la direttiva denominata'{1}'. La direttiva verrà ignorata.|Si verifica quando il sistema non è stato trovato il `directive` processore specificato all'interno di un `custom` direttiva. Il messaggio include il nome della direttiva, nome del processore e il numero di riga della direttiva.|Impostare il `processor` attributo della direttiva per il nome del processore di direttiva.|  
|Un parametro obbligatorio '{0}'per la direttiva'{1}' non è stato trovato. La direttiva verrà ignorata.|Si verifica quando il sistema non è incluso un parametro di direttiva obbligatorio. Il messaggio include il nome del parametro mancano, il nome della direttiva e il numero di riga.|Specificare il parametro mancante.|  
|Il processore denominato '{0}'non supporta la direttiva denominata'{1}'. La direttiva verrà ignorata.|Si verifica quando un processore di direttiva non supporta una direttiva. Il messaggio include il numero di riga e il nome della direttiva che causa l'errore insieme al nome del processore di direttiva.|Correggere il nome della direttiva.|  
|La direttiva include per il file '{0}' causa un ciclo infinito.|Visualizzata se direttive includono circolari vengono specificati (ad esempio, il file include file B, che include il file).|Non si specifica circolare le direttive di inclusione.|  
|Esecuzione della trasformazione:|Antepone la stringa a tutti gli errori o avvisi generati durante l'esecuzione della trasformazione.|Non applicabile.|  
|È stato trovato un tag di inizio o fine imprevisto all'interno di un blocco. Assicurarsi che non sia stato digitato erroneamente un tag di inizio o alla fine e che non hai tutti i blocchi annidati nel modello.|Visualizzato quando si dispone di un'eccezione imprevista \<# o #>. Vale a dire, se hai un \<& dopo un altro tag di apertura che non è stato chiuso, oppure l'utente dispone di un simbolo #> quando è presente alcun tag di apertura non chiusa prima di esso. Il messaggio include il numero di riga del tag non corrispondenti.|Rimuovere il tag di inizio o fine non corrispondente o usare un carattere di escape.|  
|È stata specificata una direttiva in un formato non corretto. La direttiva verrà ignorata. Specificare la direttiva nel formato `<#@ name [parametername="parametervalue"]*  #>`|Se non si specifica una direttiva nel formato corretto, visualizzato dal parser. Il messaggio include il numero di riga della direttiva non corretto.|Verificare che tutte le direttive sono nel formato `<#@ name [parametername="parametervalue"]*  #>`. Per altre informazioni, vedere [direttive di modello di testo T4](../modeling/t4-text-template-directives.md).|  
|Non è stato possibile caricare l'Assembly '{0}'per il processore di direttiva registrato'{1}'<br /><br /> {2}|Si verifica quando un processore di direttiva non è stato possibile caricare dall'host. Il messaggio identifica l'assembly fornito per il processore di direttiva e il nome del processore di direttiva.|Assicurarsi che il processore di direttiva sia registrato correttamente e che sia presente l'assembly.|  
|Non è riuscito a trovare il tipo '{0}'nell'Assembly'{1}'per il processore di direttiva registrato'{2}'<br /><br /> {3}|Si verifica quando un tipo di processore di direttiva potrebbe non essere caricato dall'assembly. Il messaggio include il nome del tipo, assembly e processore di direttiva.|Vshost Trova informazioni processore di direttiva (nome assembly e tipo) nel Registro di sistema. Assicurarsi che il processore di direttiva sia registrato correttamente e che il tipo presente nell'assembly.|  
|Si è verificato un problema durante il caricamento dell'assembly '{0}'|Si verifica quando si verifica un problema durante il caricamento di un assembly. Il messaggio include il nome dell'assembly.|È possibile specificare gli assembly da caricare in \<@# assembly #> direttive e dai processori di direttiva. Il messaggio di errore che segue questa stringa deve fornire ulteriori dati sul motivo per cui il caricamento dell'assembly non riuscita.|  
|Si è verificato un problema durante la creazione e l'inizializzazione del processore di direttiva denominato '{1}'. Il tipo del processore è {0}. La direttiva verrà ignorata.|Si verifica quando il sistema non è stato possibile creare o inizializzare un processore di direttiva. Il messaggio include il numero di riga e il nome della direttiva e il tipo di processore.|Assicurarsi che usi il processore di direttiva corretto e che il processore di direttiva abbia un costruttore predefinito pubblico. Per scoprire il motivo per cui il metodo Initialize () del processore di direttiva non è possibile eseguire in caso contrario, utilizzare le opzioni di debug. Per altre informazioni, vedere [risoluzione dei problemi di modelli di testo](../modeling/debugging-a-t4-text-template.md).|  
|È stata generata un'eccezione durante l'elaborazione di una direttiva denominata '{0}'.|Si verifica quando un processore di direttiva genera un'eccezione durante l'elaborazione di una direttiva.|Assicurarsi che i parametri al processore di direttiva siano corretti.|  
|L'host ha generato un'eccezione durante il tentativo di risolvere il riferimento all'assembly '{0}'.|Si verifica quando l'host genera un'eccezione quando tenta di risolvere un riferimento all'assembly. Il messaggio include l'assembly di riferimento stringa.|Assembly riferimenti provenire da \<@# assembly #> direttive e dai processori di direttiva. Assicurarsi che il parametro 'name' fornito dal parametro assembly sia corretto.|  
|Provare a specificare non supportata {1} valore '{0}' per la direttiva {2}|Si verifica con RequiresProvidesDirectiveProcessor (tutti i processori di direttiva generati in modo derivano), quando si fornisce un non supportato richiede o include argomenti.|Assicurarsi che i nomi in name = 'value' specificate coppie di richiede e fornisce i parametri siano corretti.|


