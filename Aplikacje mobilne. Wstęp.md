## Kurs programowania aplikacji na urządzenia mobilne. Pojęcia podstawowe

W tym miejscu będą powstawać treści obowiązujące również na lekcjach klas programowo wyższych. Robię te notatki nie dla siebie, ale dla Was i będę ich wymagał na regularnych kartkówkach. Początkowo myślałem, że praktyczne podejście do tematu programowania wystarczy ale, ze względu na aspekty dydaktycznej i metodologicznej  poprawności nauczania, samo przeklikiwanie i przeciąganie komponentów, lub też ich generowanie przez jakiś język znaczników jest niepoprawne. A ja chciałbym chociaż jedną programową rzecz zrobić od początku do końca dobrze. I, jak np. do desktopów podchodziłem bardzo praktycznie rzucając treści opakowane przykładem obsługi wybranej grupy komponentów, tutaj będą padać pojęcia, które są pod spodem, często bardzo abstarkcyjne. Oczywiście nie ustrzegę się błędów (nie mam tutaj słownika i nie mam czasu edytować tego gdzie indziej, więc proszę o wyrozumiałość i wskazywanie rażących literówek i ortów), ale poświęcam swój prywatny czas by powstały przetrawione, spójne materiały do samodzielnej nauki a o nie bardzo ciężko w sieci.
Przede wszyskim, mój kurs aplikacji mobilnych będzie dotyczył programowania w Javie (w alternatywnym podejściu można użyć Kotlina) w środowisku Android Studio w wersji HengeHog. Będę zwracał uwagę na ograniczenie zasobów urządzeń mobilnych, wydajność procesora, czy zużycie pamięci. Od strony praktycznej na początku skupię się na budowaniu interfejsów komunikacji z użytkownikiem a potem na logikach działania róznych aplikacji z uwzględnieniem komunikacji z różnymi elementami, w jakie wyposażone są smartfony (i inne urządzenia mobilne), np. żyroskop, aparat, karta sim czy GPS.

Efektywne projektowanie aplikacji na Androida wymaga znajomości podstawowych pojęć nt. cyklu życia aplikacji mobilnej, stąd poniższy wykaz pojęć:

## 1. Kontext (obiekt typu _Context_) 
Jest to środowisko, w którym uruchamiana jest aplikacja mobilna. Za jego pomocą możemy zarządzać aplikacją i uzyskać dostęp do parametrów aplikacji oraz urządzenia na którym została ta aplikacja uruchomiona.

## 2. Aktywność (obiekt typu _Activity_) 
Wywołanie funkcji aplikacji mobilnej odbywa się przez uruchomienie aktywności. Aktywności budują zatem wszystkie funkcjonalności aplikacji mobilnej i zawierają ich implementację. W jednym zachowaniu się aplikacji mozna wywoływać kolejne aktywności, dzięki czemu można realizować nawet bardzo złożone scenariusze.

### Kontekst

W wielu aplikacjach, również konsolowych, potrzebne jest przetwarzanie ciągów znaków.
Język C ułatwia to za pomocą rodziny funkcji do obsługi ciągów znaków znajdujących się w pliku nagłówkowym
string.h. W języku C++ jest to cstring. Te pliki nagłówkowe działają dla ciągów znaków języka C z biblioteki
tego języka a nie z klasy. Różne implementacje języka C++ udostępniają w tym celu proste klasy.
