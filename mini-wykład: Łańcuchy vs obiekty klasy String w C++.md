## Klasa String : teoria

### Wstęp

W wielu aplikacjach, również konsolowych potrzebne jest przetwarzanie ciągów znaków.
Język C ułatwia to za pomocą rodziny funkcji do obsługi ciągów znaków znajdujących się w pliku nagłówkowym
string.h. W języku C++ jest to cstring. Te pliki nagłówkowe działają dla ciągów znaków języka C z biblioteki
tego języka a nie z klasy. Różne implementacje języka C++ udostępniają w tym celu proste klasy.
Klasa string zawiera bogaty zestaw metod, konstruktorów, przeciążonych operatorów do przypisywania ciągu
znaków, porówywania, czy uzyskiwania dostępu do poszczególnych znaków ciągu.
Nie chciałem w klasie pierwszej wprowadzać tego tematu w kontekście obiektowym, bo paradygmat ten poznacie dopiero
w klasie drugiej. Nie chcę teraz wprowadzać nawet pojęcia kostruktora jest ich aż sześć.
Postaram się potraktować obiekty klasy string jako "typ złożony" i o obiektowości nie wspomnę wcale.

Jak utworzyć napis? Podaję 2 sposoby:

> [!NOTE]
> string one ("Jestem debeściakiem");
>
> 





Napisz rekurencyjną funkcję, która obliczy silnię podanej liczby naturalnej $n$.<br>
Silnia to iloczyn wszystkich liczb naturalnych od $1$ do $n$. Oznaczana jest jako $n!$.

**Przykład:** $5! = 5 * 4 * 3 * 2 * 1 = 120$
