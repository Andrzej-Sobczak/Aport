---
title: "Historyjki użytkownika: Aport dla Pupilii, etap 1"
type: artifact
artifact_type: user-stories
knowledge_area: product
---

# Historyjki użytkownika: Aport dla Pupilii, etap 1

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — historyjki H-01–H-13 w treści z tego dnia. Otwarte sprawy są
w pytaniach specyfikacji wymagań.

## Kontekst

Historyjki dla pierwszego etapu Aportu w sklepach Pupilii: zadania na zmianie,
przyjęcie dostaw, rozbieżności i korekty, asystent i wiedza dla pracowników.
Zakres i wyłączenia są takie same jak w
[specyfikacji wymagań etapu 1](wymagania-aport-etap-1.md). Historyjki opisują
potrzebę i kryteria akceptacji; zachowanie systemu i jego źródło są
w wymaganiach W-xx, do których odsyła każda historyjka.

Role: doradca klienta (pracownik sklepu), kierownik sklepu. Potrzeby pochodzą
z wywiadów: DYR — `raw/inbox/pupilia_wywiad_dyrektorka.md`, TO-BE —
`raw/inbox/pupilia_wywiad_sprzedaz_w_sklepie_TO-BE.md`, AS-IS —
`raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md` (znaczniki czasu) oraz
z opisu działalności, OPIS — `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md`
(numer wiersza).

## Historyjki

### H-01 Pilne sprawy na początku zmiany

Jako kierownik sklepu chcę na początku zmiany zobaczyć, co jest pilne i co wymaga
mojej decyzji, aby rozdzielić pracę, zanim ktoś zacznie czytać wszystkie wiadomości.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Na dziś jest dostawa, komunikat o kampanii i wycofanie partii | Kierownik otwiera Aport | Wycofanie partii jest na górze listy; każda sprawa ma termin |
| Jedna ze spraw wymaga decyzji kierownika | Kierownik przegląda listę | Sprawa jest wyróżniona jako wymagająca decyzji |

Wymagania: W-02, W-03, W-04. Źródło potrzeby: DYR 00:41:07, 00:41:52.

### H-02 Moje zadania

Jako doradca chcę widzieć zadania przypisane do mojej roli i je zamykać, aby
kolejna osoba wiedziała, co już zrobiono.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Doradca jest zalogowany w swoim sklepie | Otwiera listę zadań | Widzi tylko zadania swojej roli i sklepu |
| Zadanie jest wykonane | Doradca je zamyka | W systemie źródłowym zapisano wykonawcę, czas i wynik |

Wymagania: W-01, W-05. Źródło potrzeby: OPIS w. 206; DYR 00:44:49, 00:47:42.

### H-03 Własne konto na wspólnym tablecie

Jako doradca chcę pracować na wspólnym tablecie na własnym koncie, aby było
wiadomo, kto przyjął towar albo zgłosił różnicę.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Sklep ma jeden tablet, na zmianie są dwie osoby | Druga osoba loguje się po pierwszej | Czynności zapisują się na właściwą osobę |
| Pracownik nie ma uprawnienia do korekty stanu | Otwiera produkt | Funkcja korekty jest niedostępna |

Wymagania: W-06, W-07, W-18. Źródło potrzeby: DYR 00:42:33.

### H-04 Przyjęcie dostawy ze zestawieniem

Jako doradca chcę przyjmować dostawę skanerem i od razu widzieć różnice
z dokumentem wysyłki, aby nie liczyć wszystkiego drugi raz.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Dostawa ma dokument wysyłki | Doradca skanuje towar | Zestawienie pokazuje ilość oczekiwaną i przyjętą dla każdej pozycji |
| Brakuje jednego kartonu | Doradca kończy przyjęcie | Przyjęto potwierdzoną część, brak jest zapisany przy dostawie |

Wymagania: W-09, W-10. Źródło potrzeby: DYR 00:44:07; AS-IS 00:20:02 (pomyłki przy przyjęciu wariantu).

### H-05 Zgłoszenie problemu z dostawą

Jako doradca chcę zgłosić uszkodzony lub brakujący towar z dostawy do logistyki,
aby nie szukać, kto się tym zajmie.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Karton jest uszkodzony | Doradca odkłada go i zgłasza uszkodzenie | Zgłoszenie trafia do logistyki z numerem dostawy i pozycją |
| Zgłoszenie zostało rozpatrzone | Doradca otwiera dostawę | Widzi wynik zgłoszenia |

Wymagania: W-11, W-12. Źródło potrzeby: DYR 00:44:07, 00:47:42.

### H-06 Uzupełnienie braku przy następnej dostawie

Jako kierownik chcę przy kolejnej dostawie wiedzieć, czy brak z poprzedniej
uzupełniono, aby zdecydować, czy coś domówić.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| W poprzedniej dostawie zgłoszono brak | Przychodzi kolejna dostawa | Kierownik widzi, czy brak został uzupełniony |

Wymagania: W-12. Źródło potrzeby: DYR 00:44:07.

### H-07 Dokończenie przerwanego przyjęcia

Jako doradca z następnej zmiany chcę dokończyć przyjęcie przerwane przez
koleżankę, aby nie liczyć od nowa.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Przyjęcie przerwano, bo pracownika zawołano do kasy | Inna osoba otwiera tę dostawę | Widzi, ile policzono, co odłożono i czy zgłoszono różnicę |
| Przejmująca osoba kończy liczenie | Zamyka przyjęcie | Wynik obejmuje czynności obu osób, przypisane do każdej z nich |

Wymagania: W-13, W-06. Źródło potrzeby: DYR 00:44:49.

### H-08 Zgłoszenie, że towaru nie ma, choć system go pokazuje

Jako doradca chcę zgłosić przy produkcie, że nie znalazłam towaru, aby
koleżanka z kolejnej zmiany nie szukała go znowu przy następnym telefonie.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| System pokazuje 1 sztukę, na sali i zapleczu jej nie ma | Doradca zgłasza rozbieżność przy produkcie | Zgłoszenie jest zapisane; stan w systemie się nie zmienia |
| Zgłoszenie nie jest wyjaśnione | Inna osoba sprawdza ten produkt | Widzi zgłoszenie, zanim odpowie klientowi |

Wymagania: W-15, W-16. Źródło potrzeby: TO-BE 00:14:29; AS-IS 00:54:59; DYR 00:45:31.

### H-09 Wyjaśnienie i korekta stanu

Jako kierownik chcę mieć zgłoszenia rozbieżności w jednym miejscu i poprawić
stan z podaniem powodu, aby sprawy nie leżały w zeszycie pod kasą.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| W sklepie są otwarte zgłoszenia | Kierownik otwiera listę zgłoszeń | Widzi wszystkie i te, które wymagają jego decyzji |
| Kierownik ustalił, że towaru nie ma | Wykonuje korektę bez podania powodu | Korekta jest odrzucona |
| Kierownik podaje powód | Wykonuje korektę | Stan jest poprawiony; zapis wskazuje osobę i powód; zgłoszenie znika z produktu |

Wymagania: W-17, W-18, W-19. Źródło potrzeby: TO-BE 00:14:29; AS-IS 00:53:07–00:54:39.

### H-10 Porównanie dwóch karm przy półce

Jako doradca chcę zeskanować dwa worki i zobaczyć obok siebie ich skład, aby
pokazać klientce różnicę bez odwracania worków i czytania drobnego druku.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Oba warianty mają zatwierdzone karty produktów | Doradca skanuje dwa kody | Widzi cechy obu wariantów obok siebie, ze źródłem i wersją karty |
| Jeden wariant nie ma zatwierdzonej karty | Doradca skanuje dwa kody | Widzi informację o braku karty i nie dostaje porównania opartego na niepotwierdzonych danych |

Wymagania: W-20, W-21, W-22, W-23. Źródło potrzeby: TO-BE 00:01:19; AS-IS 00:09:04–00:11:30; DYR 00:49:13.

### H-11 Instrukcja dla czynności

Jako kierownik chcę zapytać asystenta, co zrobić z uszkodzonym towarem po
dostawie, aby nie szukać maila z centrali.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Instrukcja istnieje w obowiązującej wersji | Kierownik zadaje pytanie | Otrzymuje odpowiedź z odnośnikiem do instrukcji i numerem wersji |
| Pracownik nie ma uprawnienia do procedur wewnętrznych | Zadaje to samo pytanie | Nie otrzymuje treści, do których nie ma dostępu |

Wymagania: W-20, W-26, W-27. Źródło potrzeby: DYR 00:49:13, 00:46:57; AS-IS 00:40:46.

### H-12 Brak lub błąd w wiedzy

Jako doradca chcę widzieć, kiedy karty brakuje albo informacje są sprzeczne,
i łatwo zgłosić błędną odpowiedź, aby nie zapewniać klienta bez podstawy.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Dwie karty podają sprzeczne informacje | Doradca pyta asystenta | Odpowiedź wskazuje sprzeczność i osobę odpowiedzialną za treść |
| Odpowiedź asystenta jest błędna | Doradca ją zgłasza | Właściciel treści otrzymuje pytanie, odpowiedź i źródło |

Wymagania: W-24, W-25. Źródło potrzeby: DYR 00:18:40, 00:49:42.

### H-13 Praca bez asystenta

Jako doradca chcę mieć karty produktów i instrukcje, gdy asystent nie odpowiada,
aby dalej obsługiwać klientów przy większym ruchu.

| Warunki | Działanie lub zdarzenie | Oczekiwany wynik |
|---|---|---|
| Asystent jest niedostępny | Doradca szuka karty produktu lub instrukcji | Karta i instrukcja otwierają się w Aporcie |

Wymagania: W-28. Źródło potrzeby: DYR 00:52:59.

## Źródła, powiązania i pytania

- Wymagania i ich pytania: [specyfikacja etapu 1](wymagania-aport-etap-1.md).
  Historyjki nie mają osobnego wykazu pytań; otwarte sprawy są tam.
- Pojęcia: [[wiki/domain/pupilia-slownik|słownik]]; reguły:
  [[wiki/domain/pupilia-reguly-sprzedazy|reguły biznesowe]].
- Bez historyjki pozostają W-08 (zdarzenia w trakcie zmiany), W-14 (partia
  oszacowana) i W-29 (wyszukiwanie według potrzeby). W-29 czeka na decyzję
  o zakresie (pytanie 8 w specyfikacji).
