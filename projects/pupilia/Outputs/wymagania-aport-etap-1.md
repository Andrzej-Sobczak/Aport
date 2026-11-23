---
title: "Specyfikacja wymagań: Aport dla Pupilii, etap 1"
type: artifact
artifact_type: requirements-specification
knowledge_area: product
---

# Specyfikacja wymagań: Aport dla Pupilii, etap 1

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — wymagania W-01–W-29 w treści z tego dnia, z zachowaniem oznaczeń
statusu źródła (Plan, Kierunek, Postulat, Interpretacja). Pytania z ostatniej
sekcji pozostają otwarte.

## Cel i zakres

Wymagania dla pierwszego etapu Aportu w sklepach Pupilii, zgodnie z
[PRD](prd-aport.md) (zatwierdzony 2026-11-22): zadania na zmianie, przyjęcie
dostaw, zgłaszanie rozbieżności i korekty stanu oraz asystent i wiedza dla
pracowników. Etap opiera się na kierunku dyrektorki: zacząć od spraw, które sklep
załatwia już dziś, i sprawdzić, czy łatwiej je zacząć, przerwać i przekazać
[DYR 00:55:07].

Poza zakresem tego dokumentu: odbiory zamówień i wydzielona pula (etap 2) oraz
obszary bez ustalonego etapu (pulpit kierownika, uzupełnienia zapasu, komunikaty
i zgłoszenia do centrali, propozycja koszyka, zwroty) — PRD, pytanie 1.

Kolumna „Źródło” podaje status: **Plan** (OPIS), **Kierunek** (DYR, bez decyzji),
**Postulat** (TO-BE), **Interpretacja** (wniosek analityka do potwierdzenia).
Oznaczenia źródeł: OPIS — `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md`
(numer wiersza); DYR — `raw/inbox/pupilia_wywiad_dyrektorka.md`; TO-BE —
`raw/inbox/pupilia_wywiad_sprzedaz_w_sklepie_TO-BE.md` (znacznik czasu).

## Wymagania

### Zadania, dostęp i urządzenia

| Identyfikator | Oczekiwane zachowanie lub rezultat | Warunki i kryteria sprawdzenia | Źródło i miejsce |
|---|---|---|---|
| W-01 | Po zalogowaniu pracownik widzi zadania właściwe dla swojej roli i swojego sklepu | Dwie osoby o różnych rolach w jednym sklepie widzą listy zgodne z rolą; pracownik innego sklepu nie widzi zadań tego sklepu | Plan: OPIS w. 206, 208 |
| W-02 | Zadania są uporządkowane według terminu i skutków opóźnienia | Przy jednoczesnym zadaniu „wycofanie partii” i komunikacie o kampanii wycofanie jest wyżej; przy dwóch zwykłych zadaniach wyżej jest to z wcześniejszym terminem | Plan: OPIS w. 206; Kierunek: DYR 00:41:07. Miara „skutku opóźnienia” — pytanie 1 |
| W-03 | Kierownik na początku zmiany widzi, co jest pilne, jaki ma termin i co wymaga jego decyzji | Lista kierownika wyróżnia sprawy wymagające decyzji; każda sprawa ma termin | Kierunek: DYR 00:41:07, 00:41:52 |
| W-04 | Pracę przydziela kierownik; Aport pokazuje pilność i termin, ale nie przydziela pracy sam | Zadanie nie zmienia wykonawcy bez działania kierownika lub pracownika | Kierunek: DYR 00:41:52; sposób przydziału w Aporcie — Interpretacja, pytanie 2 |
| W-05 | Zakończenie zadania zapisuje wykonawcę, czas i wynik w systemie, z którego zadanie pochodzi | Po zamknięciu zadania w systemie źródłowym widać wykonawcę, czas i wynik | Plan: OPIS w. 202, 206. System źródłowy zadań etapu 1 — pytanie 7 |
| W-06 | Każdy pracownik pracuje na własnym koncie, także na wspólnym tablecie; dostęp zależy od sklepu i zadania | Dwie osoby kolejno na jednym tablecie: zapisy czynności wskazują właściwe osoby; pracownik bez uprawnienia nie widzi funkcji | Plan: OPIS w. 208; Kierunek: DYR 00:42:33 |
| W-07 | Czynności ewidencyjne wykonuje się na urządzeniach sklepowych z czytnikiem kodów dwuwymiarowych, nie aparatem prywatnego telefonu | Skanowanie w przyjęciu i korekcie działa na tablecie z czytnikiem | Plan: OPIS w. 208; reguła P-28 |
| W-08 | Opóźnienie lub zagrożenie (np. dostawy) pojawia się na liście zadań w trakcie zmiany, niezależnie od nocnego zasilania hurtowni | Zdarzenie zarejestrowane w trakcie dnia jest widoczne na liście przed końcem zmiany; dopuszczalny czas — pytanie 5 | Plan: OPIS w. 321; Kierunek: DYR 00:48:30 |

### Przyjęcie dostawy

| Identyfikator | Oczekiwane zachowanie lub rezultat | Warunki i kryteria sprawdzenia | Źródło i miejsce |
|---|---|---|---|
| W-09 | Pracownik przyjmuje dostawę, skanując towar, i widzi zestawienie: co sklep miał dostać, a co przyjęto | Dla dostawy z dokumentem wysyłki zestawienie pokazuje różnice w ilościach po pozycjach | Plan: OPIS w. 212; Kierunek: DYR 00:44:07 |
| W-10 | Przy braku sklep przyjmuje potwierdzoną część i odnotowuje brak | Dostawa z brakującym kartonem: przyjęta ilość jest równa zeskanowanej, brak jest zapisany przy dostawie | Kierunek: DYR 00:44:07 |
| W-11 | Uszkodzenie, niedobór lub nadwyżkę pracownik zgłasza do rozstrzygnięcia przez właściwą jednostkę, ze wskazaniem dostawy | Zgłoszenie trafia do logistyki i zawiera numer dostawy, pozycję i rodzaj różnicy | Plan: OPIS w. 212; Kierunek: DYR 00:44:07 |
| W-12 | Sklep widzi, co wynikło ze zgłoszenia, a przy kolejnej dostawie — czy brak uzupełniono | Status zgłoszenia jest widoczny w sklepie; przy następnej dostawie widać informację o uzupełnieniu braku | Kierunek: DYR 00:44:07 |
| W-13 | Przerwane przyjęcie może dokończyć inna osoba; widzi, ile już policzono, co odłożono i czy różnicę zgłoszono | Przyjęcie przerwane w połowie: druga osoba kontynuuje od miejsca przerwania, bez ponownego liczenia | Kierunek: DYR 00:44:49, 00:45:31 |
| W-14 | Partia oszacowana na podstawie ruchów EAN nie jest pokazywana jako potwierdzona | Widok rozróżnia partię potwierdzoną i oszacowaną | Plan: OPIS w. 214 |

### Rozbieżności i korekty stanu

| Identyfikator | Oczekiwane zachowanie lub rezultat | Warunki i kryteria sprawdzenia | Źródło i miejsce |
|---|---|---|---|
| W-15 | Pracownik zgłasza przy produkcie, że nie znalazł towaru albo ile sztuk faktycznie jest, bez czekania na kierownika | Zgłoszenie jest możliwe z uprawnieniami doradcy; stan w systemie się nie zmienia | Kierunek: DYR 00:45:31; Postulat: TO-BE 00:14:29; reguła P-27 |
| W-16 | Zgłoszona rozbieżność jest widoczna przy produkcie dla kolejnych pracowników do czasu wyjaśnienia | Inna osoba, także z kolejnej zmiany, sprawdzająca ten produkt widzi zgłoszenie przed odpowiedzią klientowi | Kierunek: DYR 00:45:31; Postulat: TO-BE 00:14:29 |
| W-17 | Kierownik widzi zgłoszenia rozbieżności razem i wie, które wymagają jego decyzji | Lista zgłoszeń sklepu z oznaczeniem spraw do decyzji kierownika | Kierunek: DYR 00:45:31; Postulat: TO-BE 00:14:29 |
| W-18 | Korekta stanu wymaga uprawnienia i powodu | Próba korekty bez uprawnienia albo bez powodu jest odrzucana; korekta zapisuje osobę i powód | Plan: OPIS w. 214; reguła P-27 |
| W-19 | Inwentaryzacja, przesunięcie i odpis są odrębnymi operacjami, każda z własnym zapisem | Każda operacja ma osobny zapis z rodzajem operacji | Plan: OPIS w. 214 |

### Asystent i wiedza dla pracowników

| Identyfikator | Oczekiwane zachowanie lub rezultat | Warunki i kryteria sprawdzenia | Źródło i miejsce |
|---|---|---|---|
| W-20 | Pracownik wyszukuje wiedzę produktową i procedury; odpowiedź wskazuje źródło i obowiązującą wersję treści | Każda odpowiedź ma odnośnik do źródła z numerem wersji | Plan: OPIS w. 224; Kierunek: DYR 00:49:13 |
| W-21 | Z odpowiedzi o produkcie można otworzyć kartę produktu, z której pochodzi | Kliknięcie źródła otwiera kartę właściwego SKU | Kierunek: DYR 00:49:13; Postulat: TO-BE 00:01:19 |
| W-22 | Asystent korzysta wyłącznie z zatwierdzonych kart produktów; nie uznaje dwóch karm za równoważne bez potwierdzonego składu | Pytanie o produkt bez zatwierdzonej karty kończy się informacją o braku, a nie odpowiedzią z innego źródła | Plan: OPIS w. 97; Kierunek: DYR 00:18:40, 00:55:07 |
| W-23 | Pracownik porównuje dwa warianty przy półce po zeskanowaniu ich kodów | Po zeskanowaniu dwóch kodów widać obok siebie cechy z kart produktów (np. skład analityczny) i wielkość opakowania | Kierunek: DYR 00:42:33, 00:49:13; Postulat: TO-BE 00:01:19 |
| W-24 | Gdy brakuje karty albo informacje są sprzeczne, pracownik to widzi i wie, kogo zapytać | Odpowiedź wskazuje brak lub sprzeczność oraz osobę odpowiedzialną za treść | Kierunek: DYR 00:18:40, 00:49:42 |
| W-25 | Pracownik może jednym działaniem przekazać błędną odpowiedź asystenta osobie odpowiedzialnej za treść | Zgłoszenie zawiera pytanie, odpowiedź i źródło; trafia do właściciela treści | Kierunek: DYR 00:49:42 |
| W-26 | Asystent wskazuje obowiązującą instrukcję dla czynności, np. postępowania z towarem uszkodzonym po dostawie | Pytanie o procedurę zwraca instrukcję w obowiązującej wersji | Kierunek: DYR 00:49:13; Plan: OPIS w. 224 |
| W-27 | Dostęp do procedur wewnętrznych, warunków zakupu i danych kosztowych zależy od uprawnień pracownika | Pracownik bez uprawnienia nie otrzymuje tych treści w odpowiedzi | Plan: OPIS w. 224 |
| W-28 | Gdy asystent nie odpowiada, pracownik nadal ma dostęp do kart produktów i instrukcji | Przy wyłączonym asystencie karty i instrukcje są dostępne w Aporcie | Kierunek: DYR 00:52:59 |
| W-29 | Pracownik wyszukuje produkty według potrzeby klienta, np. „sucha karma dla dorosłego psa, bez drobiu i zbóż, duży worek do 200 zł” | Wynik zawiera tylko produkty spełniające podane cechy, z kartą produktu | Postulat: TO-BE 00:01:19. Zakres — pytanie 8 |

## Reguły, pojęcia i ograniczenia

- Pojęcia: [[wiki/domain/pupilia-slownik|słownik]]; relacje:
  [[wiki/domain/pupilia-model-dziedziny|model dziedziny]].
- Reguły: [[wiki/domain/pupilia-reguly-sprzedazy|reguły biznesowe]], zwłaszcza
  D-11 (dzisiejsza korekta stanu), P-27 (korekta i zgłoszenie) i P-28 (urządzenia).
- Ograniczenia z PRD: Aport nie jest kasą, księgą ani rejestrem zapasu; zapis
  pozostaje w systemach nadrzędnych [OPIS w. 202]. Decyzje o blokadach podejmuje
  dział jakości [DYR 00:46:14].
- Wymagania jakościowe są w [katalogu NFR](nfr-aport.md); progi, których źródła
  nie podają, są tam pytaniami (PRD, pytanie 7).

## Pytania i ustalenia

Pytania zebrano też w [liście pytań do interesariuszy](pytania-do-interesariuszy.md);
odpowiedzi są zapisywane tam.

1. Jak mierzyć „skutek opóźnienia” w kolejności zadań (W-02)? Kto ustala
   priorytety poza wycofaniem partii?
2. Czy kierownik przydziela zadania w Aporcie, czy tylko ustnie na podstawie listy
   (W-04)?
3. Pracownicy chcą wstrzymywać rezerwacje sztuki po zgłoszeniu rozbieżności, także
   w internecie [TO-BE 00:14:29]. Plan wstrzymuje zobowiązania przy nieuzgodnionym
   stanie źródła towaru (reguła P-07), ale nie przy zgłoszeniu dla jednego produktu.
   Czy to wymaganie etapu 1?
4. Kryteria odbioru asystenta pracowników — OPIS podaje je tylko dla AsAI
   [w. 269–273] (PRD, pytanie 6).
5. Wymagania jakościowe: czas pojawienia się zdarzenia na liście (W-08), czas
   odpowiedzi, praca bez łączności (PRD, pytania 3 i 7).
6. Liczba tabletów na sklep — do sprawdzenia w pilotażu [DYR 00:42:33].
7. Z którego systemu pochodzą zadania etapu 1 i gdzie zapisuje się przyjęcie
   i korekta: w WMS czy w ewidencji sklepu [OPIS w. 202]?
8. Czy wyszukiwanie według potrzeby klienta (W-29) wchodzi do etapu 1? Źródłem
   jest tylko postulat.
