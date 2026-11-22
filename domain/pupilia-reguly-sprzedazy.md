---
title: "Reguły biznesowe: sprzedaż w sklepie i realizacja zamówień Pupilii"
type: artifact
artifact_type: business-rules
knowledge_area: domain
---

# Reguły biznesowe: sprzedaż w sklepie i realizacja zamówień Pupilii

## Kontekst i zakres

Dotyczy sieci sklepów zoologicznych Pupilia: sprzedaży w sklepie stacjonarnym
oraz planowanej realizacji zamówień internetowych z udziałem sklepów, w tym
odbiorów i zwrotów. Znaczenie pojęć podaje
[[wiki/domain/pupilia-slownik|słownik pojęć Pupilii]]. Przebieg obecny opisuje
[[wiki/domain/pupilia-proces-sprzedazy-as-is|proces sprzedaży AS-IS]], a docelowy
z Aportem — [[projects/pupilia/Outputs/karta-procesu-sprzedaz-w-sklepie|karta procesu TO-BE]].

Notatka ma dwie części:

- **Dziś (D)** — reguły stosowane obecnie, według wywiadu z kierownikiem
  i doradczynią jednego sklepu oraz wywiadu z dyrektorką sprzedaży. Część z nich
  to ustalenia wewnętrzne sklepu, a nie zasady sieci; zaznaczono to przy regule.
- **Plan (P)** — reguły modelu docelowego z opisu działalności. Opisują zamiar
  firmy, a nie działające rozwiązanie. Uzupełnienia z wywiadu z dyrektorką,
  których nie ma w opisie, oznaczono przy regule dopiskiem „(kierunek, DYR)”:
  to wypowiedź bez podjętej decyzji.

Oczekiwania pracowników z wywiadu TO-BE nie są regułami. Gdy są sprzeczne
z regułą, opisano je w sekcji pytań.

Oznaczenia źródeł:

- **AS-IS**: `raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md` (znacznik czasu);
- **TO-BE**: `raw/inbox/pupilia_wywiad_sprzedaz_w_sklepie_TO-BE.md` (znacznik czasu);
- **DYR**: `raw/inbox/pupilia_wywiad_dyrektorka.md` (znacznik czasu);
- **OPIS**: `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md` (numer wiersza).

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — reguły D-01–D-12 i P-01–P-28 w treści z tego dnia. Pytania
z ostatniej sekcji pozostają otwarte; ich rozstrzygnięcie zmieni treść i wymaga
zachowania zatwierdzonej wersji.

## Reguły — dziś

| Nr | Treść reguły | Wyjątki | Powiązane pojęcia lub procesy | Źródło i miejsce |
|---|---|---|---|---|
| D-01 | Fakturę na firmę wystawia się tylko wtedy, gdy NIP wpisano do kasy przed zamknięciem paragonu | Brak. Podstawę prawną zna księgowość centrali | POS, sprzedaż w kasie | AS-IS 00:03:24, 00:04:11 |
| D-02 | Usunięcie pozycji z otwartego paragonu wymaga kodu lub karty kierownika albo zastępcy. Do tego czasu kasa jest zablokowana | Brak | Doradca klienta, kierownik sklepu | AS-IS 00:06:47–00:08:50; DYR 00:04:39 |
| D-03 | Gdy cena na półce jest niższa niż w kasie, klient płaci cenę z półki. Korektę na paragonie wykonuje kierownik albo zastępca; dotyczy ona jednego paragonu, nie ceny w systemie | Brak | POS, korekta ceny | AS-IS 00:35:48, 00:36:30, 00:42:08 |
| D-04 | Promocji obowiązującej tylko w sklepie internetowym nie stosuje się w sklepie; nikt w sklepie nie może wyrównać ceny do internetowej | Promocje obowiązujące we wszystkich kanałach | Promocja, kanał sprzedaży | AS-IS 00:37:26, 00:38:10 |
| D-05 | Odłożony towar czeka do 20:00 dnia odłożenia. Ustalenie wewnętrzne sklepu, nie zapis w systemie | Wyjątkowo do 12:00 następnego dnia, gdy klient dzwoni wieczorem. W praktyce towar bywa przetrzymywany 3–4 dni | Odłożenie | AS-IS 00:21:19, 00:21:42 |
| D-06 | Za odłożony towar nie pobiera się przedpłaty; klient płaci całość przy odbiorze, w nowej, zwykłej sprzedaży | Brak | Odłożenie, sprzedaż w kasie | AS-IS 00:24:29, 00:25:01; DYR 00:07:38 |
| D-07 | Sklep nie wydaje zamówień internetowych i nie przyjmuje ich zwrotów; klienta kieruje do infolinii lub formularza | Brak | Zamówienie internetowe, COK | AS-IS 00:32:15–00:33:25, 00:52:47 |
| D-08 | Zwrot pełnowartościowego towaru kupionego w sklepie przyjmuje się z oryginałem paragonu, w terminie i z nienaruszonym opakowaniem; zatwierdza go kierownik albo zastępca | Nie przyjmuje się otwartej karmy ani przysmaków. Termin i pozostałe wyłączenia określa regulamin centrali, którego nie ma w materiałach | Zwrot towaru | AS-IS 00:51:53 |
| D-09 | Rabatu ilościowego nie udziela się w sklepie; negocjacje cenowe prowadzi dział handlowy centrali | Brak | Stały klient (biznesowy) | AS-IS 00:45:31 |
| D-10 | Doradca nie dobiera karmy przy chorobie; o karmie weterynaryjnej decyduje lekarz weterynarii | Brak | Doradztwo | AS-IS 00:14:43; DYR 00:00:45 |
| D-11 | Stan w systemie koryguje kierownik po wyjaśnieniu różnicy; zgłoszenie doradcy nie zmienia stanu w kasie | Termin korekty zależy od wartości towaru i czasu kierownika | Korekta stanu, stan na kasie | AS-IS 00:53:20–00:54:39; DYR 00:03:09 |
| D-12 | Pojedynczego towaru nie zamawia się ani nie przesuwa z innego sklepu pod konkretnego klienta | Kierownik może na własną odpowiedzialność zwiększyć zamówienie sklepowe pod dużego klienta | Przesunięcie międzysklepowe, zamówienie sklepowe | AS-IS 00:29:55, 00:30:35, 00:43:32 |

## Reguły — plan

| Nr | Treść reguły | Wyjątki | Powiązane pojęcia lub procesy | Źródło i miejsce |
|---|---|---|---|---|
| P-01 | Cena regularna jest wspólna dla sieci; promocje mogą zależeć od kanału, lokalizacji i okresu. System prowadzi historię cen, w tym najniższą cenę z 30 dni przed obniżką | Brak | Usługa cen i promocji | OPIS w. 103; DYR 00:19:23 |
| P-02 | Odbiór z zapasu sklepu realizuje się wyłącznie z wydzielonej puli. Przesunięcie do puli pracownik potwierdza w Aporcie, a towaru z puli nie sprzedaje się w kasie. Kompletacji z półek sali nie przewidziano | Brak | Wydzielona pula, odbiór z zapasu sklepu | OPIS w. 115–117 |
| P-03 | Sprzedaż w POS nie pomniejsza wydzielonej puli | Brak | Ewidencja zapasu sklepu, wydzielona pula | OPIS w. 119 |
| P-04 | Gdy produktu nie ma w puli, klient dostaje propozycję dostawy z magazynu centralnego do sklepu albo pod adres | Brak | Dostawa paczki do sklepu | OPIS w. 117; DYR 00:30:57 |
| P-05 | Dostępność = zapas dopuszczony do sprzedaży internetowej − blokady − aktywne rezerwacje − alokacje. Towar w transporcie i zwroty czekające na ocenę jej nie zwiększają | Brak | Dostępność (internetowa) | OPIS w. 125 |
| P-06 | Dane o dostępności z pamięci podręcznej lub repliki można pokazać jako bieżące, jeśli mają najwyżej 60 sekund. Wiążącą rezerwację zawsze potwierdza usługa dostępności | Brak | Usługa dostępności | OPIS w. 127 |
| P-07 | Przerwana synchronizacja, brak ciągłości zdarzeń albo nieuzgodniony stan wstrzymują nowe zobowiązania dla danego źródła towaru do czasu wyjaśnienia | Brak | Usługa dostępności | OPIS w. 129 |
| P-08 | Brak sygnału z POS przez 15 minut uruchamia alarm dla wsparcia IT i kierownika sklepu | Brak | POS | OPIS w. 129 |
| P-09 | Rezerwacja powstaje przy przejściu z koszyka do płatności, obejmuje cały koszyk i zdolność realizacji i trwa 15 minut. Nie powstaje, gdy choć jedna pozycja lub wymagany termin są niedostępne | Brak | Rezerwacja, zdolność realizacji | OPIS w. 133 |
| P-10 | Potwierdzenie płatności zamienia rezerwację w alokację bez ponownego pomniejszania dostępności; brak potwierdzenia w terminie zwalnia rezerwację | Brak | Rezerwacja, alokacja | OPIS w. 135 |
| P-11 | Zakup w kasie trafia do konta klienta tylko po podaniu lub zeskanowaniu identyfikatora. Identyfikator nie daje dostępu do historii zakupów | Zakup bez identyfikatora pozostaje poza historią klienta | Identyfikator klienta, konto klienta | OPIS w. 141–143; DYR 00:23:40 |
| P-12 | Dostęp do zamówienia wymaga uwierzytelnienia albo bezpiecznej weryfikacji; sam numer zamówienia lub nazwisko nie wystarczają | Brak | Konto klienta, zamówienie internetowe | OPIS w. 143; DYR 00:52:17 |
| P-13 | Ponowienie stałego zestawu tworzy nowe zamówienie z aktualną ceną, które klient zatwierdza. Zmiana receptury, wycofanie lub brak wariantu wymagają pokazania różnic i zgody na zamiennik | Automatyczną subskrypcję zarząd rozważy po pilotażu | Stały zestaw | OPIS w. 151; DYR 00:25:03 |
| P-14 | Zamówienie internetowe z propozycji koszyka doradcy wlicza się do wyniku zarządczego sklepu, który uczestniczył w sprzedaży | Zasady liczenia (zmiany koszyka, zwroty) ustalą controlling i sprzedaż internetowa | Propozycja koszyka, wynik zarządczy sklepu | OPIS w. 153; DYR 00:26:30 |
| P-15 | Przed płatnością klient zna cenę brutto, koszt dostawy i wiążący termin realizacji; OMS utrwala te warunki, więc późniejsze zmiany cennika ich nie zmieniają | Brak | Termin realizacji, OMS | OPIS w. 168 |
| P-16 | Koszt dostawy zależy od liczby paczek, masy, wymiarów i trasy; próg bezpłatnej dostawy dla produktów ciężkich uwzględnia marżę po kosztach realizacji | Brak | Zamówienie internetowe | OPIS w. 170; DYR 00:20:54 |
| P-17 | Zamówienie z odbiorem z zapasu sklepu jest gotowe do 2 godzin od płatności w godzinach otwarcia | Opłacone później niż godzinę przed zamknięciem — gotowe następnego dnia otwarcia do 11:00 | Odbiór z zapasu sklepu, kompletacja | OPIS w. 174 |
| P-18 | Powiadomienie o gotowości z jednorazowym kodem odbioru wychodzi dopiero po pełnej kompletacji (odbiór z puli) albo po przyjęciu w sklepie wszystkich paczek (paczka do sklepu). Status przewoźnika nie oznacza gotowości | Brak | Gotowość do odbioru, kod odbioru | OPIS w. 176, 184; DYR 00:35:14 |
| P-19 | Gdy przy kompletacji brakuje pozycji, stan jest weryfikowany, a klient wybiera realizację częściową, inny wariant albo anulowanie; zamówienie czeka na odpowiedź. Zmianę opłaconego zamówienia przeprowadza osoba uprawniona (kierunek, DYR) | Wyjątek nierozwiązany w terminie przejmuje COK | Kompletacja, COK | OPIS w. 178; DYR 00:34:29 |
| P-20 | Na odbiór są 3 dni otwarcia sklepu od dnia następującego po potwierdzeniu gotowości. Przy nieodebraniu pracownik potwierdza fizyczną obecność towaru; po przyjęciu go do zapasu następuje zwrot środków | Brak | Gotowość do odbioru, zwrot środków | OPIS w. 180; DYR 00:36:43 |
| P-21 | Paczka z magazynu dociera do sklepu w ciągu 2 dni roboczych od wydania; wysyłkę, przyjęcie w sklepie i wydanie klientowi potwierdza się skanem | Brak | Dostawa paczki do sklepu | OPIS w. 184 |
| P-22 | Zamówienie o masie wysyłkowej powyżej 30 kg dzieli się na paczki zgodnie z limitami przewoźnika | Brak | Dostawa paczki do sklepu | OPIS w. 186 |
| P-23 | Sklep ma limity liczby, łącznej masy i objętości przechowywanych paczek oraz zdolności wydawania; osiągnięcie któregokolwiek wyłącza nowe terminy dla tej placówki | Kierownik może ograniczyć przyjmowanie nowych odbiorów, np. przy mniejszej obsadzie (kierunek, DYR) | Zdolność realizacji | OPIS w. 186; DYR 00:33:08, 00:33:51 |
| P-24 | COK odpowiada w ciągu jednego dnia roboczego, a w sprawach płatności lub wydania paczki — w ciągu 4 godzin pracy COK (pn–sb 8:00–20:00) | Poza godzinami pracy: AsAI i formularz z informacją o czasie odpowiedzi | COK, sprawa | OPIS w. 190; DYR 00:39:35 |
| P-25 | Anulowanie przed wydaniem, odstąpienie od umowy, reklamacja i zwrot środków to odrębne procesy z własnymi statusami i odpowiedzialnością | Brak | Zwrot towaru, reklamacja | OPIS w. 194; DYR 00:38:07 |
| P-26 | Zakup internetowy można zwrócić przez przewoźnika albo w sklepie; sklep rejestruje przyjęcie w Aporcie, a towar trafia do miejsca oceny i nie zwiększa automatycznie zapasu | Zakres zwrotów i placówek nie jest ustalony (kierunek, DYR; zob. pytanie 3) | Zwrot towaru, miejsce oceny | OPIS w. 196; DYR 00:37:29, 00:38:07 |
| P-27 | Korekta stanu wymaga uprawnienia i uzasadnienia; inwentaryzacja, przesunięcie i odpis to odrębne operacje. Pracownik może zgłosić rozbieżność bez korekty (kierunek, DYR) | Brak | Korekta stanu, zgłoszenie rozbieżności | OPIS w. 214; DYR 00:45:31 |
| P-28 | Do czynności ewidencyjnych nie używa się aparatów prywatnych telefonów | Brak | Aport | OPIS w. 208 |

## Pytania i rozbieżności

Pytania zebrano w
[[projects/pupilia/Outputs/pytania-do-interesariuszy|liście pytań do interesariuszy]]
projektu Aport; odpowiedzi są zapisywane tam.

1. **Korekty w kasie.** Dziś usunięcie pozycji i korekta ceny wymagają kierownika
   (D-02, D-03). Pracownicy chcą, żeby doradca robił to sam, z zapisem osoby i czasu,
   a cenę poprawiał w ustalonym limicie [TO-BE 00:16:04]. Dyrektorka: „korektę robi
   uprawniona osoba”, a o kasie zdecyduje audyt POS [DYR 00:43:18; OPIS w. 309].
   Czy reguła ma się zmienić i jaki byłby limit?
2. **Odłożenie telefoniczne w modelu docelowym.** Plan nie zawiera reguły dla
   odłożeń. Dyrektorka chce ustalić czas oczekiwania i odpowiedzialność, gdy
   odłożenie uzgodniły dwie placówki [DYR 00:29:34]. Czy D-05 i D-06 pozostają,
   a jeśli tak, czy w systemie?
3. **Zwrot zakupu internetowego w sklepie.** OPIS: „w dowolnym sklepie” [w. 196].
   Dyrektorka: najpierw ustalenie, jakie zakupy i w których placówkach [DYR 00:37:29].
   Do czasu decyzji obowiązuje D-07.
4. **Regulamin zwrotów** (termin, wyłączenia) — brak w materiałach [AS-IS 00:52:36].
5. **Wartości limitów** zdolności sklepu (P-23) i skład wydzielonej puli (P-02) nie są
   podane. Ustalą je kierownik z logistyką i sprzedażą [DYR 00:30:57, 00:33:08].
6. **Rabat dla klienta biznesowego.** Dziś brak (D-09). Kierownik oczekuje, że kasa
   naliczy stały rabat ustalony przez centralę [TO-BE 00:10:45]. Plan tego nie opisuje.
7. **Promocje internetowe w sklepie.** D-04 opisuje stan dzisiejszy. P-01 pozwala
   na promocje zależne od kanału, więc ta różnica może pozostać. Plan nie mówi,
   jak sklep poznaje warunki promocji; pracownicy chcą je widzieć w Aporcie i w kasie
   [TO-BE 00:16:04].
8. **Podstawa prawna D-01** nie została potwierdzona; kierownik odsyła do księgowości
   [AS-IS 00:04:11].
