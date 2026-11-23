# Aport dla Pupilii

## Cel i zakres

Projekt Aportu, czyli środowiska pracy pracowników sklepów sieci Pupilia.
Obejmuje opis produktu (PRD), wymagania etapu 1, architekturę rozwiązania
i docelowy proces sprzedaży w sklepie (TO-BE). Stan obecny, opracowany w tym
projekcie, jest wiedzą o sieci i leży w wiki. Funkcje dla klienta (AsAI, konto, aplikacja mobilna) są poza zakresem
projektu.

## Kontekst

- Program: [[wiki/product/pupilia-program|program rozwoju Pupilii do 2030 r.]]
  (cel, skala, mierniki).
- Słownik: [[wiki/domain/pupilia-slownik|słownik pojęć Pupilii]].
- Reguły: [[wiki/domain/pupilia-reguly-sprzedazy|reguły biznesowe sprzedaży Pupilii]]
  (dziś i plan).
- Model: [[wiki/domain/pupilia-model-dziedziny|model dziedziny Pupilii]].
- Proces obecny: [[wiki/domain/pupilia-proces-sprzedazy-as-is|sprzedaż w sklepie (AS-IS)]].
- Systemy: [[wiki/architecture/pupilia-systemy|mapa systemów i integracji Pupilii]].

Wiedza wspólna dla sieci — cele programu, definicje, reguły, relacje, proces
obecny i mapa systemów — jest w wiki; dokumenty projektu do niej odsyłają.
W projekcie jest tylko to, co dotyczy Aportu.

## Materiały i wyniki prac

Oryginały są wspólne dla bazy i leżą w `raw/inbox/` pod nazwami, pod którymi
je otrzymano. Projekt odsyła do nich ścieżką, dlatego `Inputs/files/` jest pusty.

- `raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md` — kierownik i doradczyni, stan obecny
- `raw/inbox/pupilia_wywiad_sprzedaz_w_sklepie_TO-BE.md` — kierownik i doradczyni, oczekiwania
- `raw/inbox/pupilia_wywiad_dyrektorka.md` — dyrektorka sprzedaży, kierunki dla sieci
- `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md` — opis działalności i planów firmy

Rezultaty:

- [PRD: Aport](Outputs/prd-aport.md).
- [Wymagania: etap 1](Outputs/wymagania-aport-etap-1.md) — W-01–W-29.
- [Historyjki: etap 1](Outputs/historyjki-aport-etap-1.md) — H-01–H-13, odsyłają
  do wymagań.
- [Karta procesu: sprzedaż w sklepie z Aportem](Outputs/karta-procesu-sprzedaz-w-sklepie.md)
  — przebieg docelowy (TO-BE).
- [Koncepcja architektury](Outputs/koncepcja-architektury-aport.md) — miejsce
  Aportu wśród systemów, zależności etapu 1.
- [Wymagania jakościowe (NFR)](Outputs/nfr-aport.md) — NFR-01–NFR-25, progi tylko
  ze źródeł.
- [Pytania do interesariuszy](Outputs/pytania-do-interesariuszy.md) — PI-01–PI-33.

## Pytania i decyzje

Otwarte pytania ze wszystkich dokumentów, także z wiki, zebrano w
[liście pytań do interesariuszy](Outputs/pytania-do-interesariuszy.md), według
adresatów i z oznaczeniem, co blokują. Odpowiedź zapisuj raz, w sekcji
„Odpowiedzi” tej listy; zatwierdzone dokumenty aktualizuj w ich kolejnej wersji.

Decyzja z 2026-11-22, Andrzej Sobczak (ekspert ds. procesów i cyfryzacji):
zatwierdzone w treści z tego dnia

- w wiki: słownik, reguły biznesowe (D-01–D-12, P-01–P-28), model dziedziny,
  proces sprzedaży AS-IS i mapa systemów;
- w projekcie: PRD, wymagania etapu 1 (W-01–W-29), historyjki (H-01–H-13),
  karta procesu TO-BE, koncepcja architektury, NFR (NFR-01–NFR-25)
  i lista pytań do interesariuszy (PI-01–PI-33).

Pytania we wszystkich dokumentach są otwarte. Oznaczenia Kierunek, Postulat i Interpretacja zachowują
swoje znaczenie; NFR bez progu („Nie ustalono”) nadal go nie mają.

## Następny krok

Zebranie odpowiedzi na otwarte pytania, zwłaszcza o system ewidencji zapasu
sklepu, źródło zadań, pracę bez łączności i kryteria asystenta. Potem wymagania
etapu 2 (odbiory) po decyzji o zakresie (PRD, pytania 1–2). Przy zmianie
zatwierdzonej treści zachować wersję z 2026-11-22.
