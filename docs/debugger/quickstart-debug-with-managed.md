---
title: Eseguire il debug di codice gestito | Microsoft Docs
description: Eseguire il debug di C# o Visual Basic usando il debugger di Visual Studio
ms.custom: mvc
ms.date: 03/18/2018
ms.topic: quickstart
helpviewer_keywords:
- debugger
ms.assetid: f4cea2e1-08dc-47ac-aba2-3b8c338e607f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: d6b4f6fecabe7947e59a235dbb71e9f5e0803b10
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53955477"
---
# <a name="quickstart-debug-with-c-or-visual-basic-using-the-visual-studio-debugger"></a>Guida introduttiva: Eseguire il debug con C# o Visual Basic usando il debugger di Visual Studio

Il debugger di Visual Studio propone molte funzionalità potenti per il debug delle app. Questo argomento consente di apprendere in modo rapido come usare alcune funzionalità di base.

## <a name="create-a-new-project"></a>Creare un nuovo progetto 

1. In Visual Studio scegliere **File > Nuovo progetto**.

2. In **Visual C#** o **Visual Basic** scegliere **.NET Core** e quindi nel riquadro al centro scegliere **App console (.NET Core)**.

     Se non viene visualizzato il modello di progetto **Console App (.NET Core)** (App console (.NET Core)), fare clic sul collegamento **Apri il programma di installazione di Visual Studio** nel riquadro sinistro della finestra di dialogo **Nuovo progetto**. Verrà avviato il Programma di installazione di Visual Studio. Scegliere il carico di lavoro **Sviluppo per desktop .NET** e **.NET Core**, quindi scegliere **Modifica**.

3. Digitare un nome come **MyDbgApp** e fare clic su **OK**.

    Visual Studio crea il progetto.

4. In *Program.cs* o *Module1.vb* sostituire il codice seguente

    ```csharp
    class Program
    {
        static void Main(string[] args)
        {
        }
    }
    ```

    ```vb
    Module Module1
        Sub Main()
        End Sub
    End Module
    ```

    con questo codice:

    ```csharp
    class Program
    {
        private static void doWork()
        {
            LinkedList<int> c1 = new LinkedList<int>();

            c1.AddLast(10);
            c1.AddLast(20);

            LinkedList<int> c2 = new LinkedList<int>(c1);
            int i = c2.First.Value;
            int j = c2.First.Value;
            Console.Write("The first element is ");
            Console.Write(i);
            Console.Write("\n");
            Console.Write("The second element is ");
            Console.Write(j);
            Console.Write("\n");

        }

        static int Main()
        {
            // using namespace std;
            doWork();
            return 0;

        }
    }
    ```

    ```vb
    Imports System.Collections.Generic

    Namespace MyDbgApp
        Class Program
            Private Shared Sub doWork()
                Dim c1 As New LinkedList(Of Integer)()

                c1.AddLast(10)
                c1.AddLast(20)

                Dim c2 As New LinkedList(Of Integer)(c1)
                Dim i As Integer = c2.First.Value
                Dim j As Integer = c2.First.Value
                Console.Write("The first element is ")
                Console.Write(i)
                Console.Write(vbLf)
                Console.Write("The second element is ")
                Console.Write(j)
                Console.Write(vbLf)

            End Sub

            Public Shared Function Main() As Integer
                ' using namespace std;
                doWork()
                Return 0

            End Function
        End Class
    End Namespace
    ```

    > [!NOTE]
    > In Visual Basic verificare che l'oggetto di avvio sia impostato su `Sub Main` (**Proprietà > Applicazione > Oggetto di avvio**).

## <a name="set-a-breakpoint"></a>Imposta punto di interruzione

Un *punto di interruzione* è un indicatore che segnala il punto in cui Visual Studio dovrebbe sospendere l'esecuzione del codice in modo da poter esaminare i valori delle variabili, il comportamento della memoria o lo stato di esecuzione di un ramo del codice. È la più semplice funzionalità di debug.

1. Per impostare il punto di interruzione, fare clic nella barra di navigazione a sinistra della chiamata di funzione `doWork` o selezionare la riga di codice e premere **F9**.

    ![Impostare un punto di interruzione](../debugger/media/dbg-qs-set-breakpoint-csharp.png "Impostare un punto di interruzione")

2. Premere **F5** o scegliere **Debug > Avvia debug**.

    ![Raggiungere un punto di interruzione](../debugger/media/dbg-qs-hit-breakpoint-csharp.png "Raggiungere un punto di interruzione")

    Il debugger si ferma in corrispondenza del punto di interruzione impostato. L'istruzione in corrispondenza della quale si è bloccato il debugger e si è interrotta l'esecuzione dell'app è indicata dalla freccia gialla. La riga con la chiamata di funzione `doWork` non è stata ancora eseguita.

    > [!TIP]
    > Se è presente un punto di interruzione in un ciclo o in una ricorsione oppure sono presenti molti punti di interruzione in un codice che si esegue di frequente, usare un [punto di interruzione condizionale](../debugger/using-breakpoints.md#BKMK_Specify_a_breakpoint_condition_using_a_code_expression) per fare in modo che il codice venga sospeso SOLO se sono soddisfatte specifiche condizioni. Un punto di interruzione condizionale può fare risparmiare tempo e può facilitare il debug di problemi che sono difficili da riprodurre.

## <a name="navigate-code"></a>Spostarsi all'interno del codice

Sono disponibili diversi comandi per indicare al debugger di continuare. Viene illustrato un comando di spostamento nel codice utile che è stato introdotto in Visual Studio 2017.

Mentre l'elaborazione è ferma al punto di interruzione, passare il mouse sopra l'istruzione `c1.AddLast(20)` finché appare il pulsante verde **Esegui fino alla riga selezionata** ![Esegui fino alla riga selezionata](../debugger/media/dbg-tour-run-to-click.png "RunToClick") quindi premere il pulsante **Esegui fino alla riga selezionata**.

![Esegui fino alla riga selezionata](../debugger/media/dbg-qs-run-to-click-csharp.png "Esegui fino alla riga selezionata")

L'app riprende l'esecuzione, esegue la chiamata a `doWork` e si blocca sulla riga di codice in cui si è fatto clic.

I comandi della tastiera comuni usati per eseguire il codice sono **F10** e **F11**. Per altre istruzioni dettagliate, vedere [Presentazione del debugger](../debugger/debugger-feature-tour.md).

## <a name="inspect-variables-in-a-datatip"></a>Esaminare le variabili in un suggerimento dati

1. Nella riga corrente del codice, segnalata dal puntatore di esecuzione giallo, passare il mouse sopra l'oggetto `c1` per visualizzare un suggerimento dati.

    ![Visualizzare un suggerimento dati](../debugger/media/dbg-qs-data-tip-csharp.png "Visualizzare un suggerimento dati")

    Il suggerimento dati mostra il valore corrente della variabile `c1` e consente di controllarne le proprietà. Se viene visualizzato un valore non previsto durante il debug, è probabile che ci sia un bug nelle righe di codice precedenti o chiamate. 

2. Espandere il suggerimento dati per esaminare i valori delle proprietà dell'oggetto `c1`.

3. Se si preferisce bloccare il suggerimento dati in modo che sia sempre possibile vedere il valore di `c1` mentre si esegue il codice, fare clic sulla piccola icona Aggiungi. Il suggerimento dati aggiunto può essere spostato in una posizione più comoda.

## <a name="edit-code-and-continue-debugging"></a>Modificare il codice e continuare il debug

Se durante una sessione di debug, nel codice si rileva una modifica che si desidera testare, è possibile farlo.

1. Fare clic sulla seconda istanza di `c2.First.Value` e modificare `c2.First.Value` in `c2.Last.Value`.

2. Premere **F10** (o selezionare **Debug > Esegui istruzione/routine**) alcune volte per far avanzare il debugger ed eseguire il codice modificato.

    ![Modifica e continua](../debugger/media/dbg-qs-edit-and-continue-csharp.gif "Modifica e continua")

    **F10** fa avanzare il debugger un'istruzione alla volta, ma ignora le funzioni anziché fermarsi. Il codice ignorato viene comunque eseguito.

Per altre informazioni sull'uso della funzione di modifica e continua e sulle limitazioni della funzionalità, vedere [Modificare il codice e continuare il debug](../debugger/edit-and-continue.md).

## <a name="next-steps"></a>Passaggi successivi

In questa esercitazione si è appreso come avviare il debugger, eseguire il codice ed esaminare le variabili. Sono disponibili una panoramica delle funzionalità del debugger e collegamenti a ulteriori informazioni.

> [!div class="nextstepaction"]
> [Tour delle funzionalità del debugger](../debugger/debugger-feature-tour.md)
