---
title: Eseguire il binding ai dati nella finestra di progettazione XAML
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- VS.XamlDesigner.DataBinding
dev_langs:
- CSharp
- VB
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- uwp
ms.openlocfilehash: f0d9ccd32c8f616e6f998bcd1f31773460c89a20
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53866124"
---
# <a name="walkthrough-bind-to-data-in-xaml-designer"></a>Procedura dettagliata: Eseguire il binding ai dati nella finestra di progettazione XAML

Nella finestra di progettazione XAML è possibile impostare le proprietà di data binding mediante la tavola da disegno e la finestra Proprietà. Questa procedura dettagliata illustra come associare dati a un controllo. In particolare, la procedura dettagliata illustra come creare una classe di carrello semplice con una classe [DependencyProperty](/uwp/api/Windows.UI.Xaml.DependencyProperty) denominata `ItemCount` e associare la proprietà `ItemCount` alla proprietà **Text** di un controllo [TextBlock](/uwp/api/Windows.UI.Xaml.Controls.TextBlock).

## <a name="to-create-a-class-to-use-as-a-data-source"></a>Per creare una classe da usare come origine dati

1. Nel menu **File** scegliere **Nuovo** > **Progetto**.

1. Nella finestra di dialogo **Nuovo progetto** scegliere il nodo **Visual C#** o **Visual Basic**, espandere il nodo **Desktop di Windows** e scegliere il modello **Applicazione WPF**.

1. Assegnare al progetto il nome **BindingTest** e fare clic sul pulsante **OK**.

1. Aprire il file **MainWindow.xaml.cs** (o **MainWindow.xaml.vb**) e aggiungere il codice seguente. In C# aggiungere il codice nello spazio dei nomi `BindingTest` (prima della parentesi chiusa finale nel file). In Visual Basic, è sufficiente aggiungere la nuova classe.

   ```csharp
   public class ShoppingCart : DependencyObject
   {
       public int ItemCount
       {
           get { return (int)GetValue(ItemCountProperty); }
           set { SetValue(ItemCountProperty, value); }
       }

       public static readonly DependencyProperty ItemCountProperty =
            DependencyProperty.Register("ItemCount", typeof(int),
            typeof(ShoppingCart), new PropertyMetadata(0));
   }
   ```

   ```vb
   Public Class ShoppingCart
       Inherits DependencyObject

       Public Shared ReadOnly ItemCountProperty As DependencyProperty = DependencyProperty.Register(
            "ItemCount", GetType(Integer), GetType(ShoppingCart), New PropertyMetadata(0))
       Public Property ItemCount As Integer
           Get
               ItemCount = CType(GetValue(ItemCountProperty), Integer)
           End Get
           Set(value As Integer)
               SetValue(ItemCountProperty, value)
           End Set
       End Property
   End Class
   ```

   Questo codice imposta un valore 0 come numero predefinito dell'elemento usando l'oggetto [PropertyMetadata](/uwp/api/Windows.UI.Xaml.PropertyMetadata).

1. Scegliere **Compila** > **Compila soluzione** dal menu **File**.

## <a name="to-bind-the-itemcount-property-to-a-textblock-control"></a>Per associare la proprietà ItemCount a un controllo TextBlock

1. In Esplora soluzioni aprire il menu di scelta rapida per **MainWindow.xaml** e scegliere **Progettazione visualizzazioni**.

1. Nella casella degli strumenti scegliere un controllo [Grid](/uwp/api/Windows.UI.Xaml.Controls.Grid) e aggiungerlo al modulo.

1. Dopo aver selezionato il controllo `Grid` fare clic sul pulsante **Nuovo** accanto alla proprietà **DataContext** nella finestra Proprietà.

1. Nella finestra di dialogo **Seleziona oggetto** verificare che la casella di controllo **Mostra tutti gli assembly** sia deselezionata, scegliere **ShoppingCart** nello spazio dei nomi **BindingTest** e fare clic sul pulsante **OK**.

     La figura seguente illustra la finestra di dialogo **Seleziona oggetto** con **ShoppingCart** selezionato.

     ![Finestra di dialogo Seleziona oggetto](../designers/media/blendselectobject.png)

1. Nella **casella degli strumenti`TextBlock` scegliere un controllo**  e aggiungerlo al modulo.

1. Dopo aver selezionato il controllo `TextBlock`, scegliere il marcatore della proprietà a destra della proprietà **Text** e scegliere **Crea associazione dati**. Il marcatore della proprietà ha l'aspetto di una piccola casella.

1. Nella casella **Percorso** della finestra di dialogo Crea associazione dati scegliere la proprietà **ItemCount : (int32)** e fare clic sul pulsante **OK**.

     La figura seguente illustra la finestra di dialogo **Crea associazione dati** con la proprietà **ItemCount** selezionata.

     ![Finestra di dialogo Crea data binding](../designers/media/xaml_create_data_binding.png)

1. Premere **F5** per eseguire l'app.

     Il controllo `TextBlock` dovrebbe ora visualizzare il valore predefinito 0 come testo.

## <a name="see-also"></a>Vedere anche

- [Creare un'interfaccia utente tramite la finestra di progettazione XAML](../designers/creating-a-ui-by-using-xaml-designer-in-visual-studio.md)
- [Finestra di dialogo Aggiungi convertitore di valori](https://msdn.microsoft.com/library/c5f3d110-a541-4b55-8bca-928f77778af8)