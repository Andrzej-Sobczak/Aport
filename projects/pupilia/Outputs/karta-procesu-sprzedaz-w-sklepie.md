---
title: "Karta procesu: sprzedaż w sklepie Pupilii z Aportem (TO-BE)"
type: artifact
artifact_type: business-process-card
knowledge_area: domain
---

# Karta procesu: sprzedaż w sklepie Pupilii z Aportem (TO-BE)

Dotyczy: sieci sklepów zoologicznych Pupilia, sprzedaży w sklepie stacjonarnym
oraz planowanego środowiska pracy pracowników **Aport**.

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — karta w treści z tego dnia, z zachowaniem oznaczeń Plan, Kierunek
i Postulat. Pytania pozostają otwarte.

Oznaczenia źródeł (pełne ścieżki w sekcji „Źródła”): **TO-BE** — wywiad
o oczekiwaniach sklepu, **DYR** — wywiad z dyrektorką sprzedaży, **OPIS** — opis
działalności Pupilii (numer wiersza), **AS-IS** — wywiad o stanie obecnym.
W nawiasach podano znacznik czasu nagrania.

## Cel i granice

Karta opisuje docelowy przebieg sprzedaży w sklepie z Aportem. Stan obecny
— początek i koniec procesu, role, warunki pracy, kroki A1–F3 i zakończenia
K1–K5, do których odsyłają kroki poniżej — opisuje
[[wiki/domain/pupilia-proces-sprzedazy-as-is|proces sprzedaży AS-IS]].
Granice są takie same: przyjęcie dostaw, zamawianie towaru do sklepu,
inwentaryzacja, wycofanie partii i obsługa w COK pojawiają się tylko tam,
gdzie przerywają sprzedaż.

## Przebieg TO-BE

Źródła różnią się statusem. **Plan** — opis docelowego modelu w OPIS;
**Kierunek** — wypowiedź dyrektorki bez podjętej decyzji; **Postulat** —
oczekiwanie pracowników sklepu z wywiadu TO-BE. Żaden z tych zapisów nie jest
zatwierdzonym przebiegiem procesu.

| Krok | Rola | Działanie i wynik | Status i źródło | Następny krok i warunek przejścia |
|---|---|---|---|---|
| T1 | Doradca | Przy półce, na tablecie z Aportem, skanuje warianty i porównuje skład, cenę i dostępność. Odpowiedź asystenta wskazuje źródło i wersję karty produktu | Plan [OPIS w. 208, 224]; Kierunek [DYR 00:42:33, 00:49:13]; Postulat [TO-BE 00:01:19] | Zakup od razu: T5. Zakup później: T2. Brak towaru: T3 |
| T2 | Doradca, klient | Doradca przygotowuje propozycję koszyka z identyfikatorem sklepu i pracownika. Klient otwiera ją w serwisie WWW lub aplikacji i sam zatwierdza zamówienie | Plan [OPIS w. 153]; Kierunek [DYR 00:25:40] | Zamówienie trafia do wyniku zarządczego sklepu [OPIS w. 153]. Zasady liczenia nie są ustalone [DYR 00:26:30] |
| T3 | Doradca | Przy braku na półce sprawdza dostępność w magazynie i informuje o terminie i koszcie dostawy. Składa zamówienie w sklepie; klient płaci w kasie lub przez link | Postulat [TO-BE 00:08:11]. OPIS opisuje zatwierdzenie zamówienia przez klienta [w. 153] (zob. pytanie 4) | Kurier albo odbiór w automacie [TO-BE 00:08:11]: koniec po stronie sklepu. Dostawa paczki do sklepu (Plan [OPIS w. 117]): T6a |
| T4 | Doradca, inny sklep | Sprawdza w Aporcie wolną sztukę w innym sklepie i wysyła prośbę o odłożenie. Tamten sklep potwierdza; klient dostaje wiadomość z adresem i terminem | Postulat [TO-BE 00:08:11] (zob. pytanie 3) | Odbiór w innym sklepie |
| T5 | Doradca | Sprzedaż w kasie. Klient może podać identyfikator, aby przypisać zakup do konta, albo kupić bez niego. Identyfikator nie daje dostępu do historii zakupów | Plan [OPIS w. 141–143]; Kierunek [DYR 00:23:40] | Koniec |
| T6 | Pracownik sklepu | **Odbiór z puli sklepu:** po płatności w Aporcie pojawia się zadanie kompletacji. Pracownik skanuje pozycje i odkłada towar w strefie odbiorów. Powiadomienie z jednorazowym kodem odbioru wychodzi dopiero po pełnej kompletacji | Plan [OPIS w. 115, 174–176]; Kierunek [DYR 00:28:41] | T8. Gdy brakuje pozycji: T7 |
| T6a | Pracownik sklepu | **Paczka z magazynu do sklepu:** przyjmuje paczki skanem. Gotowość potwierdza się po przyjęciu wszystkich paczek, a nie na podstawie statusu przewoźnika | Plan [OPIS w. 162, 184]; Kierunek [DYR 00:35:14] | T8 |
| T7 | Pracownik, COK | Pracownik sprawdza stan i zgłasza brak. Klient wybiera realizację częściową, inny wariant albo anulowanie; zmianę wprowadza osoba uprawniona. Nierozwiązane w terminie wyjątki przejmuje COK | Plan [OPIS w. 178]; Kierunek [DYR 00:34:29] | T6 lub koniec |
| T8 | Pracownik sklepu | Odnajduje zamówienie, sprawdza uprawnienie do odbioru, wydaje towar i potwierdza wydanie | Plan [OPIS w. 176, 184]; Kierunek [DYR 00:36:02]; Postulat [TO-BE 00:10:45] (zob. pytanie 6) | Koniec. Brak odbioru w ciągu 3 dni otwarcia: sprawdzenie towaru, przyjęcie do zapasu, zwrot środków [OPIS w. 180] |
| T9 | Doradca | **Odłożenie telefoniczne** widoczne w Aporcie i w kasie jako zajęte. Po wygaśnięciu powstaje zadanie odniesienia towaru, a klient dostaje przypomnienie z możliwością przedłużenia | Postulat [TO-BE 00:10:45]. Kierunek: decyzja jeszcze nie zapadła [DYR 00:29:34] (zob. pytanie 2) | C3 (AS-IS) albo T8 |
| T10 | Doradca, kierownik | **Brak towaru wbrew stanowi:** doradca zgłasza to w Aporcie przy produkcie, a kolejna zmiana widzi zgłoszenie. Kierownik dokonuje korekty z uprawnieniem i powodem. Postulat: do wyjaśnienia sztuka nie jest oferowana, także w internecie | Plan: korekta z uprawnieniem i powodem [OPIS w. 214]; Kierunek: zgłoszenie bez czekania na kierownika [DYR 00:45:31]; Postulat: wstrzymanie oferowania sztuki [TO-BE 00:14:29] — plan wstrzymuje zobowiązania tylko dla całego źródła towaru [OPIS w. 129] (zob. PI-07 w liście pytań) | Korekta albo wyjaśnienie dostawy |
| T11 | Doradca | **Korekty w kasie:** sam zdejmuje pozycję przed paragonem, z zapisem osoby i czasu; zawiesza rachunek; poprawia cenę przy starej etykiecie w ustalonym limicie, z powodem i zadaniem wydruku etykiety | Postulat [TO-BE 00:16:04]. Kierunek: „korektę robi uprawniona osoba”; decyzja o kasie po audycie [DYR 00:43:18; OPIS w. 309] (zob. pytanie 5) | A5 |
| T12 | Doradca | Po zeskanowaniu produktu w Aporcie i w kasie widzi cenę, okres promocji i warunki. Kasa nalicza rabat z kuponu | Plan: promocje zależne od kanału i lokalizacji [OPIS w. 103]; Kierunek [DYR 00:19:23]; Postulat [TO-BE 00:16:04] | A5 |
| T13 | Doradca | **Zwrot zamówienia internetowego w sklepie:** rejestruje przyjęcie w Aporcie i odkłada towar do miejsca oceny. Towar nie zwiększa od razu zapasu | Plan: „w dowolnym sklepie” [OPIS w. 196]. Kierunek: zakres zwrotów i placówki do ustalenia [DYR 00:37:29, 00:38:07] (zob. pytanie 7) | Koniec po ocenie towaru |
| T14 | Kierownik, doradca | **Reklamacja zakupu z kasy w Aporcie:** zgłoszenie ze zdjęciami i numerem sprawy; status widzi klient i każda zmiana | Postulat [TO-BE 00:19:20]. Kierunek: wymaga osobnej decyzji [DYR 00:38:07] | Koniec po decyzji |
| T15 | Kierownik | **Duże zamówienia:** termin, sposób płatności i odbiór w sklepie albo dostawa z magazynu uzgodnione z góry; kasa nalicza rabat ustalony przez centralę po zeskanowaniu karty klienta | Postulat [TO-BE 00:10:45]. Kierunek: do uzgodnienia po stronie sprzedaży [DYR 00:30:16] | A1 |

**Mierniki:** cele programu, na które wpływa ten proces (gotowość zamówień
w terminie, anulowania z braku towaru, kolejny zakup w ciągu 90 dni, dostępność
oferty podstawowej na półce), podaje
[[wiki/product/pupilia-program|program rozwoju Pupilii]].
Dyrektorka potwierdza je w wywiadzie [DYR 00:16:17, 00:27:13, 00:57:30, 00:58:17].

Raport sklepu według kierownika ma obejmować sprzedaż w kasie, liczbę zamówień
wydanych i złożonych w sklepie oraz liczbę porad zakończonych zakupem
w internecie, z obrotem i marżą [TO-BE 00:21:36]. Dyrektorka przewiduje marżę
tylko dla osób, które na jej podstawie decydują, a o premii ma zdecydować
osobno [DYR 00:26:30, 00:48:30] (zob. pytanie 8).

## Źródła

- TO-BE: `raw/inbox/pupilia_wywiad_sprzedaz_w_sklepie_TO-BE.md`,
  całość (ok. 08:05–08:28, „wtorek”). Znaczniki są orientacyjne.
- DYR: `raw/inbox/pupilia_wywiad_dyrektorka.md`, całość
  (00:00:00–01:05:00). Znaczniki są orientacyjne.
- OPIS: `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md`, całość
  (wiersze 1–347).
- AS-IS: `raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md`; stan obecny
  opisuje [[wiki/domain/pupilia-proces-sprzedazy-as-is|proces sprzedaży AS-IS]].
- Pojęcia użyte w karcie: [[wiki/domain/pupilia-slownik|słownik pojęć Pupilii]].
- Reguły biznesowe, także planowane: [[wiki/domain/pupilia-reguly-sprzedazy|reguły sprzedaży Pupilii]].

## Pytania

Pytania zebrano w [liście pytań do interesariuszy](pytania-do-interesariuszy.md);
odpowiedzi są zapisywane tam.

1. Kto jest właścicielem procesu sprzedaży w sklepie po stronie Pupilii?
2. Czy telefoniczne odłożenia mają być obsługiwane w Aporcie? Pracownicy tego
   oczekują [TO-BE 00:10:45], a dyrektorka mówi, że decyzja nie zapadła,
   i wskazuje do ustalenia czas oczekiwania oraz odpowiedzialność przy odłożeniu
   uzgodnionym przez dwie placówki [DYR 00:29:34]. Do decyzji pozostaje też
   obecny limit do 20:00 albo do 12:00 następnego dnia.
3. Czy odłożenie w innym sklepie na prośbę z Aportu (T4) wchodzi w zakres?
   OPIS opisuje wydzieloną pulę tylko dla zamówień internetowych [w. 115].
4. Kto składa zamówienie internetowe, gdy klient jest w sklepie? Pracownicy
   chcą składać je sami, z płatnością w kasie lub przez link [TO-BE 00:08:11],
   a OPIS przewiduje, że propozycję koszyka zatwierdza klient [w. 153].
   Czy płatność w kasie za zamówienie internetowe jest planowana?
5. Czy doradca otrzyma uprawnienie do zdjęcia pozycji, zawieszenia rachunku
   i korekty ceny w limicie [TO-BE 00:16:04]? Jaki będzie limit? Dyrektorka mówi
   tylko o „uprawnionej osobie” [DYR 00:43:18], a o kasie zdecyduje audyt POS
   [OPIS w. 309].
6. Jak klient potwierdza uprawnienie do odbioru? Doradczyni wymienia numer z SMS-a
   albo kod w telefonie [TO-BE 00:10:45], a OPIS — jednorazowy kod odbioru
   [w. 176]. Dyrektorka wymaga sprawdzenia uprawnienia, gdy klient zna tylko
   numer zamówienia [DYR 00:36:02].
7. Czy zwrot zamówienia internetowego będzie możliwy „w dowolnym sklepie”
   [OPIS w. 196], czy najpierw w wybranych placówkach i dla określonych zakupów
   [DYR 00:37:29]?
8. Jak liczyć udział sklepu w zamówieniach z porad: zasady controllingu,
   widoczność marży dla kierownika i wpływ na premię [TO-BE 00:21:36;
   DYR 00:26:30, 00:48:30]?
9. Czy w sklepie można sprawdzić historię zakupów klienta po numerze telefonu
   lub kodzie z aplikacji [TO-BE 00:04:38 — „to, co zawsze dla Borysa”]?
   OPIS: identyfikator przy kasie nie daje dostępu do historii [w. 143];
   dyrektorka: dostęp wymaga potwierdzenia tożsamości [DYR 00:23:40].
10. Czym jest „Tropek”, który ma wysyłać klientce przypomnienie [TO-BE 00:04:38]?
    Nazwa nie występuje w OPIS ani w wywiadzie z dyrektorką. Czy chodzi
    o aplikację mobilną, czy o asystenta AsAI?
11. Czy obsługa dużych zamówień i stały rabat dla klienta biznesowego (T15)
    wchodzą w zakres [DYR 00:30:16]? Kto ustala rabat?
12. Treść regulaminu zwrotów sklepu stacjonarnego (termin, wyłączenia) —
    analityk miał otrzymać kopię [AS-IS 00:52:36]; nie ma jej wśród materiałów.
