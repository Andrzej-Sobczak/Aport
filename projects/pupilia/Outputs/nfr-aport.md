---
title: "Wymagania jakościowe (NFR): Aport dla Pupilii"
type: artifact
artifact_type: nfr-catalog
knowledge_area: architecture
---

# Wymagania jakościowe (NFR): Aport dla Pupilii

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — NFR-01–NFR-25 w treści z tego dnia. Wymagania oznaczone
„Nie ustalono” nie mają przez to progu; pytania pozostają otwarte.

## Kontekst

Wymagania jakościowe dla Aportu, środowiska pracy pracowników sklepów Pupilii.
Zakres funkcji określają [PRD](prd-aport.md) i
[wymagania etapu 1](wymagania-aport-etap-1.md). Miejsce Aportu wśród systemów
opisuje [koncepcja architektury](koncepcja-architektury-aport.md).

Potrzeba: pracownik ma obsłużyć klienta przy półce i dokończyć czynność bez
czekania na kierownika, kasę lub telefon [DYR 00:13:06, 00:42:33]. Przy dwóch
osobach na zmianie każde odejście od kasy zatrzymuje obsługę [AS-IS 00:01:12].

**Skala (OPIS w. 65–69; październik 2026 — Dziś, koniec 2030 — Plan):**

| | Październik 2026 | Koniec 2030 |
|---|---:|---:|
| Sklepy | 95 | 200 |
| Pracownicy sklepów | 400 | 830 |

Wcześniejszych etapów źródła nie podają, a liczby równoczesnych użytkowników
nie da się z nich wyznaczyć (pytanie 2).

Źródła progów: OPIS — `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md`
(numer wiersza); DYR — `raw/inbox/pupilia_wywiad_dyrektorka.md`; AS-IS —
`raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md` (znacznik czasu).
Status: **Plan** (OPIS), **Kierunek** (DYR, bez decyzji), **Interpretacja**
(wniosek analityka). Progi podano tylko tam, gdzie podaje je źródło. Wymagania
funkcjonalne o podobnym celu, np. W-05, W-06, W-28, są w specyfikacji; tutaj
jest tylko ich strona jakościowa.

## Wymagania

### Aktualność danych

| Id | Wymaganie | Warunki lub obciążenie | Miara i próg albo reguła zgodności | Sposób weryfikacji | Źródło |
|---|---|---|---|---|---|
| NFR-01 | Dostępność pokazana w Aporcie jako bieżąca nie jest starsza niż dopuszcza reguła | Odczyt z pamięci podręcznej lub repliki | Wiek danych ≤ 60 s; starsze dane nie są pokazywane jako bieżące | Test z repliką opóźnioną o 59 s i 61 s | Plan: OPIS w. 127; reguła P-06 |
| NFR-02 | Zdarzenie operacyjne (np. opóźniona dostawa, wycofanie partii) pojawia się na liście zadań w trakcie zmiany, niezależnie od nocnego zasilania hurtowni | Zdarzenie zarejestrowane w systemie źródłowym w godzinach pracy sklepu | Próg nie podany; źródło wymaga tylko „w trakcie pracy”, nie następnego dnia (pytanie 1) | Pomiar czasu od zapisu zdarzenia do widoczności w Aporcie | Plan: OPIS w. 321; Kierunek: DYR 00:48:30, 01:00:27. Dotyczy W-08 |
| NFR-03 | Każdy widok z liczbami pokazuje okres, źródło i czas odświeżenia danych | Pulpit kierownika (etap nieustalony) | Reguła zgodności: trzy informacje przy każdym widoku | Przegląd widoków | Plan: OPIS w. 218; Kierunek: DYR 00:48:30 |
| NFR-04 | Wynik dzienny w raportach jest uzgodniony rano, a brak danych ze sklepu jest widoczny przy liczbie | Raport zarządczy z hurtowni | Do 8:00 następnego dnia operacyjnego; raport z brakującym źródłem oznaczony jako niepełny | Kontrola zasilania i oznaczeń | Plan: OPIS w. 321; Kierunek: DYR 01:00:27 |

### Niezawodność i ciągłość działania

| Id | Wymaganie | Warunki lub obciążenie | Miara i próg albo reguła zgodności | Sposób weryfikacji | Źródło |
|---|---|---|---|---|---|
| NFR-05 | Brak sygnału z POS jest wykrywany i zgłaszany | Kasa sklepu nie wysyła danych | Alarm po 15 min dla wsparcia IT i kierownika sklepu. Czy kierownik dostaje go w Aporcie — pytanie 3 | Test z odłączoną kasą | Plan: OPIS w. 129; reguła P-08 |
| NFR-06 | Przy nieuzgodnionym stanie źródła towaru Aport nie pozwala przyjmować nowych zobowiązań z tego źródła | Etap 2 (wydzielona pula, odbiory); przerwana synchronizacja, brak ciągłości zdarzeń | Reguła zgodności P-07 | Test przerwania synchronizacji | Plan: OPIS w. 129 |
| NFR-07 | Gdy asystent nie odpowiada, karty produktów i instrukcje pozostają dostępne | Awaria modeli lub bramy modeli, większy ruch po kampanii | Reguła zgodności: dostęp do kart i instrukcji bez asystenta. Czasu przełączenia i dostępności nie podano | Test z wyłączonym asystentem, w próbie w sklepie przy kliencie | Kierunek: DYR 00:52:59. Dotyczy W-28. Dla AsAI OPIS w. 283 opisuje tryb ograniczony (pytanie 6) |
| NFR-08 | Przerwaną czynność (np. przyjęcie dostawy) można dokończyć bez utraty tego, co już zapisano | Przerwanie przez wezwanie do kasy, zmiana osoby | Reguła zgodności: zapisane pozycje nie giną po przerwaniu. Czasu przekazania nie podano („chwila”) | Test przerwania i przejęcia przez inną osobę | Kierunek: DYR 00:44:49. Dotyczy W-13 |
| NFR-09 | Po utracie połączenia w trakcie czynności da się ustalić, czy czynność doszła do skutku, a ponowienie nie dubluje skutku | Etap 2: wydanie paczki. Interpretacja: także zamknięcie przyjęcia i korekta | Reguła zgodności: jeden skutek przy ponowieniu; stan czynności możliwy do sprawdzenia na miejscu | Test zerwania połączenia tuż po potwierdzeniu | Kierunek: DYR 00:36:02, 01:01:19; Plan dla zamówień i płatności: OPIS w. 135 |
| NFR-10 | Zachowanie Aportu bez łączności sieciowej | Kasa dziś traci sieć w szczycie (16–17) | Nie ustalono (pytanie 4) | — | AS-IS 00:59:30; OPIS w. 300 (tylko POS) |
| NFR-11 | Dostępność usługi w godzinach pracy sklepów | — | Nie ustalono (pytanie 5) | — | Brak w źródłach |

### Wydajność i użyteczność

| Id | Wymaganie | Warunki lub obciążenie | Miara i próg albo reguła zgodności | Sposób weryfikacji | Źródło |
|---|---|---|---|---|---|
| NFR-12 | Czas odpowiedzi przy kliencie (karta produktu, porównanie, odpowiedź asystenta) | Doradca przy półce z klientem | Nie ustalono; dyrektorka oczekuje, że doradca „szybko dostanie odpowiedź” (pytanie 5) | — | Kierunek: DYR 00:49:13 |
| NFR-13 | Czas całej czynności w Aporcie, łącznie z czekaniem na odpowiedź lub decyzję, nie rośnie w stosunku do obecnego sposobu | Pilotaż, różne placówki i zmiany | Miara: czas czynności, ukończenie za pierwszym razem, powrót rozbieżności następnego dnia, praca wykonywana nadal poza Aportem. Progu i wartości bazowej nie podano | Obserwacja w pilotażu bez podpowiedzi zespołu projektu | Kierunek: DYR 00:56:38, 01:03:28 |
| NFR-14 | Aport działa na sprzęcie sklepowym: tablet z czytnikiem kodów dwuwymiarowych i drukarka etykiet; aplikacja WWW responsywna | Tablet przenoszony na salę i zaplecze | Reguła zgodności: czynności etapu 1 wykonalne na tablecie z czytnikiem | Test na docelowym tablecie | Plan: OPIS w. 200, 208; Kierunek: DYR 00:42:33 |

### Bezpieczeństwo i rozliczalność

| Id | Wymaganie | Warunki lub obciążenie | Miara i próg albo reguła zgodności | Sposób weryfikacji | Źródło |
|---|---|---|---|---|---|
| NFR-15 | Dostęp według sklepu, roli i zadania, nadawany przez usługę zarządzania tożsamością | Wszyscy użytkownicy | Reguła zgodności: brak dostępu do zadań i danych innego sklepu i innej roli | Test uprawnień dla par rola–sklep | Plan: OPIS w. 208, 307 |
| NFR-16 | Każda czynność ewidencyjna jest przypisana do osoby, także na wspólnym tablecie | Zmiana użytkownika na jednym urządzeniu | Reguła zgodności: zapis wskazuje osobę, która wykonała czynność. Czasu automatycznego wylogowania nie podano (pytanie 7) | Test dwóch kolejnych użytkowników | Plan: OPIS w. 208; Kierunek: DYR 00:42:33. Dotyczy W-06 |
| NFR-17 | Usługa danych sprawdza dostęp przed przekazaniem treści do modelu; uprawnienia i limity są kontrolowane poza modelem | Asystent pracowników; procedury wewnętrzne, warunki zakupu, dane kosztowe | Reguła zgodności: treść bez uprawnienia nie trafia do modelu | Testy uprawnień asystenta | Plan: OPIS w. 224, 265 |
| NFR-18 | Pytania, dokumenty i odpowiedzi modelu są kontrolowane pod kątem wstrzyknięcia instrukcji, ujawnienia informacji, podmiany źródeł i użycia niedozwolonych narzędzi | Asystent pracowników | Reguła zgodności; zestaw testów nie podany | Testy bezpieczeństwa asystenta | Plan: OPIS w. 265 |
| NFR-19 | Asystent w Aporcie ma własną tożsamość techniczną, zestaw narzędzi, zakres źródeł i uprawnienia, odrębne od AsAI | Wspólna brama modeli | Reguła zgodności | Przegląd konfiguracji | Plan: OPIS w. 263 |
| NFR-20 | Model językowy nie wykonuje dowolnych zapytań do baz produkcyjnych; miary liczy warstwa analityczna | Asystent wyjaśniający wyniki | Reguła zgodności | Przegląd narzędzi dostępnych asystentowi | Plan: OPIS w. 226 |
| NFR-21 | Czynności ewidencyjne nie są wykonywane aparatem prywatnego telefonu | Przyjęcia, korekty, wydania | Reguła zgodności P-28 | Przegląd dopuszczonych urządzeń | Plan: OPIS w. 208 |

### Jakość asystenta i danych

| Id | Wymaganie | Warunki lub obciążenie | Miara i próg albo reguła zgodności | Sposób weryfikacji | Źródło |
|---|---|---|---|---|---|
| NFR-22 | Asystent w Aporcie przechodzi własne testy akceptacyjne przed uruchomieniem | Asystent pracowników | Progów nie podano. Dla AsAI: ≥ 500 scenariuszy, zgodność ze źródłami ≥ 98% (≥ 95% w każdym obszarze), zero błędów krytycznych (pytanie 6) | Zbiór scenariuszy odseparowany od danych rozwojowych | Plan: OPIS w. 263; dla AsAI w. 269–273 |
| NFR-23 | Zmiana modelu, instrukcji, narzędzi lub wiedzy wymaga testów regresji; zmiana modelu lub uprawnień — pełnych testów krytycznych | Utrzymanie asystenta | Reguła zgodności. OPIS opisuje ją w części o AsAI (pytanie 6) | Rejestr zmian i wyników testów | Plan: OPIS w. 279 |
| NFR-24 | Zdarzenia Aportu trafiają do hurtowni z pochodzeniem, czasem zdarzenia i czasem pozyskania; identyfikatory analityczne nie są danymi logowania | Zasilanie hurtowni | Reguła zgodności | Kontrola jakości danych w hurtowni | Plan: OPIS w. 319 |
| NFR-25 | Dzienniki rozmów z asystentem są przechowywane zgodnie z polityką retencji | Asystent pracowników | Okresu nie podano; OPIS zapowiada politykę retencji z odrębnymi okresami dla rozmów | — | Plan: OPIS w. 147, 259 (dla AsAI) |

## Konflikty i pytania

Pytania zebrano też w [liście pytań do interesariuszy](pytania-do-interesariuszy.md);
odpowiedzi są zapisywane tam.

1. **Czas pojawienia się zdarzenia na liście zadań (NFR-02, W-08).** Ile minut
   wolno minąć od zapisu opóźnienia lub wycofania partii do widoczności
   w Aporcie? Czy wycofanie partii ma krótszy próg niż inne zadania?
2. **Obciążenie.** Ilu pracowników pracuje w Aporcie równocześnie na zmianę
   i w szczycie (dostawa, kampania)? Ile sklepów obejmie pilotaż i etap 1?
3. **Alarm o braku sygnału z POS (NFR-05).** Czy kierownik ma go dostawać
   w Aporcie, czy innym kanałem?
4. **Praca bez łączności (NFR-10).** Które czynności etapu 1 muszą działać bez
   sieci, np. skanowanie przy przyjęciu, a które mogą czekać na połączenie?
   Kasa traci sieć w szczycie [AS-IS 00:59:30]. (PRD, pytanie 3; koncepcja,
   pytanie 4)
5. **Czas odpowiedzi i dostępność usługi (NFR-11, NFR-12).** Jakie progi
   przyjąć i w jakich godzinach Aport musi działać? Źródła ich nie podają
   (PRD, pytanie 7).
6. **Asystent pracowników a kryteria AsAI (NFR-07, NFR-22, NFR-23, NFR-25).**
   OPIS podaje kryteria uruchomienia, regresję, model zapasowy, tryb ograniczony
   i retencję tylko dla AsAI [w. 269–283]. Co z tego obowiązuje asystenta
   w Aporcie i z jakimi progami? (PRD, pytanie 6)
7. **Wspólny tablet (NFR-16).** Jak szybko ma następować wylogowanie lub
   przełączenie użytkownika? Wymóg rozliczalności i szybkiego przekazania
   tabletu mogą się wykluczać; źródła nie rozstrzygają.
8. **Wartości bazowe pilotażu (NFR-13).** Kto zmierzy obecny czas czynności
   (przyjęcie dostawy, wyjaśnienie rozbieżności) przed pilotażem, żeby było
   z czym porównać?
