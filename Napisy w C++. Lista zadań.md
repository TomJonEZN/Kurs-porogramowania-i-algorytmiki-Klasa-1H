## Napisy: zadania Lista 1 

#### Uwaga: Należy pisać funkcje zgodnie ze specyfikacją zadania a następnie przetestować ich działanie.
#### Czas oddania to najbliższy czwartek, 7 marca, zadań nie należy wysyłać, tylko przynieść je ze sobą.

### Zadanie 1 (łatwe)
Napisz funkcję char at1(string napis, int a), która zwraca znak (char) z napisu pod indeksem a.<br>
**Przykład:** at1("ABBA", 1) powinna zwrócić 'B'.

### Zadanie 2 (łatwe)
Napisz funkcję string substr1(string napis, int a, int b), która zwraca podłańcuch (string) z napisu od indeksu a do indeksu b.<br>
**Przykład:** substr1("ABBA", 2, 3) powinna zwrócić "BA".

### Zadanie 3 (łatwe)
Napisz funkcję string append1(string napis1, string napis2), która zwraca konkatenację (sklejenie) dwóch napisów.<br>
**Przykład:** append1("AB", "BA") powinna zwrócić "ABBA".

### Zadanie 4 (łatwe)
Napisz funkcję int find1(string napis, char znak), która zwraca indeks pierwszego wystąpienia znaku w napisie.<br>
**Przykład:** afind1("Ala ma kota", 'a') powinna zwrócić 5.

### Zadanie 5 (łatwe)
Napisz funkcję int string replace1(string napis, char z1, char z2), która zamienia wszystkie wystąpienia z1 w napisie za pomocą z2
i zwraca tak zbudowany napis. Pamiętaj, że w zadaniach budujących napisy nie możesz ich mutować (zamieniać liter)! W zamian buduj je od nowa.<br>
**Przykład:** replace1("Ala ma kota", 'a', 'e') powinna zwrócić "Ale me kote".

### Zadanie 6 (łatwe, obowiązkowe, z lekcji)
Napisz funkcję string longest(string napis, char znak), która znajduje nadłuższy podłańcuch w napisie gdzie separatorem dla słów jest podany znak.<br> 
**Przykład:** longest("Ala ma kota a kot ma Alę", ' ') powinna zwrócić "kota".

### Zadanie 7 (łatwe)
Napisz funkcję string rev1(string napis), która odwraca napis (uwaga, należy goi odwrócić w miejscu a nie tylko wypisać w odwrotnej kolejności.<br>
**Przykład:** rev1("ezeteniak") powinna zwrócić "kaineteze".

### Zadanie 8 (łatwe)
Napisz funkcję bool ispalindrome("napis"), która sprawdza, czy napis jest palindromem i zwraca true/false w odpowiednich przypadkach. Palindromem jest napis, który jest tożsamy w czytaniu w obu kierunkach, np. "kajak", "jakłysyłkaj" lub "kobyłamamałybok"<br> 
**Przykład:** ispalindrome("ABBA") powinna zwrócić true (1).

### Zadanie 9 (nieco trudniejsze)
Najdłuższy wspólny podciąg (ang. longest common subsequence) to najdłuższy podciąg znaków, które występują w tej samej kolejności w dwóch porównywanych łańcuchach znaków. Elementy podciągów nie muszą przy tym leżeć obok siebie (tym różni się ten problem od problemu najdłuższego wspólnego podłańcucha (ang. longest common substring). Napisz funkcję string lcs(string napis1, string napis2), która zwraca najdłuższy wspólny podłańcuch (string) czyli najdłuższy ciąg znaków, który występuje w obu napisach i znaki są w nim w tej samej kolejności<br>
**Przykład:** lcs("Ala ma kota", "A kot ma Alę") powinna zwrócić " kot".

### Zadanie 10 (średniej trudności, obowiązkowe, z lekcji)
[pesele](https://www.szybkiplik.pl/5nqq5RPLx9)
