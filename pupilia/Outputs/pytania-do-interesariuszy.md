# Aport dla Pupilii: pytania do interesariuszy

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — lista w treści z tego dnia; pytania pozostają otwarte.

Lista zbiera otwarte pytania z dokumentów projektu Aport
i z wiki Pupilii. Powtórzenia połączono, a pytania pogrupowano według osób, które
mogą na nie odpowiedzieć. Odpowiedzialność za decyzje przyjęto według wywiadu
z dyrektorką sprzedaży [`raw/inbox/pupilia_wywiad_dyrektorka.md`, 01:02:46]:
sprzedaż odpowiada za zakres i kolejność wdrożenia, logistyka za dostawy i braki,
jakość za blokady, obsługa klienta za zmiany zamówień, finanse za rozliczenia,
a IT za rozwiązanie możliwe do uruchomienia i utrzymania.

Kolumna **Blokuje** wskazuje, na co czeka odpowiedź:

- **etap 1** — pierwsze sklepy: zadania, dostawy, rozbieżności, asystent;
- **pilotaż** — przygotowanie i ocena próby w sklepach;
- **etap 2** — odbiory zamówień i wydzielona pula;
- **później** — obszary bez ustalonego etapu.

Kolumna **Gdzie w dokumentach** służy zespołowi projektu: wskazuje dokumenty
i numery pytań, których dotyczy odpowiedź. Odpowiedź zapisuje się raz, w sekcji
„Odpowiedzi” na końcu tej listy. Zatwierdzone dokumenty aktualizuje się w ich
kolejnej wersji, z odesłaniem do numeru PI.

## Najpilniejsze spośród blokujących etap 1

| Nr | Do kogo | Sprawa |
|---|---|---|
| PI-11 | IT | Który system prowadzi zapas sklepu |
| PI-12 | IT | Z jakich systemów pochodzą zadania |
| PI-13 | IT, sprzedaż | Harmonogram systemów potrzebnych w etapie 1 |
| PI-14 | IT, sprzedaż | Praca bez łączności |
| PI-17 | IT, sprzedaż, właściciele treści | Kryteria odbioru asystenta |
| PI-06 | Sprzedaż, jakość | Kolejność zadań i przydział pracy |

## 1. Dyrektorka sprzedaży: zakres i wdrożenie

| Nr | Pytanie | Blokuje | Gdzie w dokumentach |
|---|---|---|---|
| PI-01 | Które obszary bez ustalonego etapu wchodzą do pierwszego wdrożenia: pulpit kierownika, propozycje uzupełnień, komunikaty i zgłoszenia do centrali, propozycja koszyka, zwroty? | etap 1, etap 2 | PRD 1 |
| PI-02 | **Odłożenia telefoniczne.** Pracownicy chcą, żeby odłożona sztuka była widoczna w Aporcie i w kasie, z zadaniem odniesienia po terminie. Decyzja nie zapadła. Czy odłożenia trafią do systemu, a jeśli tak, do którego (Aport, kasa, usługa dostępności)? Jaki czas oczekiwania obowiązuje: dzisiejszy do 20:00 (wyjątkowo do 12:00 następnego dnia), czy inny? Kto odpowiada, gdy odłożenie uzgodniły dwa sklepy? | później | PRD 2; karta 2; reguły 2; słownik 1–2; model 7 |
| PI-03 | **Sprawdzanie i odkładanie towaru w innym sklepie.** Czy doradca może z Aportu sprawdzić wolną sztukę w innym sklepie i poprosić o jej odłożenie? Jeśli tak, jaką dostępność ma widzieć: stan sklepu, towar wolny do wzięcia czy dostępność internetową? | później | karta 3; słownik 3 |
| PI-04 | **Zamówienie za klienta.** Czy pracownik może złożyć zamówienie internetowe za klienta obecnego w sklepie, z płatnością w kasie lub linkiem? Plan przewiduje, że propozycję koszyka zatwierdza klient. | później | karta 4 |
| PI-05 | **Uprawnienia doradcy w kasie.** Czy doradca dostanie prawo do zdjęcia pozycji z paragonu, zawieszenia rachunku i korekty ceny w limicie? Jaki byłby limit? Czy te zmiany wejdą do audytu kasy (POS) i kto je prowadzi? | później | karta 5; reguły 1; PRD 9 |
| PI-06 | **Kolejność zadań i przydział pracy.** Jak mierzyć „skutek opóźnienia”, który decyduje o kolejności zadań? Kto ustala priorytety poza wycofaniem partii (to ustala jakość)? Czy kierownik przydziela zadania w Aporcie, czy tylko ustnie na podstawie listy? | etap 1 | wymagania 1–2 |
| PI-07 | **Zgłoszona rozbieżność a rezerwacje.** Pracownicy chcą, żeby po zgłoszeniu „nie ma towaru” sztuka przestała być oferowana, także w internecie. Plan wstrzymuje nowe zobowiązania (rezerwacje) tylko przy przerwanej synchronizacji albo nieuzgodnionym stanie całego źródła towaru. Czy to wymaganie etapu 1? | etap 1 | wymagania 3 |
| PI-08 | Czy wyszukiwanie produktów według potrzeby klienta (np. „sucha karma dla dorosłego psa, bez drobiu, do 200 zł”) wchodzi do etapu 1? Wnioskują o nie tylko pracownicy. | etap 1 | wymagania 8 |
| PI-09 | **Pilotaż.** Czy miary z pilotażu (czas całej czynności z czekaniem, ukończenie za pierwszym razem, powrót rozbieżności, praca nadal wykonywana poza Aportem) przyjąć jako kryteria oceny Aportu? Kto zmierzy obecny czas tych czynności przed pilotażem? Ile tabletów na sklep przyjąć na start? | pilotaż | PRD 5, 10; wymagania 6; NFR 8 |
| PI-10 | Kto jest właścicielem procesu sprzedaży w sklepie po stronie Pupilii? W jakim zakresie z Aportu korzystają magazyn i obsługa klienta? | później | karta 1; koncepcja 7 |

Kolejne pytania do sprzedaży, wspólne z innymi działami: PI-13, PI-14, PI-17,
PI-24, PI-27, PI-32.

## 2. IT i architektura programu

| Nr | Pytanie | Blokuje | Gdzie w dokumentach |
|---|---|---|---|
| PI-11 | **Ewidencja zapasu sklepu.** Opis działalności raz łączy ją z kasą, a raz mówi „WMS lub ewidencja sklepu”. Który system prowadzi stan sklepu, wydzieloną pulę (jedną czy kilka) i partie w sklepach? Gdzie zapisuje się przyjęcie dostawy i korekta stanu? | etap 1 | mapa 2; koncepcja 2; wymagania 7; PRD 4; model 2 |
| PI-12 | **Źródło zadań.** Z których systemów pochodzą zadania etapu 1 (dostawy, wycofania partii, komunikaty) i gdzie zapisuje się ich wykonanie? | etap 1 | koncepcja 1; wymagania 7 |
| PI-13 | **Harmonogram.** Kiedy będą gotowe systemy, bez których etap 1 nie ruszy: zarządzanie tożsamością (konta i role), PIM z zatwierdzonymi kartami produktów, repozytorium wiedzy z bramą modeli i platforma integracyjna? Jaka jest kolejność wdrażania pozostałych systemów programu? | etap 1 | mapa 4; koncepcja 5 |
| PI-14 | **Praca bez łączności.** Kasa dziś traci sieć w godzinach szczytu (ok. 16–17). Które czynności w Aporcie muszą działać bez sieci, a które mogą poczekać na połączenie? Jak ustalić, czy czynność, np. zamknięcie przyjęcia, a w etapie 2 wydanie paczki, doszła do skutku, gdy połączenie zerwało się tuż po niej? | etap 1, etap 2 | PRD 3; koncepcja 4; NFR 4 |
| PI-15 | **Progi jakości.** Ile czasu może minąć od zapisu opóźnienia dostawy lub wycofania partii do pojawienia się zadania w Aporcie? Ilu pracowników pracuje w Aporcie równocześnie, także w szczycie? Jaki czas odpowiedzi jest dopuszczalny przy kliencie i w jakich godzinach Aport musi działać? Jak szybko ma następować wylogowanie lub zmiana osoby na wspólnym tablecie? | etap 1 | NFR 1, 2, 5, 7; wymagania 5; PRD 7 |
| PI-16 | Jakim kanałem kierownik ma dostawać alarm o braku sygnału z kasy przez 15 minut: w Aporcie czy innym? | etap 1 | NFR 3 |
| PI-17 | **Asystent dla pracowników.** Opis działalności podaje tylko dla asystenta klientów: kryteria uruchomienia (co najmniej 500 scenariuszy, 98% zgodności ze źródłami), testy po zmianie modelu, model zapasowy, tryb ograniczony i przechowywanie rozmów. Co z tego obowiązuje asystenta w Aporcie i z jakimi progami? Kto zatwierdza jego uruchomienie? | etap 1 | PRD 6; wymagania 4; koncepcja 6; NFR 6 |
| PI-18 | **Zgłoszenia sklepów i komunikaty.** Który system prowadzi zgłoszenia sklepów do logistyki, jakości i IT oraz komunikaty i instrukcje centrali? System CRM obsługuje sprawy klientów, nie sklepów. | etap 1 | mapa 6; koncepcja 3 |
| PI-19 | **Kasa (POS).** Kto prowadzi audyt kasy i kiedy zapadnie decyzja o jej rozbudowie albo wymianie? | później | mapa 1 |
| PI-20 | Jak systemy będą wymieniać dane (sposób, format, częstotliwość)? Czy dziś zamówienia prowadzi platforma e-commerce, a system zamówień (OMS) przejmie je dopiero po wdrożeniu? Jakie statusy będzie miało zamówienie? | później | mapa 3, 5; model 4 |

## 3. Logistyka

| Nr | Pytanie | Blokuje | Gdzie w dokumentach |
|---|---|---|---|
| PI-21 | Jakie limity obowiązują sklep przy odbiorach: liczba, masa i objętość przechowywanych paczek oraz liczba wydań? Jaki towar i w jakiej ilości trafia do wydzielonej puli? Pytanie do uzgodnienia z kierownikami i sprzedażą. | etap 2 | reguły 5 |

Zgłoszenia różnic w dostawie: zob. PI-18.

## 4. Dział jakości

| Nr | Pytanie | Blokuje | Gdzie w dokumentach |
|---|---|---|---|
| PI-22 | Jak partia, którą oszacowano z ruchów kodów EAN (a nie potwierdzono), wiąże się ze sprzedażą i zwrotami w sklepie? Co sklep raportuje jakości, gdy partii nie da się ustalić? | etap 1 | model 8 |

Priorytet wycofania partii na liście zadań: zob. PI-06.

## 5. Obsługa klienta i sprzedaż internetowa

| Nr | Pytanie | Blokuje | Gdzie w dokumentach |
|---|---|---|---|
| PI-23 | **Potwierdzenie odbioru.** Czym klient potwierdza prawo do odbioru: jednorazowym kodem (tak mówi plan), numerem z SMS-a, kodem w telefonie? Co robi pracownik, gdy klient zna tylko numer zamówienia? | etap 2 | karta 6; słownik 6 |
| PI-24 | **Zwrot zakupu internetowego w sklepie.** Plan mówi o „dowolnym sklepie”, a dyrektorka chce zacząć od wybranych placówek i rodzajów zakupów. Które sklepy i jakie zakupy? Kiedy sprawę przejmuje obsługa klienta? | później | karta 7; reguły 3 |
| PI-25 | Czy jedno zamówienie może łączyć kilka sposobów otrzymania towaru, np. część z puli sklepu, a część z magazynu? | etap 2 | model 3 |
| PI-26 | **Klient w sklepie.** Jakie formy identyfikatora klienta są planowane (kod z aplikacji, numer telefonu, karta klienta)? Czy pracownik sklepu ma widzieć historię zakupów klienta? Plan mówi, że identyfikator nie daje do niej dostępu. | później | karta 9; słownik 5 |

## 6. Controlling i finanse

| Nr | Pytanie | Blokuje | Gdzie w dokumentach |
|---|---|---|---|
| PI-27 | **Wynik sklepu z zamówień internetowych.** Jak liczyć udział sklepu, gdy klient zmieni koszyk, otrzyma kilka propozycji albo zwróci towar? Czy propozycja koszyka od doradcy, „zapisanie karmy na koncie klientki” i zestaw zaproponowany przez asystenta klientów to ta sama rzecz? Czy wynik wpływa na premię? Kto w sklepie widzi marżę: czy kierownik? | później | karta 8; PRD 8; słownik 7; model 6 |
| PI-28 | Na jakiej podstawie prawnej faktury na firmę nie wystawia się do paragonu wydanego bez NIP? Kierownik odsyła do księgowości. | później | reguły 8 |

## 7. Dane produktowe, marketing i sprzedaż

| Nr | Pytanie | Blokuje | Gdzie w dokumentach |
|---|---|---|---|
| PI-29 | Ile kodów EAN może mieć jeden wariant handlowy (SKU), np. po zmianie opakowania? Jak klient i doradca dowiedzą się, że to ten sam produkt? | etap 1 | model 1 |
| PI-30 | Jak sklep ma poznawać warunki promocji, zwłaszcza tych, które obowiązują tylko w jednym kanale? Czy cena, promocja i dostępność przy karcie produktu wchodzą do etapu 1 Aportu? Wymagania etapu 1 ich nie obejmują, a komunikaty mają etap nieustalony. | etap 1 | reguły 7 |
| PI-31 | Czym są „Tropek” (ma wysyłać klientce przypomnienie), „cena klubowa”, „karta klienta” i „stały rabat” dla klienta biznesowego? Nazwy padają w wywiadzie TO-BE („Tropka” wprowadza analityk [TO-BE 00:04:38]), ale nie ma ich w opisie działalności. Czym różni się lista zakupowa od stałego zestawu na koncie klienta? | później | karta 10; słownik 10; model 5 |
| PI-32 | **Klienci biznesowi.** Czy duże zamówienia z terminem, płatnością i miejscem odbioru ustalonymi z góry oraz stały rabat naliczany w kasie wchodzą w zakres? Kto ustala rabat: dziś negocjacje prowadzi dział handlowy centrali. Czy Aport ma obsługiwać reklamacje zakupów z kasy (wymaga osobnej decyzji)? | później | karta 11; reguły 6; PRD 2 |
| PI-33 | Brakuje regulaminu zwrotów sklepu stacjonarnego (termin, wyłączenia). Kto może go przekazać? | później | karta 12; reguły 4 |

## Do decyzji w zespole projektu

Te sprawy dotyczą nazewnictwa w dokumentach. Nie trzeba ich zadawać
interesariuszom.

- Słowo „rezerwacja” stosować tylko dla 15-minutowej blokady koszyka przed płatnością;
  telefoniczne odłożenie nazywać „odłożeniem” (słownik 1).
- Pisać „wariant handlowy (SKU)”, bo w rozmowie „wariant” bywa smakiem albo
  gramaturą (słownik 4).
- Przy „zwrocie” wskazywać proces: anulowanie, odstąpienie, reklamacja albo zwrot
  środków (słownik 8).
- „Zamówienie” w dokumentach TO-BE oznacza zamówienie internetowe; zamówienie
  sklepowe do dostawy nazywać wprost (słownik 9).
- „Zgłoszenie” pisać z dopełnieniem: sprawa klienta w CRM, zgłoszenie sklepu
  do centrali albo zgłoszenie rozbieżności (słownik 11).
- „Dostawa do sklepu” to zatowarowanie; zamówienie klienta to „dostawa paczki
  do sklepu” (słownik 12).

## Dokumenty źródłowe pytań

Projekt `projects/pupilia/Outputs/`: [PRD](prd-aport.md),
[wymagania etapu 1](wymagania-aport-etap-1.md),
[karta procesu TO-BE](karta-procesu-sprzedaz-w-sklepie.md),
[koncepcja architektury](koncepcja-architektury-aport.md),
[NFR](nfr-aport.md). Wiki:
[[wiki/domain/pupilia-slownik|słownik]],
[[wiki/domain/pupilia-reguly-sprzedazy|reguły]],
[[wiki/domain/pupilia-model-dziedziny|model dziedziny]],
[[wiki/architecture/pupilia-systemy|mapa systemów]].
Pytania z tych dokumentów połączono w PI-01–PI-33 i sprawy nazewnictwa.
Dokumenty odsyłają do tej listy.

## Odpowiedzi

Format wpisu: numer PI, data, kto odpowiedział, treść odpowiedzi, dokumenty do
aktualizacji w kolejnej wersji. Brak odpowiedzi.
