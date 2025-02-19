# Grid: Akasztofa
## Feladat
Solution neve: **WpfApp1**

Projekt leírása:Csinálni kell 2 gridet egyik az a fő grid a másik meg a betűk kiírásához kell.A fő gridet felosztjuk 2x2-re.Az 1 első gridet felhasználjuk a adott szó hosszának megjelenítésére.A 2 gridet a hibák számának megjelenítésére van felhasználva.A 3 griden belűl van még egy grid ami a 
betűkre van felhasználva.A 4 grid meg a jaték nevét tartalmazza.

Működés:Van egy random generált szó ami ki kell találni.

1. Window méretét beállítjuk 750x750-esre
2. Grid: A Grid konténer két fő oszlopot és két fő sort tartalmaz. Az egyik oszlopban jelenik meg a feladvány (kitalálandó szó), a másikban pedig az információs szövegek.
3. A Click eseményre a "BetuGomb_Click" eseménykezelőt állítjuk be minden Buttonra


```C#
<Window x:Class="WpfApp1.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:WpfApp1"
        mc:Ignorable="d"
        Title="MainWindow" Height="750" Width="750">
    <Grid Background="Gainsboro">
        <Grid.ColumnDefinitions>
            <ColumnDefinition />
            <ColumnDefinition />
        </Grid.ColumnDefinitions>
        <Grid.RowDefinitions>
            <RowDefinition />
            <RowDefinition />
        </Grid.RowDefinitions>

        <TextBlock x:Name="PuzzleText" Grid.Column="0" Grid.Row="0" HorizontalAlignment="Center" VerticalAlignment="Center" FontSize="24"/>

        <Grid x:Name="LetterButtonsGrid" Grid.Column="0" Grid.Row="1" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Grid.ColumnDefinitions>
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
            </Grid.ColumnDefinitions>
            <Grid.RowDefinitions>
                <RowDefinition />
                <RowDefinition />
                <RowDefinition />
                <RowDefinition />
                <RowDefinition />
            </Grid.RowDefinitions>

            <Button Content="A" Grid.Row="0" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Á" Grid.Row="0" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="B" Grid.Row="0" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="C" Grid.Row="0" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="D" Grid.Row="0" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="E" Grid.Row="0" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="É" Grid.Row="0" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="F" Grid.Row="1" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="G" Grid.Row="1" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="H" Grid.Row="1" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="I" Grid.Row="1" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Í" Grid.Row="1" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="J" Grid.Row="1" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="K" Grid.Row="1" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="L" Grid.Row="2" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="M" Grid.Row="2" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="N" Grid.Row="2" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="O" Grid.Row="2" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ó" Grid.Row="2" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ö" Grid.Row="2" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ő" Grid.Row="2" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="P" Grid.Row="3" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Q" Grid.Row="3" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="R" Grid.Row="3" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="S" Grid.Row="3" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="T" Grid.Row="3" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="U" Grid.Row="3" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ú" Grid.Row="3" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="Ü" Grid.Row="4" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ű" Grid.Row="4" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="V" Grid.Row="4" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="W" Grid.Row="4" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="X" Grid.Row="4" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Y" Grid.Row="4" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Z" Grid.Row="4" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
        </Grid>

        <TextBlock Grid.Column="1" Grid.Row="1" HorizontalAlignment="Center" VerticalAlignment="Center" FontSize="18" Text="Akasztófa Játék"/>
        <TextBlock x:Name="InfoText" Grid.Column="1" Grid.Row="0" HorizontalAlignment="Center" VerticalAlignment="Center" FontSize="18"/>
        <WrapPanel x:Name="LetterButtonsPanel" HorizontalAlignment="Center" VerticalAlignment="Center" Margin="10"/>

    </Grid>
</Window>

```
1. Grid: A Grid konténer két fő oszlopot és két fő sort tartalmaz. Az egyik oszlopban jelenik meg a feladvány (kitalálandó szó), a másikban pedig az információs szövegek.
2. FeladvanyText: A TextBlock elem, ami a kitalálandó szót jeleníti meg. A betűk helyett "_" (aláhúzás) jelenik meg, amíg nem lettek kitalálva.
3. BetuGombokGrid: Egy Grid elrendezés, amely betűgombokat tartalmaz. A betűgombok (A-Z, Á-Ű) elhelyezése oszlopokban és sorokban történik.
4. InfoText: A hibák számát jelző TextBlock elem, amely mutatja, hogy hány hibát követtek el a játék során.

6. Felveszünk egy amőba nevű mátrixot, és egy player1 boolean változót (ez majd a későbbiekben fog kelleni)

```C#
private int[,] amoba = new int[3, 3] { { 0, 0, 0 }, { 0, 0, 0 }, { 0, 0, 0 } };
private bool player1 = true;
```

7. A Button_Click metódus-ban meg kell állapítani, hogy melyik gombon történt a kattintás, ezt az object típusú sender paraméter tartalmazza. Az object típus lehetővé teszi, hogy bármilyen típusú objektumot átadjunk az eseménykezelőnek, mert minden típus az object típusból származik, így az object típusú referencia bármilyen típusú objektumra mutathat. Az eseménykezelőn belül típuskonverziót végzünk a sender paraméteren, hogy a konkrét típusú objektumhoz férjünk hozzá. Például, ha a sender egy gomb, akkor Button típusra konvertáljuk, hogy a gomb tulajdonságait módosíthassuk. 
is operátor: ellenőrízzük, hogy a sender egy adott típusú objektum-e.

```C#
private void Button_Click(object sender, RoutedEventArgs e)
{
    if (sender is Button button && button.Content == null)
    {
        
    }
}
```

8. Ha sikerül Button típusként azonosítani a sender-t, akkor kiolvassuk az adott button helyzetét és ezt felvesszük sor és oszlopként int változókba.

```C#
private void Button_Click(object sender, RoutedEventArgs e)
{
    if (sender is Button button && button.Content == null)
    {
        int row = Grid.GetRow(button);
        int col = Grid.GetColumn(button);
    }
}
```

9. Majd megnézzük a player1 változónkant amit kivűl létre hoztunk, hogy igaz e? Ha igaz, akkor az adott button-nak a Contentjét, tehát a szövegét beállítjuk X-re, a player1 érték false lesz (ezért legközelebb O-t rak le) és átadja a button kordinátáját az amőba mátrixnak, és a helyére egy 1-est írunk be, ez fogja az X-eket jelölni a mátrixban. Viszont legközelebb ha rámegyünk a gombra, akkor a player1 változónk már hamis, ezért a button szövege O lesz, és vissza állítjuk igazra a player1-et így mindig egyszer X-et egyszer, O-t rakunk le. És persze ennek is átadjuk a kordinátáját, és az O gombokat 2-vel jelöljük. És itt létrekell hozzunk egy WinnerCheck() függvényt, ahol minden kattintáskor ellenőrizzük hogy valaki nem e nyert e

```C#
private void Button_Click(object sender, RoutedEventArgs e)
{
    if (sender is Button button && button.Content == null)
    {
        int row = Grid.GetRow(button);
        int col = Grid.GetColumn(button);
        if (player1)
        {
            button.Content = "x";
            player1 = false;
            amoba[row, col] = 1;
        }
        else
        {
            button.Content= "o";
            player1 = true;
            amoba[row,col] = 2;
        }
        WinnerCheck();
    }
}
```

10. A WinnerCheck() függvényben ahogy említettem minden gombnyomásnál megnézzük hogy nyert e vagy az X vagy az O. Először felveszünk egy üres string változót winner névvel, ide fogjuk elmenteni a nyertest (x vagy o). 

```C#
private void WinnerCheck()
{
    string winner = string.Empty;
}
```

11. 3 nagy esetben nyerhet valamelyik fél. Vagy oszloposan 3 féle képen, vagy vízszintesen 3 féle képen, vagy átlósan 2 féle képen. A C# úgy kezeli a két dimenziós tömböket, hogyha végig megyünk rajtuk egy for-al, akkor a "amoba.GetLength(0)" a "0" mindig a sorok számát veszi át (a mi esetünkben ez 3 most) és az "amoba.GetLength(1)" az "1" mindig az oszlopok számát veszi át (ez is 3 a mi esetünkben, de ha a mátrixnak különböző az értéke, akkor ez változik) 
    1. *Oszloposan megyünk végig rajta:*
    For ciklussal végig megyünk a mátrixon, 0-ról kezdünk és addig megyünk, ahány sorból áll a mátrix, ezt tudjuk a amoba.GetLength(0)-val elérni. A for cikloson belül, megnézzük hogy ha egy adott oszlop, összes értéke 1, akkor X nyer, ha nem 1 akkor O nyer. Mivel oszlopokat nézünk, ezért a mátrix első értéke mindig ugyan azok lesznek (0, 1, 2), mert az jelöli a sorokat, és csak a második értéke lesz az *i*-edik elem, így tudjuk megnézni az összes oszlopot (Az első oszlop adatai a mi esetünkben **0,0; 1,0 és 2,0**). És ezeket meg nézzük hogy az értékük egyenlőek-e. És ha van egy nyertes, akkor egy break a for végén, hogy ne ellenőrizze tovább.
    ```C#
    for (int i = 0; i < amoba.GetLength(0); i++)
    {
        if (amoba[0,i]!= 0 && amoba[0,i] == amoba[1,i] && amoba[1,i] == amoba[2,i])
        {
            winner = amoba[0, i] == 1 ? "x" : "o";
            break;
        }
    }
    ```
    2. *Vízszintesen megyünk végig rajta:*
    Ez ugyan úgy működik mint amikor az oszlopokat ellenőriztük, csak a amoba.GetLength(1) itt 1 lesz az érték mivel itt most egy sor a mi esetünkben 3 oszlop tartalma. És az amőba mátrix első értéke lesz így az *i*-edik érték, mert az fog változni mint oszlopok, és a második érték az vagy 0 vagy 1 vagy 2. És ezeket meg nézzük hogy az értékük egyenlőek-e. És ha van egy nyertes, akkor egy break a for végén, hogy ne ellenőrizze tovább.
    ```C#
    for (int i = 0;i < amoba.GetLength(1); i++)
    {
        if (amoba[i, 0] != 0 && amoba[i, 0] == amoba[i, 1] && amoba[i, 1] == amoba[i, 2])
        {
            winner = amoba[i, 0] == 1 ? "x" : "o";
            break;
        }
    }
    ```
    3. *Átlósan ellenőrizzük le:*
    Itt két féle képen lehet alaki nyertes, ilyen X alakból az egyik átló. A középső, mátrixban 1,1-elem azon mindenféle képpen át fog menni, és megnézzük hogy megvan e az egyik átló \ vagy a másik átló /. És itt mivel az 1,1 az mind két esetben benne van, azt leellenőrizzük, hogyha 1 az értéke akkor X, ha nem 1 akkor O nyert.
    ```C#
    if ((amoba[0,0] != 0 && amoba[0,0] == amoba[1, 1] && amoba[1, 1] == amoba[2, 2]) ||
            (amoba[0, 2] != 0 && amoba[0, 2] == amoba[1, 1] && amoba[1, 1] == amoba[2, 0]))
    {
        winner = amoba[1, 1] == 1 ? "x" : "o";
    }
    ```

12. A WinnerCheck() végén, meg kell nézni hogy a winner, ha már nem üres, akkor kiírja a nyertest egy felugró üzenetbe, és lefuttatjuk a Restart() függvényt, hogy újra induljon a játék.
```C#
private void WinnerCheck()
{
    string winner = string.Empty;
    //columncheck
    for (int i = 0; i < amoba.GetLength(0); i++)
    {
        if (amoba[0,i]!= 0 && amoba[0,i] == amoba[1,i] && amoba[1,i] == amoba[2,i])
        {
            winner = amoba[0, i] == 1 ? "x" : "o";
            break;
        }
    }
    //rowcheck
    for (int i = 0;i < amoba.GetLength(1); i++)
    {
        if (amoba[i, 0] != 0 && amoba[i, 0] == amoba[i, 1] && amoba[i, 1] == amoba[i, 2])
        {
            winner = amoba[i, 0] == 1 ? "x" : "o";
            break;
        }
        }
        //crosscheck
        if ((amoba[0,0] != 0 && amoba[0,0] == amoba[1, 1] && amoba[1, 1] == amoba[2, 2]) ||
            (amoba[0, 2] != 0 && amoba[0, 2] == amoba[1, 1] && amoba[1, 1] == amoba[2, 0]))
        {
            winner = amoba[1, 1] == 1 ? "x" : "o";
        }
        if (winner != "")
        {
            MessageBox.Show(winner);
            Restart();
        }
}
```

13. Restart() függvényben az összes button szövegét null-ra állítjuk, így a kijelzőn törlödik az összes X és O. Majd egy dupla for ciklussal végig megyünk a mátrixon, és minden elemét vissza álltijuk 0-ra. És ekkor ha a felugró üzenetet le OK-oljál, kezdődhet újra a játék.

```C#
private void Restart()
{
    Button00.Content = null;
    Button01.Content = null;
    Button02.Content = null;
    Button10.Content = null;
    Button11.Content = null;
    Button12.Content = null;
    Button00.Content = null;
    Button21.Content = null;
    Button22.Content = null;
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            amoba[i, j] = 0;
        }
    }
}
```
<details>
<summary>Nyiss le az xaml forrásért!</summary> 

```C#
<Window x:Class="WpfApp1.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:WpfApp1"
        mc:Ignorable="d"
        Title="MainWindow" Height="750" Width="750">
    <Grid Background="Gainsboro">
        <Grid.ColumnDefinitions>
            <ColumnDefinition />
            <ColumnDefinition />
        </Grid.ColumnDefinitions>
        <Grid.RowDefinitions>
            <RowDefinition />
            <RowDefinition />
        </Grid.RowDefinitions>

        <TextBlock x:Name="PuzzleText" Grid.Column="0" Grid.Row="0" HorizontalAlignment="Center" VerticalAlignment="Center" FontSize="24"/>

        <Grid x:Name="LetterButtonsGrid" Grid.Column="0" Grid.Row="1" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Grid.ColumnDefinitions>
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
                <ColumnDefinition />
            </Grid.ColumnDefinitions>
            <Grid.RowDefinitions>
                <RowDefinition />
                <RowDefinition />
                <RowDefinition />
                <RowDefinition />
                <RowDefinition />
            </Grid.RowDefinitions>

            <Button Content="A" Grid.Row="0" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Á" Grid.Row="0" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="B" Grid.Row="0" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="C" Grid.Row="0" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="D" Grid.Row="0" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="E" Grid.Row="0" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="É" Grid.Row="0" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="F" Grid.Row="1" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="G" Grid.Row="1" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="H" Grid.Row="1" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="I" Grid.Row="1" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Í" Grid.Row="1" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="J" Grid.Row="1" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="K" Grid.Row="1" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="L" Grid.Row="2" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="M" Grid.Row="2" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="N" Grid.Row="2" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="O" Grid.Row="2" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ó" Grid.Row="2" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ö" Grid.Row="2" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ő" Grid.Row="2" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="P" Grid.Row="3" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Q" Grid.Row="3" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="R" Grid.Row="3" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="S" Grid.Row="3" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="T" Grid.Row="3" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="U" Grid.Row="3" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ú" Grid.Row="3" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />

            <Button Content="Ü" Grid.Row="4" Grid.Column="0" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Ű" Grid.Row="4" Grid.Column="1" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="V" Grid.Row="4" Grid.Column="2" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="W" Grid.Row="4" Grid.Column="3" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="X" Grid.Row="4" Grid.Column="4" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Y" Grid.Row="4" Grid.Column="5" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
            <Button Content="Z" Grid.Row="4" Grid.Column="6" Margin="1" Width="40" Height="40" Click="LetterButton_Click" />
        </Grid>

        <TextBlock Grid.Column="1" Grid.Row="1" HorizontalAlignment="Center" VerticalAlignment="Center" FontSize="18" Text="Akasztófa Játék"/>
        <TextBlock x:Name="InfoText" Grid.Column="1" Grid.Row="0" HorizontalAlignment="Center" VerticalAlignment="Center" FontSize="18"/>
        <WrapPanel x:Name="LetterButtonsPanel" HorizontalAlignment="Center" VerticalAlignment="Center" Margin="10"/>

    </Grid>
</Window>


```
</details>

<details>
<summary>Nyiss le az xaml.cs forrásért!</summary>

```C#
using System.Text;
using System.Windows;
using System.IO;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace WpfApp1
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        private string selectedWord;
        private List<char> guessedLetters = new List<char>();
        private int mistakeCount = 0;
        private const int MaxMistakes = 11;

        public MainWindow()
        {
            InitializeComponent();
            NewGame();
        }

        private void NewGame()
        {
            LoadWords();
            guessedLetters.Clear();
            mistakeCount = 0;
            UpdatePuzzle();
            UpdateInfo();

            foreach (object element in LetterButtonsGrid.Children)
            {
                if (element is Button button)
                {
                    button.IsEnabled = true;
                }
            }
        }

        private void LoadWords()
        {
            try
            {
                List<string> words = new List<string>();
                using (StreamReader sr = new StreamReader("words.txt"))
                {
                    string line;
                    while ((line = sr.ReadLine()) != null)
                    {
                        if (line.Length <= 20 && !line.Contains(" ") && !line.Contains("-"))
                        {
                            words.Add(line.ToUpper());
                        }
                    }
                }

                if (words.Count == 0)
                {
                    MessageBox.Show("No valid words found in the file!");
                    return;
                }

                Random random = new Random();
                selectedWord = words[random.Next(words.Count)];
            }
            catch (Exception ex)
            {
                MessageBox.Show($"An error occurred while loading the words: {ex.Message}");
            }
        }

        private void UpdatePuzzle()
        {
            string puzzle = "";
            foreach (char letter in selectedWord)
            {
                puzzle += (guessedLetters.Contains(letter) ? letter.ToString() : "_") + " ";
            }
            PuzzleText.Text = puzzle;
        }

        private void UpdateInfo()
        {
            InfoText.Text = $"Mistakes: {mistakeCount} / {MaxMistakes}";
        }

        private void LetterButton_Click(object sender, RoutedEventArgs e)
        {
            if (sender is Button button)
            {
                char letter = button.Content.ToString()[0];
                button.IsEnabled = false;

                if (selectedWord.Contains(letter))
                {
                    guessedLetters.Add(letter);
                    UpdatePuzzle();

                    if (PuzzleText.Text.Replace(" ", "") == selectedWord)
                    {
                        MessageBox.Show("Congratulations, you won! A new game will start.");
                        NewGame();
                    }
                }
                else
                {
                    mistakeCount++;
                    UpdateInfo();

                    if (mistakeCount >= MaxMistakes)
                    {
                        MessageBox.Show($"You lost! The word was: {selectedWord}. A new game will start.");
                        NewGame();
                    }
                }
            }
        }
    }
}

```
</details>
