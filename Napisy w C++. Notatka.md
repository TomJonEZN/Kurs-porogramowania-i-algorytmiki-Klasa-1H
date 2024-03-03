## Napisy. Łańcuchy znaków i obiekty klasy String : krótka notatka

### Wstęp

W wielu aplikacjach, również konsolowych, potrzebne jest przetwarzanie ciągów znaków.
Język C ułatwia to za pomocą rodziny funkcji do obsługi ciągów znaków znajdujących się w pliku nagłówkowym
string.h. W języku C++ jest to cstring. Te pliki nagłówkowe działają dla ciągów znaków języka C z biblioteki
tego języka a nie z klasy. Różne implementacje języka C++ udostępniają w tym celu proste klasy.
Klasa string zawiera bogaty zestaw metod, konstruktorów, przeciążonych operatorów do przypisywania ciągu
znaków, porówywania, czy uzyskiwania dostępu do poszczególnych znaków ciągu.
Nie chciałem w klasie pierwszej wprowadzać tego tematu w kontekście obiektowym, bo paradygmat ten poznacie dopiero
w klasie drugiej. Nie chcę teraz wprowadzać nawet pojęcia kostruktora a jest ich aż sześć.
Postaram się potraktować obiekty klasy string jako "typ złożony" i o obiektowości nie wspomnę wcale.
Kiedy zatem użyję słowa "napis", bardzo często będę je utozsamiał świadomie z czymś nietożsamym, tj. z 
obiektem klasy string. Nie jest to dydaktycznie poprawne, ale sami wywołaliście ten temat.
Postaram się ograniczyć do niezbędnego minimum informacji aby łatwo było wyłuskać najistotniejsze elementy.

> [!NOTE]
> ***1. Jak utworzyć napis? Podaję 2 sposoby:***

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
  //1
  string imie = "Marceli";
  //2
  string nazwisko("Debeściak");
  cout << imie << " " << nazwisko << endl;
  return 0;
}
``` 

> [!TIP]
> ***2. Jak wprowadzać dane do napisu? W przypadku języka C++ można to zrobić na np. tak (są inne sposoby):***

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
  char imie[100] // ok w  C++03; niedozwolony zapis w C++11 i wyżej z wyjątkiem c++17;
  string nazwisko;  
  //1
  cin.getline(imie, 100);        //wczytuje słowo, pomija \n
  //2
  cin >>nazwisko;                //wczytuje słowo  
  cout << imie << " " << nazwisko << endl;  
  return 0;
}
```

> [!IMPORTANT]
> ***3. Jak porównywać napisy? W języku C++ można je porównywać za pomocą przeciążonych operatorów <, ==, != etc.
> oczywiście są one porównywane pod względem porządku leksykograficznego (jak w słowniku):***

```cpp
#include <iostream>
#include <string>

using namespace std;

int main() {
  
  string napis1("kopytko");
  char napis2[20] = "anakonda";
  string napis3("jestem gitem");
  
  // możesz używać znanych Ci operatorów porównywannia
  if(napis2 < napis1)
     cout << napis3 << endl;
     
  return 0;
}
```

> [!CAUTION]
> ***4. Jak sprawdzić długość napisu? Są dwie funkcje, które działają tak samo. Jest to pochodząca z klasy string składowa length()***
> ***Metoda size() została dodana później w celu zapewnienia zgodności z biblioteką STL***

```cpp
#include <iostream>
#include <string>

using namespace std;

int main() {
  
  string napis1("bingo");
  string napis2 = "matma";
  
  if(napis1.size() == napis2.length())
     cout << "oba ciągi mają taką samą długość" << endl;
     
  return 0;
}
```

> [!WARNING]
> ***5. Porządek znaków wyznaczany jest przez kod ASCII w którym cyfry uznawane są za mniejsze od dużych liter  a duże litery są***
> ***mniejsze od małych liter, spójrz na porządek znaków w tablicy kodów ASCII (czasem będzie trzeba odjąć lub dodać 48 od/do cyfr***
> ***wyrażonych znakiem, aby otrzymać ich wartość dziesiętną. Zapamiętaj, że napisy otaczamy znakiem cudzysłowu a znaki znakiem***
> ***apostrofu!!! Spójrz (przykładowo znak '0' ma wartość 48 a '9' wartość 57:***

![](https://cdn.shopify.com/s/files/1/1014/5789/files/Standard-ASCII-Table_large.jpg?10669400161723642407)

****Dla przykładu iterowania oraz budowania funkcji wokół napisu taki oto kod. Zwróć uwagę, w jaki sposób napis jest przekazany do funkcji,
w jaki sposób przechodzimy po napisie i jak traktujemy znaki napisu, zwłaszcza te, które reprezentują cyfry:****

```cpp
#include <iostream>
#include <string> 
using namespace std; 
  
void foo(string napis, int d) 
{  
    string numer("10");
    for (int i = 0; i < d; i++) { 
        cout<< napis[i]<< " "; 
    }    
    cout << "\nJestem w technikum nr ";
        for (int i = 0; i < numer.size(); i++)  
            cout << numer[i] - 48; 
} 
  
int main() 
{ 
    string napis = "Kocham EZN"; 
    int dlugosc = napis.length(); 
    foo(napis, dlugosc); 
}
```
> [!CAUTION]
> ***Uwaga, nie mutuj napisów, nawet jeśli masz wrażenie, że to działa poprawnie. Przy omawianiu wskaźników powiem, jak to robić dobrze.***
> ***Poniższy kod obrazuje, w jaki sposób powinieneś tworzyć nowe napisy. Na liście pojawią się zadania, wktórych powinieneś napisać***
> ***przydatne w tym celu funkcje. W kodzie padło dziwne słowo "literał". Jest to po prostu dana zapisana w kodzie, w bieżącym kontekście sa to napisy***

```cpp
#include <iostream>
#include <string> 
using namespace std; 
  
int main() 
{
    string napis1 = "literał1";
    string napis2("literał2"); 
    
    napis1[0] = 'x';        // nie rób tego na listach!!!
    napis2[0] = 'y';          
    
    // zamiast mutowania buduj napisy od zera np. tak
    
    string napis3 = "";
    napis3 += 'z';
    for(int i = 1; i < napis2.length() - 1; i++)
       napis3 += napis2[i];
    napis3 += '3';
    
    cout << napis1 << " " << napis2 << " " << napis3 << endl;
}
```



> [!CAUTION]
>***Uwaga: W pliku "Napisy. Lista zadań.md" znajdziesz listę zadań w omawianym temacie. Dwa z nich są obowiązkowe.
> Nie wolno Ci używać przy rozwiązywaniu wbudowanych metod np find() czy at() czy substr() lub innych!!!
> Jedynie długość napisu możesz obsługiwać opowiedzianymi funkcjami length() lub size().
> Jeśli będą Ci potrzebne jakieś dodatkowe metody, musisz je napisać sam/sama!!!***

[Napisy w C++ Lista zadań](Napisy w C++. Lista zadań/).
 


Napisz rekurencyjną funkcję, która obliczy silnię podanej liczby naturalnej $n$.<br>
Silnia to iloczyn wszystkich liczb naturalnych od $1$ do $n$. Oznaczana jest jako $n!$.

**Przykład:** $5! = 5 * 4 * 3 * 2 * 1 = 120$
