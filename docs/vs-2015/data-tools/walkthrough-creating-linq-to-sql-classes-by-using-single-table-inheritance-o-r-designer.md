---
title: 'Procedura dettagliata: Creazione di classi LINQ to SQL tramite ereditarietà a tabella singola (O-R Designer) | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 63bc6328-e0df-4655-9ce3-5ff74dbf69a4
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5afa250189ffc3b7eda41d567a5c9684a2c8550f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/22/2018
ms.locfileid: "47520253"
---
# <a name="walkthrough-creating-linq-to-sql-classes-by-using-single-table-inheritance-or-designer"></a>Procedura dettagliata: creazione di classi LINQ to SQL tramite ereditarietà a una sola tabella (O/R Designer)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versione più recente di questo argomento è reperibile in [procedura dettagliata: creazione di classi LINQ to SQL da tramite ereditarietà a tabella singola (O-R Designer)](https://docs.microsoft.com/visualstudio/data-tools/walkthrough-creating-linq-to-sql-classes-by-using-single-table-inheritance-o-r-designer).  
  
  
Il [strumenti LINQ to SQL in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md) supporta l'ereditarietà a tabella singola come viene in genere implementato nei sistemi relazionali. Questa procedura dettagliata espande i passaggi generici specificati nel [procedura: configurare l'ereditarietà tramite O/R Designer](../data-tools/how-to-configure-inheritance-by-using-the-o-r-designer.md) argomento e fornisce alcuni dati reali per illustrare l'uso dell'ereditarietà nel [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)].  
  
 In particolare, verranno illustrate le attività seguenti:  
  
-   Creazione di una tabella di database e aggiunta di dati ad essa.  
  
-   Creazione di un'applicazione Windows Form.  
  
-   Aggiunta di un file [!INCLUDE[vbtecdlinq](../includes/vbtecdlinq-md.md)] a un progetto.  
  
-   Creazione di nuove classi di entità.  
  
-   Configurazione delle classi di entità per l'uso dell'ereditarietà.  
  
-   Esecuzione di una query sulla classe ereditata.  
  
-   Visualizzazione dei dati in un Windows Form.  
  
## <a name="create-a-table-to-inherit-from"></a>Creazione di una tabella da cui ereditare  
 Per verificare il funzionamento dell'ereditarietà, verrà creata una piccola tabella Person, usata come classe di base, e verrà creato quindi un oggetto Employee che eredita dalla tabella.  
  
#### <a name="to-create-a-base-table-to-demonstrate-inheritance"></a>Per creare una tabella di base per l'illustrazione dell'ereditarietà  
  
1.  Nelle **Esplora Server**/**Esplora Database**, fare doppio clic il **tabelle** nodo e fare clic su **Aggiungi nuova tabella**.  
  
    > [!NOTE]
    >  È possibile usare il database Northwind o qualsiasi altro database a cui sia possibile aggiungere una tabella.  
  
2.  In Progettazione tabelle aggiungere le seguenti colonne alla tabella:  
  
    |Nome colonna|Tipo di dati|Ammetti Null|  
    |-----------------|---------------|-----------------|  
    |**ID**|**int**|**False**|  
    |**Type**|**int**|**True**|  
    |**firstName**|**nvarchar(200)**|**False**|  
    |**Cognome**|**nvarchar(200)**|**False**|  
    |**Manager**|**int**|**True**|  
  
3.  Impostare la colonna ID come chiave primaria.  
  
4.  Salvataggio della tabella e denominarla **persona**.  
  
## <a name="add-data-to-the-table"></a>Aggiunta di dati alla tabella  
 Allo scopo di verificare che l'ereditarietà sia configurata correttamente, è necessario aggiungere alcuni dati alla tabella per ogni classe nell'ereditarietà a tabella singola.  
  
#### <a name="to-add-data-to-the-table"></a>Per aggiungere dati alla tabella  
  
1.  Aprire la tabella nella visualizzazione dati (Fare doppio clic il **Person** nella tabella **Esplora Server**/**Esplora Database** e fare clic su **Mostra dati tabella**.)  
  
2.  Copiare i dati riportati di seguito nella tabella (È possibile copiarlo e incollarlo nella tabella selezionando l'intera riga nel riquadro dei risultati.)  
  
    ||||||  
    |-|-|-|-|-|  
    |**ID**|**Type**|**firstName**|**Cognome**|**Manager**|  
    |**1**|**1**|**Anne**|**Wallace**|**NULL**|  
    |**2**|**1**|**Carlos**|**Grilo**|**NULL**|  
    |**3**|**1**|**Yael**|**Peled**|**NULL**|  
    |**4**|**2**|**Gatis**|**Ozolins**|**1**|  
    |**5**|**2**|**Andreas**|**Luca Argentiero**|**1**|  
    |**6**|**2**|**Tiffany**|**Phuvasate**|**1**|  
    |**7**|**2**|**Alexey**|**Orekhov**|**2**|  
    |**8**|**2**|**Michał**|**Poliszkiewicz**|**2**|  
    |**9**|**2**|**Tai**|**Yee**|**2**|  
    |**10**|**2**|**Fabricio**|**Noriega**|**3**|  
    |**11**|**2**|**Barbara**|**Martin**|**3**|  
    |**12**|**2**|**Davide**|**Kwok**|**3**|  
  
## <a name="create-a-new-project"></a>Creazione di un nuovo progetto  
 Una volta creata la tabella, creare un nuovo progetto per illustrare la configurazione dell'ereditarietà.  
  
#### <a name="to-create-the-new-windows-application"></a>Per creare la nuova applicazione Windows  
  
1.  Dal **File** menu, creare un nuovo progetto.  
  
2.  Denominare il progetto **InheritanceWalkthrough**.  
  
    > [!NOTE]
    >  [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] è supportato nei progetti Visual Basic e C#. Creare il nuovo progetto in uno di questi linguaggi  
  
3.  Scegliere il **Windows Forms Application** modello e quindi fare clic su **OK**. Per altre informazioni, vedere [le applicazioni Client](http://msdn.microsoft.com/library/2dfb50b7-5af2-4e12-9bbb-c5ade0e39a68).  
  
4.  Il progetto InheritanceWalkthrough viene creato e aggiunto alla **Esplora soluzioni**.  
  
## <a name="add-a-linq-to-sql-classes-file-to-the-project"></a>Aggiunta di un file di classi LINQ to SQL al progetto  
  
#### <a name="to-add-a-linq-to-sql-file-to-the-project"></a>Per aggiungere un file LINQ to SQL al progetto  
  
1.  Nel menu **Progetto** fare clic su **Aggiungi nuovo elemento**.  
  
2.  Scegliere il **classi LINQ to SQL** modello e quindi fare clic su **Add**.  
  
     Il file .dbml viene aggiunto al progetto e viene aperto [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)].  
  
## <a name="create-the-inheritance-by-using-the-or-designer"></a>Creazione dell'ereditarietà usando Progettazione relazionale oggetti  
 Configurare l'ereditarietà trascinando un' **ereditarietà** dell'oggetto dalle **della casella degli strumenti** nell'area di progettazione.  
  
#### <a name="to-create-the-inheritance"></a>Per creare l'ereditarietà  
  
1.  Nelle **Esplora Server**/**Esplora Database**, passare alla **persona** tabella creata in precedenza.  
  
2.  Trascinare il **Person** tabella il [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] nell'area di progettazione.  
  
3.  Trascinare una seconda **Person** tabella le [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] e modificarne il nome in **dipendente**.  
  
4.  Eliminare il **Manager** proprietà dalle **persona** oggetto.  
  
5.  Eliminare il **tipo**, **ID**, **FirstName**, e **LastName** proprietà dal **dipendente** oggetto. (In altre parole, eliminare tutte le proprietà, ad eccezione di **Manager**.)  
  
6.  Dal **Object Relational Designer** scheda della finestra di **della casella degli strumenti**, creare un **ereditarietà** tra il **persona** e  **Employee** oggetti. A tale scopo, fare clic sui **ereditarietà** degli elementi nella **della casella degli strumenti** e rilasciare il pulsante del mouse. Successivamente, fare clic il **dipendente** oggetto e quindi la **persona** dell'oggetto nel [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)]. La freccia della linea di ereditarietà punterà il **persona** oggetto.  
  
7.  Scegliere il **ereditarietà** nell'area di progettazione.  
  
8.  Impostare il **proprietà Discriminator** proprietà **tipo**.  
  
9. Impostare il **Derived Class Discriminator Value** proprietà **2**.  
  
10. Impostare il **Base Class Discriminator Value** proprietà **1**.  
  
11. Impostare il **valore predefinito di ereditarietà** proprietà **persona**.  
  
12. Compilare il progetto.  
  
## <a name="query-the-inherited-class-and-display-the-data-on-the-form"></a>Esecuzione di una query sulla classe ereditata e visualizzazione dei dati nel form  
 A questo punto si aggiungerà codice al form che esegue una query per una classe specifica nel modello a oggetti.  
  
#### <a name="to-create-a-linq-query-and-display-the-results-on-the-form"></a>Per creare una query LINQ e visualizzare i risultati nel form  
  
1.  Trascinare un **ListBox** in Form1.  
  
2.  Fare doppio clic sul form per creare un gestore dell'evento `Form1_Load`.  
  
3.  Aggiungere il codice seguente al gestore eventi `Form1_Load`:  
  
    ```vb  
    Dim dc As New DataClasses1DataContext  
    Dim results = From emp In dc.Persons _  
        Where TypeOf emp Is Employee _  
        Select emp  
  
    For Each Emp As Employee In results  
        ListBox1.Items.Add(Emp.LastName)  
    Next  
    ```  
  
    ```csharp  
    NorthwindDataContext dc = new DataClasses1DataContext();  
    var results = from emp in dc.Persons  
                  where emp is Employee  
                  select emp;  
  
    foreach(Employee Emp in results)  
    {  
        listBox1.Items.Add(Emp.LastName)  
    }  
    ```  
  
## <a name="test-the-application"></a>Test dell'applicazione  
 Eseguire l'applicazione e verificare che i record visualizzati nella casella di riepilogo rappresentino tutti i dipendenti (record che presentano il valore 2 nella rispettiva colonna Type).  
  
#### <a name="to-test-the-application"></a>Per eseguire il test dell'applicazione  
  
1.  Premere F5.  
  
2.  Verificare che siano visualizzati solo i record che presentano il valore 2 nella rispettiva colonna Type.  
  
3.  Chiudere il form. (Nelle **Debug** menu, fare clic su **arresta debug**.)  
  
## <a name="see-also"></a>Vedere anche  
 [Strumenti LINQ to SQL in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [Procedura: aggiungere LINQ to SQL classi a un progetto (O-R Designer)](http://msdn.microsoft.com/library/7bb184ab-ec54-4cda-b706-604b2b4a3ed6)   
 [Procedura dettagliata: Creazione di classi LINQ to SQL (O-R Designer)](http://msdn.microsoft.com/library/35aad4a4-2e8a-46e2-ae09-5fbfd333c233)   
 [Procedura: assegnare stored procedure per eseguire aggiornamenti, inserimenti ed eliminazioni (O/R Designer)](../data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer.md)   
 [LINQ to SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)   
 [Procedura: Generare il modello a oggetti in Visual Basic o C#](http://msdn.microsoft.com/library/a0c73b33-5650-420c-b9dc-f49310c201ee)
