```c#
/*
Feladat 1 - Bekért szöveg vizsgálata.
Irassa ki hogy: Kérem adja meg a szöveget
Vizsgálja a szöveget hogy van-e benne 'Hello' szövegrész
Ha tartalmazza akkor irassa ki a szöveget, ellenkező esetben írja ki hogy a szöveg nem tartalmazza a 'Hello' részt
*/

Console.WriteLine("Kérem adja meg a szöveget");
string a = Console.ReadLine();

if (a.Contains("Hello"))
{
  Console.WriteLine($"A szöveg tartalmazza azt hogy: 'Hello'");
}
else
{
  Console.WriteLine($"A szöveg nem tartalmazza azt hogy: 'Hello'");
}

/*
Feladat 2 - Páros vagy páratlan
Irassa ki hogy: Kérem adjon meg egy egész számot
Írja ki hogy a szám páros vagy páratlan
*/

Console.Write("Kérem adjon meg egy egész számot");
int a = int.Parse(Console.ReadLine());

if (a % 2 == 0) 
{
  Console.WriteLine($"{a} az páros szám");
}
else
{
  Console.WriteLine($"{a} az páratlan szám");
}

/*
Feladat 3 - Szerkeszthető háromszög
Irassa ki hogy: Kérem adjon meg egymás után a háromszög oldalainak hosszát
Vizsgálja meg, hogy a háromszög szerkeszthető-e. (Háromszög két oldalának az összege mindig nagyobb mitn a harmadik)
*/

Console.WriteLine("Kérem adjon meg egymás után a háromszög oldalainak hosszát");
int a = int.Parse(Console.ReadLine()); 
int b = int.Parse(Console.ReadLine()); 
int c = int.Parse(Console.ReadLine()); 

if(a + b > c && b + c > a && a + c > b) 
{
  Console.WriteLine("Háromszög szerkeszthető");
}
else
{
  Console.WriteLine("Nem szerkeszthető háromszög");
}

/*
Feladat 4 - Faktoriális
Irassa ki hogy: Kérem adjon meg egy egész számot
A megadott számnak számolja ki a faktoriális értékét majd írja ki
*/

Console.WriteLine("Kérem adjon meg egy egész számot");
int a = int.Parse(Console.ReadLine()); 
int j = 1;

for(int i = 1; i <= a; i++)
{
  j = j * i;
}
Console.WriteLine(j);

/*
Feladat 5 - Szám osztói
Irassa ki hogy: Kérem adjon meg egy egész számot
A megadott számnak Írja ki az összes osztóját
Döntse el, hogy a szám prím (vagyis csak két osztója van) és írja ki hogy igen vagy nem
*/

Console.WriteLine("Kérem adjon meg egy egész számot");
int a = int.Parse(Console.ReadLine()); 
int p = 0;

for(int i = 1; i<=a; i++) 
{
  if( a % i == 0 ) 
  {
     Console.WriteLine($"{i} osztoja a(z) {a} szamnak");
     p++;
  }
}

if (p == 2) Console.WriteLine($"{a} prim");

/*
Feladat 6 - Szám osztói
Irassa ki hogy: Kérem adjon meg három egész számot
Döntse el, hogy melyik a legnagyobb és azt írja ki
*/

Console.WriteLine("Kérem adjon meg három egész számot");
int a = int.Parse(Console.ReadLine()); 
int b = int.Parse(Console.ReadLine()); 
int c = int.Parse(Console.ReadLine()); 

int x = 0;

if(a > b) 
{
  x = a;
}
else 
{
  x = b;
}

if( x > c)
{
  Console.WriteLine(x);
}
else
{
  Console.WriteLine(c);
}
```
