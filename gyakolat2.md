```c#
// lista deklarálás különböző módszerekkel
List<string> nevek1 = new List<string> {"Zita", "Bence", "Magda"};
List<string> nevek2 = ["Zita", "Bence", "Magda"];
var nevek = new List<string>
{
  "Zita",
  "Bence",
  "Magda"
};

// elem hozzáfűzése a listához
nevek.Add("Andrea");

// lista rendezése (Andrea új helyre kerül)
Console.WriteLine($"Andrea helye: {nevek.IndexOf("Andrea")}");
nevek.Sort();
Console.WriteLine($"Andrea helye: {nevek.IndexOf("Andrea")}");

// lista bejárása (foreach)
Console.WriteLine("Nevek bejárása (foreach)");
foreach(var nev in nevek)
{
  Console.WriteLine(nev);
}

//lista bejárása (for)
Console.WriteLine("Nevek bejárása (for)");
for(int i = 0; i < nevek.Count; i++)
{
  Console.WriteLine(nevek[i]);
}

// tömb deklarálása
var szamok = new int[] {3,1,6,7,2};
Console.WriteLine("Számok kiírása");
foreach(var szam in szamok)
{
  Console.WriteLine(szam);
}

// tömb rendezése
Array.Sort(szamok);

Console.WriteLine("Számok kiírása rendezés után");
foreach(var szam in szamok)
{
  Console.WriteLine(szam);
}

// elem hozzáfűzése a tömbhöz
szamok = [..szamok, 10];
Console.WriteLine("Számok kiírása összefűzés után");
foreach(var szam in szamok)
{
  Console.WriteLine(szam);
}


// Kő, papír, olló
var jatek = new List<string> {"Kő", "Papír", "Olló"};
Random rnd = new Random();
int index = rnd.Next(0, 3); //0, 1, 2

string jatekos = "Papír";
Console.WriteLine($"Gép azt mondja hogy: {jatek[index]}\nJátékos azt mondja hogy: {jatekos}");

if (jatek[index] == jatekos)
{
    Console.WriteLine("Döntetlen");
}
else 
{
    switch (index)
    {
        case 0:
            if(jatekos == "Papír") {
                Console.WriteLine("Játékos nyert");
            }
            else {Console.WriteLine("Gép nyert");}
            break;
        case 1:
            if(jatekos == "Olló") {
                Console.WriteLine("Játékos nyert");
            }
            else {Console.WriteLine("Gép nyert");}
            break;
        case 2:
            if(jatekos == "Kő") {
                Console.WriteLine("Játékos nyert");
            }
            else {Console.WriteLine("Gép nyert");}
            break;
        default:
            Console.WriteLine("Valami mas");
            break;
    }
}


//Lotto
static void szerencse(int numbers, int huzasok, string tipus)
{
    var szamok = new List<int>();
    Random rnd = new Random();
    while(szamok.Count < huzasok)
    {
        int szam = rnd.Next(1, numbers+1);
        if(szamok.Contains(szam)) { continue; }
        else {
            szamok.Add(szam);
        }
    }
    Console.WriteLine($"A heti nyerőszámok a {tipus} lottónál , nővekvő sorrendben:");
    szamok.Sort();
    foreach (var szam in szamok)
    {
        Console.Write($"{szam} ");
    }
    Console.WriteLine();
}
szerencse(35,7, "Hetes");
szerencse(45,6, "Hatos");
szerencse(90,5, "Ötös");

// Rekurzio
int start = 1;
int max_szint = 10;
static void rekurzio(int i, int depth)
{
    Console.WriteLine($"Rekurzió szintje {i}");
    i++;
    if(i > depth)
    {
        return;
    }
    rekurzio(i, depth);
}
rekurzio(start, max_szint); 

//Szorzas
int a = 6;
int b = 7;

static int multiply(int x, int y){
    return x * y;
}
Console.WriteLine($"{a} és {b} szorzatának eredménye: {multiply(a,b)}");
```
