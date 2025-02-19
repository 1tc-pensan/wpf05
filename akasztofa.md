# Grid: Akasztofa
## Feladat
Solution neve: **WpfApp1**

Projekt leírása:Csinálni kell 2 gridet egyik az a fő grid a másik meg a betűk kiírásához kell.A fő gridet felosztjuk 2x2-re.Az 1 első gridet felhasználjuk a adott szó hosszának megjelenítésére.A 2 gridet a hibák számának megjelenítésére van felhasználva.A 3 griden belűl van még egy grid ami a 
betűkre van felhasználva.A 4 grid meg a jaték nevét tartalmazza.

Működés:Van egy random generált szó ami ki kell találni.



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

1. Ablak és elrendezés (Window, Grid):

    Az alkalmazás egy Window (ablak) elemben található, amely 750x750 pixel méretű.
    Az ablak tartalmaz egy Grid elrendezést, amely 2 oszlopot és 2 sort definiál. Az első sor és oszlop tartalmazza a játékfeladatot, míg a második sor és oszlop a betűgombokat és a játék információit.
2. TextBlock - Feladvány (FeladvanyText):
    A feladvány, vagyis a titkos szó, a FeladvanyText TextBlock-ban jelenik meg. A játékosnak itt kell megpróbálnia kitalálni a szót a betűk beírásával.
    
3. Betűgombok (BetuGombokGrid):
    A második sorban található egy 7x5-ös elrendezésű gombmátrix. Minden gomb egy-egy betűt képvisel (pl. "A", "B", "C", stb.). Ezek a gombok a játékos tippjeit fogják reprezentálni. Minden gombhoz tartozik egy Click eseménykezelő, ami a betűk megnyomásakor aktiválódik.
4. InfoText:
    A InfoText TextBlock a játék állapotát mutatja: hány hibát követett el a játékos és hány hibát enged meg a játék.

5. WrapPanel - BetuGombokPanel:
    Bár a kód tartalmaz egy BetuGombokPanel elemet, jelenleg nem használjuk az elrendezést, mert a betűgombokat közvetlenül a BetuGombokGrid-ben definiáljuk.

6. A játékosok adatainak tárolása:

    A kivalasztottSzo tárolja a véletlenszerűen kiválasztott szót, amelyet a játékosnak ki kell találnia.
    A tippeltBetuk egy lista, amely a játékos által kitalált betűket tartalmazza.
    A hibakSzama változó számolja a hibás találatokat (az eltévesztett betűket), míg a MaxHibak konstans meghatározza a maximálisan megengedett hibák számát (11).

7. Játék indítása (UjJatek):

    Az UjJatek metódus inicializálja a játékot: betölti a szavakat, törli az előző játék állapotát (tippek, hibák), és frissíti a feladványt.
    Az összes betűgombot engedélyezi újra, hogy a játékos újra tippelhessen.
```C#
private void UjJatek()
        {
            BetoltSzavak();
            tippeltBetuk.Clear();
            hibakSzama = 0;
            FrissitFeladvany();
            FrissitInfo();

            foreach (object elem in BetuGombokGrid.Children)
            {
                if (elem is Button gomb)
                {
                    gomb.IsEnabled = true;
                }
            }
        }
```
8. A Szavak beolvasása a words.txt
    A szavak egy words.txt fájlból töltődnek be, ahol minden érvényes szó (max. 20 karakter hosszú, szóközök és kötőjelek nélkül) hozzáadódik a listához.

    A program véletlenszerűen kiválaszt egy szót a listából, amelyet a játékosnak ki kell találnia.

```C#
        private void BetoltSzavak()
        {
            try
            {
                List<string> szavak = new List<string>();
                using (StreamReader sr = new StreamReader("words.txt"))
                {
                    string sor;
                    while ((sor = sr.ReadLine()) != null)
                    {
                        if (sor.Length <= 20 && !sor.Contains(" ") && !sor.Contains("-"))
                        {
                            szavak.Add(sor.ToUpper());
                        }
                    }
                }

                if (szavak.Count == 0)
                {
                    MessageBox.Show("Nincsenek érvényes szavak a fájlban!");
                    return;
                }

                Random random = new Random();
                kivalasztottSzo = szavak[random.Next(szavak.Count)];
            }
            catch (Exception ex)
            {
                MessageBox.Show($"Hiba történt a szavak betöltése közben: {ex.Message}");
            }
        }
```

9. Feladvány frissítése (FrissitFeladvany):

```C#
private void FrissitFeladvany()
        {
            string feladvany = "";
            foreach (char betu in kivalasztottSzo)
            {
                feladvany += (tippeltBetuk.Contains(betu) ? betu.ToString() : "_") + " ";
            }
            FeladvanyText.Text = feladvany;
        }

```

10. A FrissitFeladvany metódus frissíti a feladványt, vagyis megjeleníti a helyes betűket és aláhúzásokat (például _), hogy a játékos lássa, hol tart a kitalálásban.
Információ frissítése (FrissitInfo):

```C#
private void FrissitInfo()
        {
            InfoText.Text = $"Hibák száma: {hibakSzama} / {MaxHibak}";
        }

```

11. A FrissitInfo metódus frissíti az információs szöveget, amely megjeleníti a hibák számát.
Betűgomb kattintásának kezelése (BetuGomb_Click):
```C#
private void BetuGomb_Click(object sender, RoutedEventArgs e)
        {
            if (sender is Button gomb)
            {
                char betu = gomb.Content.ToString()[0];
                gomb.IsEnabled = false;

                if (kivalasztottSzo.Contains(betu))
                {
                    tippeltBetuk.Add(betu);
                    FrissitFeladvany();

                    if (FeladvanyText.Text.Replace(" ", "") == kivalasztottSzo)
                    {
                        MessageBox.Show("Gratulálok, nyertél! Új játék indul.");
                        UjJatek();
                    }
                }
                else
                {
                    hibakSzama++;
                    FrissitInfo();

                    if (hibakSzama >= MaxHibak)
                    {
                        MessageBox.Show($"Vesztettél! A szó: {kivalasztottSzo}. Új játék indul.");
                        UjJatek();
                    }
                }
            }
        }
```
Amikor a játékos rákattint egy betűgombra, a BetuGomb_Click metódus aktiválódik:
A gomb tartalmából kinyeri a betűt.
Letiltja a gombot, hogy a játékos ne tudja újra megnyomni.
Ha a kitalált betű szerepel a titkos szóban, hozzáadja azt a tippeltBetuk listához, és frissíti a feladványt.
Ha a feladvány teljesen kitalálásra került (a FeladvanyText és a kivalasztottSzo megegyeznek), gratulál a játékosnak, és új játékot indít.
Ha a betű nincs a szóban, növeli a hibák számát, és frissíti az információkat.
Ha a hibák száma eléri a maximális értéket (11), akkor a játékos elveszíti a játékot, és az alkalmazás új játékot indít.
<details>

</details> 
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
