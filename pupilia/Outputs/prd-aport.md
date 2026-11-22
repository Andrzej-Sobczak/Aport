---
title: "PRD: Aport — środowisko pracy pracowników sklepów Pupilii"
type: artifact
artifact_type: prd
knowledge_area: product
---

# PRD: Aport — środowisko pracy pracowników sklepów Pupilii

Produkt: **Aport**, planowana aplikacja do codziennej pracy sklepów sieci Pupilia
i ich współpracy z centralą.

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — PRD w treści z tego dnia. Pytania z ostatniej sekcji pozostają
otwarte; kierunki rozwoju nie są przez to uzgodnione.

Źródła (pełne ścieżki w ostatniej sekcji): **OPIS** — opis działalności (numer
wiersza), **DYR** — wywiad z dyrektorką sprzedaży, **AS-IS** i **TO-BE** —
wywiady z kierownikiem i doradczynią sklepu (znacznik czasu). Status treści:
**Plan** — zapis w OPIS; **Kierunek** — wypowiedź dyrektorki bez podjętej decyzji;
**Postulat** — oczekiwanie pracowników sklepu. Pojęcia wyjaśnia
[[wiki/domain/pupilia-slownik|słownik]], reguły —
[[wiki/domain/pupilia-reguly-sprzedazy|reguły biznesowe]], przebieg sprzedaży —
[[wiki/domain/pupilia-proces-sprzedazy-as-is|proces AS-IS]] i
[karta procesu TO-BE](karta-procesu-sprzedaz-w-sklepie.md).

## Problem i cel

**Problem (stan obecny, fakty ze źródeł):**

- Informacje potrzebne przy kliencie są rozproszone: stan w kasie bywa
  nieprawdziwy, więc każde pytanie wymaga obejścia sali i zaplecza
  [AS-IS 00:18:16, 00:58:30; DYR 00:02:23]. Opis produktu daje tylko etykieta,
  nieaktualny segregator i strona WWW [AS-IS 00:10:04].
- Komunikaty, promocje i korespondencja z centralą trafiają na skrzynkę kierownika;
  pod jego nieobecność zmiana nie zna warunków promocji ani statusu reklamacji
  [AS-IS 00:40:46, 00:50:35; DYR 00:46:57].
- Ustalenia między zmianami przekazuje się ustnie, na karteczkach i w zeszycie;
  zdarza się sprzedaż odłożonego towaru [AS-IS 00:22:37, 00:23:12; DYR 00:44:49].
- Zgłoszenia do centrali giną w poczcie; sklep nie wie, kto prowadzi sprawę
  [AS-IS 00:16:26; DYR 00:47:42].
- Wynik sklepu obejmuje tylko kasę; praca doradcy zakończona zakupem
  w internecie jest niewidoczna [AS-IS 00:17:10, 01:02:47; DYR 00:06:55].
- Przy dwóch osobach na zmianie każde odejście od kasy zatrzymuje obsługę
  [AS-IS 00:01:12; DYR 00:04:39].

**Cel (Plan):** jedno środowisko pracy, w którym pracownik sklepu widzi zadania
swojej zmiany, wykonuje czynności sklepowe i ma pod ręką wiedzę potrzebną przy
kliencie. Aport udostępnia funkcje systemów nadrzędnych i nie prowadzi własnej
ewidencji [OPIS w. 200–202]. Dyrektorka ujmuje cel tak: pracownik sam przy kasie
ma wiedzieć, co powiedzieć klientowi, bez arkusza, telefonu do kierownika
i szukania maila [DYR 00:13:06].

**Związek z celami programu (interpretacja):** Aport jest jednym z elementów
[[wiki/product/pupilia-program|programu rozwoju Pupilii do 2030 r.]]. Na wynik
pracy sklepów wpływają zwłaszcza mierniki: gotowość zamówień w obiecanym terminie,
anulowania z braku towaru i dostępność oferty podstawowej na półce
[OPIS w. 340–342]. To cele całego programu, a nie Aportu samego; źródła nie
podają celów liczbowych dla Aportu.

## Odbiorcy i potrzeby

| Odbiorca | Potrzeba | Status i źródło |
|---|---|---|
| Doradca klienta (pracownik sklepu) | Przy półce: dokładny wariant, skład, cena, dostępność, warunki promocji, z odnośnikiem do karty produktu | Plan [OPIS w. 208, 224]; Kierunek [DYR 00:42:33, 00:49:13]; Postulat [TO-BE 00:01:19, 00:16:04] |
| | Zadania i ustalenia widoczne dla kolejnej zmiany; możliwość przerwania i dokończenia czynności | Kierunek [DYR 00:44:49]; Postulat [TO-BE 00:14:29] |
| | Zgłoszenie braku towaru bez czekania na kierownika | Kierunek [DYR 00:45:31]; Postulat [TO-BE 00:14:29] |
| Kierownik sklepu | Rano: co jest pilne i co wymaga decyzji, z priorytetem (np. wycofanie partii przed kampanią) | Plan [OPIS w. 206]; Kierunek [DYR 00:41:07] |
| | Przyjęcie dostawy z porównaniem do dokumentu i śledzeniem braku | Plan [OPIS w. 212]; Kierunek [DYR 00:44:07] |
| | Zgłoszenia rozbieżności w jednym miejscu; korekta z uprawnieniem i powodem | Plan [OPIS w. 214]; Kierunek [DYR 00:45:31]; Postulat [TO-BE 00:14:29] |
| | Pulpit: sprzedaż, plan, zapas zalegający, braki, straty, terminowość, z okresem i czasem odświeżenia | Plan [OPIS w. 218]; Kierunek [DYR 00:48:30] |
| | Wynik sklepu obejmujący zakupy internetowe z porad doradców | Plan [OPIS w. 153]; Kierunek [DYR 00:26:30]; Postulat [TO-BE 00:21:36] |
| Centrala: logistyka, jakość, wsparcie IT, właściciel kategorii | Zgłoszenia sklepów kierowane według rodzaju sprawy; informacja, co sklep sprawdził | Plan [OPIS w. 220]; Kierunek [DYR 00:46:14, 00:47:42] |
| Magazyn centralny, COK | Ograniczony zakres pracy w Aporcie; konsultanci COK pracują w CRM | Plan [OPIS w. 200] |

## Zakres

Zakres według OPIS (Plan). Kolumna „Etap” podaje kierunek dyrektorki
[DYR 00:55:07]; tam, gdzie go nie ma, etap jest nieustalony (pytanie 1).

| Obszar | Co obejmuje | Źródło | Etap (Kierunek) |
|---|---|---|---|
| Zadania na zmianie | Zadania według roli i lokalizacji, kolejność według terminu i skutku opóźnienia; zapis wykonawcy, czasu i wyniku w systemie źródłowym | OPIS w. 206 | 1 — pierwsze sklepy |
| Przyjęcie dostaw | Skanowanie, porównanie z dokumentem wysyłki, zgłoszenie uszkodzeń, niedoborów i nadwyżek | OPIS w. 212 | 1 |
| Rozbieżności i korekty stanu | Zgłoszenie rozbieżności; korekta, inwentaryzacja, przesunięcie i odpis jako odrębne operacje z uprawnieniem (reguła P-27) | OPIS w. 214 | 1 — zgłaszanie rozbieżności; korekty i pozostałe operacje stanu w etapie 1 to Interpretacja |
| Asystent dla pracowników | Wyszukiwanie wiedzy produktowej i procedur ze wskazaniem źródła i wersji | OPIS w. 224 | 1 — równolegle, na zatwierdzonych kartach produktów |
| Uzupełnienia zapasu | Korekta propozycji uzupełnień i domówienia | OPIS w. 212; DYR 00:17:07 | nieustalony |
| Pulpit kierownika | Sprzedaż, marża w dopuszczonym zakresie, dostępność, zapas zalegający, straty, terminowość; okres, źródło i czas odświeżenia przy każdym widoku | OPIS w. 218 | nieustalony |
| Komunikaty i zgłoszenia do centrali | Komunikaty, instrukcje i szkolenia w jednym miejscu; zgłoszenia do logistyki, jakości lub IT | OPIS w. 220; DYR 00:46:57, 00:47:42 | nieustalony |
| Wydzielona pula | Potwierdzenie przesunięcia towaru do puli (reguła P-02) | OPIS w. 115 | 2 — z odbiorami |
| Odbiory zamówień | Zadanie kompletacji z terminem, przyjęcie paczek, wydanie klientowi (reguły P-17–P-21) | OPIS w. 176, 184 | 2 — gdy gotowe są sklep, magazyn i COK |
| Propozycja koszyka | Koszyk przygotowany przez doradcę, zatwierdzany przez klienta w WWW lub aplikacji (reguła P-14) | OPIS w. 153; DYR 00:25:40 | nieustalony |
| Zwroty zakupów internetowych | Rejestracja przyjęcia zwrotu i odłożenie do oceny (reguła P-26) | OPIS w. 196; DYR 00:37:29 | nieustalony; zakres do ustalenia |

**Sprzęt i dostęp (Plan):** tablety z czytnikami kodów dwuwymiarowych, drukarki
etykiet; dostęp według sklepu i zadania przez usługę zarządzania tożsamością;
każdy pracownik na własnym koncie, także na wspólnym tablecie
[OPIS w. 208; DYR 00:42:33].

## Wyłączenia

- Aport nie jest kasą, księgą ani rejestrem zapasu. Zamówienia pozostają w OMS,
  ruchy towarowe w WMS lub ewidencji sklepu, sprzedaż fiskalna w POS, rozrachunki
  w ERP [OPIS w. 202]. Zmiany w kasie (np. wyszukiwanie, korekty) zależą od
  decyzji po audycie POS [OPIS w. 309; DYR 00:43:18].
- Konsultanci COK nie pracują w Aporcie, tylko w CRM [OPIS w. 200].
- Aport nie przydziela pracy; robi to kierownik. Aport pokazuje pilność i termin
  [DYR 00:41:52].
- O blokadzie i dopuszczeniu towaru do sprzedaży decyduje dział jakości; sklep
  zabezpiecza towar i raportuje [DYR 00:46:14].
- Zmiany warunków opłaconego zamówienia, płatności i zwroty środków prowadzą
  właściwe zespoły [DYR 00:40:27; OPIS w. 178].
- Asystent nie wykonuje dowolnych zapytań do baz produkcyjnych; miary liczy
  warstwa analityczna [OPIS w. 226].
- Kompletacja zamówień z półek sali sprzedaży [OPIS w. 115].
- Aparaty prywatnych telefonów do czynności ewidencyjnych [OPIS w. 208].
- Funkcje dla klienta (asystent AsAI, konto, aplikacja mobilna) to osobne
  produkty programu [OPIS w. 230, 309].

## Kierunki rozwoju

| Kierunek | Potrzeba lub oczekiwany efekt | Stan: rozważany lub uzgodniony |
|---|---|---|
| Odłożenia telefoniczne w Aporcie | Odłożona sztuka widoczna jako zajęta w Aporcie i w kasie; zadanie odniesienia po terminie [TO-BE 00:10:45] | Rozważany; decyzja nie zapadła [DYR 00:29:34] |
| Odłożenie towaru w innym sklepie | Doradca sprawdza wolną sztukę w innym sklepie i prosi o odłożenie [TO-BE 00:08:11] | Rozważany (postulat); brak w OPIS |
| Zamówienie składane w sklepie za klienta | Zamówienie z dostawą przy pustej półce, płatność w kasie lub linkiem [TO-BE 00:08:11] | Rozważany (postulat); OPIS przewiduje zatwierdzenie przez klienta [w. 153] |
| Duże zamówienia klientów biznesowych | Termin, płatność i miejsce odbioru uzgodnione z góry [TO-BE 00:10:45] | Rozważany; do uzgodnienia po stronie sprzedaży [DYR 00:30:16] |
| Reklamacje zakupów z kasy | Zgłoszenie ze zdjęciami i numerem sprawy, status widoczny dla każdej zmiany [TO-BE 00:19:20] | Rozważany; wymaga osobnej decyzji [DYR 00:38:07] |
| Historia zakupów klienta w sklepie | „To, co zawsze” bez pamięci doradcy [TO-BE 00:04:38] | Rozważany (postulat). Według P-11 sam identyfikator nie daje dostępu do historii; według dyrektorki dostęp do historii wymaga potwierdzenia tożsamości [DYR 00:23:40] |
| Asystent wyjaśniający wyniki i rekomendacje | Dlaczego rośnie zapas, ryzyko braku podstawowego SKU [OPIS w. 226] | Plan; według dyrektorki później, po ustaleniu miar [DYR 00:50:04] |

## Najważniejsze scenariusze i warunki powodzenia

**Scenariusze** (szczegóły w karcie procesu i regułach):

1. **Początek zmiany.** Kierownik widzi pilne sprawy i termin każdej, np. zagrożoną
   dostawę albo odbiór; przydziela pracę [DYR 00:41:07, 00:41:52, 00:48:30].
2. **Przyjęcie dostawy z brakiem.** Pracownik porównuje dostawę z dokumentem,
   zgłasza brak i przyjmuje potwierdzoną część; gdy zostanie odwołany do kasy,
   druga osoba dokańcza od miejsca przerwania [DYR 00:44:07, 00:44:49; OPIS w. 212].
3. **Brak towaru wbrew stanowi.** Doradca zgłasza rozbieżność przy produkcie,
   kolejna zmiana ją widzi, kierownik koryguje stan [karta T10; reguła P-27;
   DYR 00:45:31].
4. **Porada przy półce.** Doradca porównuje warianty na tablecie i otwiera kartę
   produktu, z której pochodzi odpowiedź [karta T1; DYR 00:49:13].
5. **Zakup później w internecie.** Doradca przygotowuje propozycję koszyka; zakup
   z niej trafia do wyniku sklepu [karta T2; reguła P-14].
6. **Odbiór zamówienia (etap 2).** Zadanie kompletacji, gotowość dopiero po
   pełnej kompletacji, wydanie po sprawdzeniu uprawnienia [karta T6–T8;
   reguły P-17–P-20].

**Warunki powodzenia pilotażu (Kierunek, DYR):**

- Mierzy się czas całej czynności z czekaniem na odpowiedź lub decyzję, ukończenie
  sprawy za pierwszym razem, powrót rozbieżności następnego dnia oraz to, co
  pracownik nadal robił poza Aportem [DYR 00:56:38].
- Pilotaż w kilku placówkach o różnym zapleczu i ruchu, z udziałem osób
  prowadzących zmiany na co dzień, bez podpowiedzi zespołu projektu
  [DYR 00:55:55, 01:03:28].
- Placówka potwierdza gotowość i zgłasza kłopot na tyle wcześnie, żeby można
  było zareagować [DYR 00:57:30].
- Wstrzymanie wdrożenia w kolejnych sklepach: wydanie towaru niewłaściwej osobie,
  możliwość sprzedaży wycofanej partii, brak ustalenia, czy paczkę wydano i czy
  klient otrzymał pieniądze [DYR 01:01:19].
- Odbiory nie mogą zabierać czasu na obsługę klientów przy półce; ocena obejmuje
  obie strony [DYR 01:01:58].

**Odpowiedzialność za decyzje (Kierunek, DYR 01:02:46):** dyrektorka sprzedaży —
zakres, kolejność wdrożenia i przyjęcie Aportu do pracy w sklepach; logistyka —
dostawy i braki; jakość — blokady; obsługa klienta — zmiany zamówień; finanse —
rozliczenia; IT — rozwiązanie możliwe do uruchomienia i utrzymania.

## Źródła i pytania

Źródła, wszystkie przeczytane w całości:

- OPIS: `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md` (w. 1–347; głównie sekcje 5–7, 9–10);
- DYR: `raw/inbox/pupilia_wywiad_dyrektorka.md`;
- AS-IS: `raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md`;
- TO-BE: `raw/inbox/pupilia_wywiad_sprzedaz_w_sklepie_TO-BE.md`.

Pytania (zebrane też w [liście pytań do interesariuszy](pytania-do-interesariuszy.md);
odpowiedzi są zapisywane tam):

1. **Etapy i terminy.** Źródła nie podają dat ani etapu dla pulpitu, uzupełnień,
   komunikatów, propozycji koszyka i zwrotów. Które z nich wchodzą do pierwszego
   wdrożenia?
2. **Decyzje zakresu:** odłożenia telefoniczne, duże zamówienia, reklamacje
   zakupów z kasy (tabela „Kierunki rozwoju”). Kto i kiedy je podejmie?
3. **Praca bez łączności.** OPIS przewiduje ją dla POS [w. 300], dla Aportu nie mówi
   nic. Kasa dziś traci łączność w szczycie [AS-IS 00:59:30].
4. **Gdzie jest ewidencjonowana wydzielona pula** — w WMS czy w ewidencji sklepu
   [OPIS w. 202]?
5. **Liczba tabletów na sklep** zależy od tego, jak często zadania nakładają się
   w czasie; do sprawdzenia w pilotażu [DYR 00:42:33].
6. **Kryteria odbioru asystenta w Aporcie.** OPIS podaje kryteria tylko dla AsAI
   (500 scenariuszy, 98% zgodności) [w. 269–273]. Czy obowiązują też asystenta
   pracowników?
7. **Wymagania jakościowe** (czas odpowiedzi, dostępność usługi, liczba
   użytkowników) nie są podane. Znane są: okres, źródło i czas odświeżenia przy
   widokach [OPIS w. 218], zadania niezależne od nocnego zasilania hurtowni
   [OPIS w. 321], dane dostępności do 60 sekund (reguła P-06).
8. **Kto widzi marżę** w pulpicie — „osoby, które mają na jej podstawie podejmować
   decyzje” [DYR 00:48:30]. Czy kierownik sklepu?
9. **Zmiany w kasie** oczekiwane przez pracowników (wyszukiwanie ze zdjęciem,
   zawieszenie rachunku, korekty przez doradcę) [TO-BE 00:16:04] są poza Aportem.
   Kto je prowadzi i czy wejdą do audytu POS?
10. **Cele dla Aportu.** Źródła podają cele programu, nie Aportu. Czy przyjąć
    miary pilotażu z wypowiedzi dyrektorki jako kryteria produktu?
