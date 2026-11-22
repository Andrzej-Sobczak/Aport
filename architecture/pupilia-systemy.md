---
title: "Pupilia: mapa systemów i integracji"
type: artifact
artifact_type: architecture-concept
knowledge_area: architecture
---

# Pupilia: mapa systemów i integracji

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — mapa systemów w treści z tego dnia, z zachowaniem rozróżnienia
Dziś i Plan. Pytania pozostają otwarte.

## Cel i granice

Systemy sieci Pupilia (sklepy, magazyn centralny, centrum obsługi klienta,
centrala): kto prowadzi jakie dane i procesy dziś (październik 2026) i w modelu
docelowym programu do 2030 r. Notatka jest wspólna dla projektów. Koncepcja
konkretnego rozwiązania, np. Aportu, odsyła tutaj i nie powtarza tej mapy.

Oznaczenia: **Dziś** to stan obecny, **Plan** to model docelowy z opisu działalności.
Źródła: OPIS — `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md`
(numer wiersza); AS-IS — `raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md`;
DYR — `raw/inbox/pupilia_wywiad_dyrektorka.md` (znacznik czasu).
Pojęcia wyjaśnia [[wiki/domain/pupilia-slownik|słownik]], reguły:
[[wiki/domain/pupilia-reguly-sprzedazy|reguły biznesowe]].

## Zasady architektoniczne (Plan)

| Zasada | Zakres i wyjątki | Stan | Źródło |
|---|---|---|---|
| Interfejsy użytkowników są oddzielone od systemów prowadzących ewidencję i procesy; WWW, aplikacja mobilna, Aport i usługi AI korzystają z funkcji systemów dziedzinowych | Cała architektura docelowa | Plan | OPIS w. 287 |
| Każdy obszar danych ma właściciela i wskazany system nadrzędny | Wszystkie obszary danych | Plan | OPIS w. 76 |
| Wymianę zdarzeń i wywołań zapewnia platforma integracyjna z rejestrem błędów i kolejką spraw do wyjaśnienia | Integracje między systemami | Plan | OPIS w. 287 |
| ERP i PIM używają wspólnego identyfikatora SKU; właściciel danych określa, który system zmienia dany atrybut | Dane produktowe | Plan | OPIS w. 95 |
| WWW, aplikacja mobilna, Aport i AsAI stosują te same reguły dostępności | Dostępność, rezerwacje (reguły P-05–P-07) | Plan | OPIS w. 127 |
| O dostępie do informacji rozstrzygają systemy, nie model językowy; uprawnienia, operacje i limity są kontrolowane poza modelem | Usługi AI (AsAI, asystent w Aporcie) | Plan | OPIS w. 265 |
| Miary liczy warstwa analityczna na kontrolowanych danych; model językowy ich nie liczy i nie wykonuje dowolnych zapytań do baz produkcyjnych | Asystent w Aporcie | Plan | OPIS w. 226 |
| Sprzedaż w POS, zamówienie w OMS, wydanie, płatność i zapis finansowy są powiązane identyfikatorami pozwalającymi odtworzyć przebieg transakcji | Uzgodnienia operacyjne i finansowe | Plan | OPIS w. 313 |
| Decyzje finansowe, kadrowe i umowne pozostają w gestii ludzi | Narzędzia AI | Plan | OPIS w. 76 |

## Systemy i odpowiedzialności

### Dziś (październik 2026)

| System | Odpowiedzialność | Znane ograniczenia | Źródło |
|---|---|---|---|
| POS (system kasowy) | Sprzedaż fiskalna i podstawowe ruchy towaru, bez identyfikacji klienta | Stary system; w szczycie (ok. 16–17) traci połączenie z systemami centrali. Kasa pokazuje tylko stan własnego sklepu | OPIS w. 48; AS-IS 00:59:30, 00:27:49 |
| ERP | Zakupy, ewidencja zapasu, faktury, księga | Moduł magazynowy bez ewidencji według lokalizacji i partii. Kierownik na komputerze na zapleczu widzi stany innych sklepów, z tymi samymi błędami | OPIS w. 49; AS-IS 00:27:55 |
| Platforma e-commerce | Własny katalog, koszyk, konta klientów | Opisy i ceny wprowadzane ręcznie | OPIS w. 50 |
| WMS | Magazyn centralny | Brak szczegółów w źródłach | OPIS w. 51 |
| Obsługa klienta | Skrzynka pocztowa, centrala telefoniczna, arkusze | Kontakty w osobnych narzędziach; trudno odtworzyć przebieg sprawy | OPIS w. 52, 40 |
| Raportowanie | Arkusze z danymi pobranymi z ERP i POS | Wynik sklepu obejmuje tylko kasę | OPIS w. 53; AS-IS 00:17:10 |
| Komunikacja centrali ze sklepem | Poczta e-mail do kierownika | Pod nieobecność kierownika zmiana nie zna treści | AS-IS 00:40:46, 00:50:35 |

Wymiana danych odbywa się w paczkach kilka razy dziennie; dane sprzedażowe
docierają do centrali z kilkugodzinnym opóźnieniem [OPIS w. 55].

### Docelowo (Plan)

| System lub usługa | Odpowiedzialność | Zmiana w programie | Źródło |
|---|---|---|---|
| ERP | Zakupy, faktury, rozrachunki, wartość zapasu, księga, koszty, kadry i płace, planowanie uzupełnień sklepów; dane handlowe i logistyczne produktu | Rozbudowa | OPIS w. 293, 95, 309 |
| PIM | Zatwierdzone cechy, opisy, zdjęcia i instrukcje produktów, wersje publikacji | Nowy | OPIS w. 294, 309 |
| Usługa cen i promocji | Cennik regularny, promocje, historia cen | Rozbudowa | OPIS w. 295, 309 |
| OMS | Zamówienia, statusy, wybór źródła realizacji; utrwala warunki zamówienia | Nowy | OPIS w. 296, 168, 309 |
| Usługa dostępności | Dostępność, rezerwacje i alokacje zapasu internetowego | Nowy | OPIS w. 297, 123, 309 |
| Platforma e-commerce | Katalog prezentacyjny, koszyk, proces zakupowy, przekazanie zamówienia do OMS | Rozbudowa | OPIS w. 298, 309 |
| WMS | Przyjęcia, lokalizacje, partie, kompletacja, pakowanie, blokady, wydania z magazynu; ilości i ruchy magazynowe | Rozbudowa | OPIS w. 299, 111, 309 |
| POS i ewidencja zapasu sklepu | Sprzedaż fiskalna, ruchy towaru, partie w zakresie faktycznej identyfikacji, praca przy braku łączności | Rozbudowa albo wymiana — decyzja po audycie POS | OPIS w. 300, 309; DYR 00:43:18 |
| Usługa konta klienta | Tożsamość klienta, profile, zgody | Nowy | OPIS w. 301, 309 |
| CRM | Kontakty i sprawy klientów ze wszystkich kanałów | Nowy | OPIS w. 302, 192, 309 |
| Usługa powiadomień | E-mail, SMS, powiadomienia w aplikacji uruchamiane zdarzeniami | Nowy | OPIS w. 303, 309 |
| Operatorzy płatności i transportu | Autoryzacja i rozliczenie płatności, etykiety, zdarzenia przesyłek | Zewnętrzni | OPIS w. 304 |
| Hurtownia danych i BI | Historia, uzgodnione miary, raporty, prognozy, dane do rekomendacji | Nowy | OPIS w. 305, 309 |
| Repozytorium wiedzy i brama modeli | Zatwierdzone treści dla AI, dostęp do dopuszczonych modeli, limity, rejestr użycia | Nowy | OPIS w. 306, 309 |
| Usługa zarządzania tożsamością | Konta pracowników, role, przypisania do lokalizacji, tożsamości techniczne usług | Nowy | OPIS w. 307, 309 |
| Platforma integracyjna | Wymiana zdarzeń i wywołań, rejestr błędów, kolejka spraw do wyjaśnienia | Nowy | OPIS w. 287, 309 |
| Serwis WWW, aplikacja mobilna | Kanały klienta; korzystają z tych samych usług | WWW — rozbudowa; aplikacja — nowa | OPIS w. 164, 309 |
| Aport | Środowisko pracy pracowników sklepów; udostępnia funkcje systemów nadrzędnych, bez własnej ewidencji | Nowy | OPIS w. 200–202, 309 |
| AsAI | Asystent klientów w WWW, potem w aplikacji | Nowy (usługi AI) | OPIS w. 230, 309 |

## Integracje (Plan)

Źródła opisują przepływy danych, ale nie sposób wymiany (protokoły, formaty,
częstotliwość poza wymienionymi niżej).

| Skąd → dokąd | Przekazywane dane | Sposób wymiany | Sytuacje błędne i ograniczenia | Źródło |
|---|---|---|---|---|
| WMS i potwierdzone przesunięcia do pul sklepowych → usługa dostępności | Zapas dopuszczony do sprzedaży internetowej | Nie podano | Przerwana synchronizacja, brak ciągłości zdarzeń lub nieuzgodniony stan wstrzymują nowe zobowiązania dla źródła towaru (P-07) | OPIS w. 123, 129 |
| Usługa dostępności → WWW, aplikacja, Aport, AsAI | Dostępność | Odczyt; pamięć podręczna lub replika dopuszczalna do 60 s | Wiążąca rezerwacja zawsze przez usługę dostępności (P-06) | OPIS w. 127 |
| POS → ewidencja sklepu, planowanie uzupełnień | Sprzedaż, ruchy towaru | Nie podano | Sprzedaż nie pomniejsza wydzielonej puli (P-03). Brak sygnału z POS przez 15 min — alarm dla IT i kierownika (P-08) | OPIS w. 119, 129 |
| E-commerce → OMS | Zamówienie z utrwalonymi warunkami | Nie podano | Identyfikatory operacji chronią przed powieleniem zamówień, płatności i alokacji | OPIS w. 298, 168, 135 |
| OMS → usługa powiadomień → klient | Gotowość, kod odbioru, statusy | Zdarzenia operacyjne | Gotowość dopiero po pełnej kompletacji lub przyjęciu wszystkich paczek (P-18) | OPIS w. 303, 176, 184 |
| Operatorzy transportu → OMS | Zdarzenia przesyłek | Nie podano | Status przewoźnika nie oznacza gotowości do odbioru | OPIS w. 304, 184 |
| ERP ↔ WMS | Uzgodnienie ewidencji ilościowej i wartościowej | Regularne uzgadnianie | Ujawnia rozbieżności do wyjaśnienia | OPIS w. 111 |
| ERP, PIM, cennik → kanały i sklepy | Dane produktów, zatwierdzone treści, cenniki | Nie podano | Publikacja w kanale po uzupełnieniu atrybutów i zatwierdzeniu treści | OPIS w. 97, 103 |
| AsAI → CRM | Sprawa z podsumowaniem i kontekstem | Po potwierdzeniu przez klienta | Bez haseł, danych karty, kodów odbioru; ponowienie nie dubluje sprawy | OPIS w. 192, 253, 257 |
| ERP, POS, OMS, WMS, CRM, PIM, cennik, kanały, AsAI, Aport → hurtownia | Historia z pochodzeniem, czasem zdarzenia i czasem pozyskania | Raz dziennie; uzgodnienie do 8:00 następnego dnia | Raport z brakującymi źródłami oznaczony jako niepełny | OPIS w. 319, 321; DYR 01:00:27 |
| Systemy operacyjne → Aport (zadania) | Zadania bieżące | Niezależnie od nocnego zasilania hurtowni | Czas dostarczenia nie podany | OPIS w. 218, 321 |
| Hurtownia → Aport (analizy) | Trendy, miary | Przez kontrolowaną usługę raportową | — | OPIS w. 218 |

## Pytania

Pytania zebrano też w
[[projects/pupilia/Outputs/pytania-do-interesariuszy|liście pytań do interesariuszy]]
projektu Aport; odpowiedzi są zapisywane tam.

1. **Wybór POS.** Rozbudowa czy wymiana — decyzja po audycie [OPIS w. 309;
   DYR 00:43:18]. Kto prowadzi audyt i kiedy jest decyzja?
2. **Ewidencja zapasu sklepu.** Tabela odpowiedzialności łączy ją z POS [w. 300],
   a Aport zapisuje ruchy „w WMS lub ewidencji sklepu” [w. 202]. Który system
   prowadzi stan sklepu, wydzieloną pulę i partie w sklepach?
3. **Sposób wymiany danych.** Źródła nie podają protokołów, formatów ani
   częstotliwości (poza 60 s dla dostępności i dziennym zasilaniem hurtowni).
4. **Kolejność wdrażania systemów.** Źródła nie podają harmonogramu programu;
   od niego zależy, co Aport zastanie w pierwszych sklepach.
5. **Platforma e-commerce a OMS.** Czy dziś platforma prowadzi zamówienia sama,
   a OMS przejmie je dopiero po wdrożeniu?
6. **Komunikacja z centralą.** Czy komunikaty, instrukcje i zgłoszenia sklepów
   [w. 220] mają własny system nadrzędny, czy są częścią Aportu?

## Źródła i powiązania

- OPIS: przeczytany w całości (w. 1–347); wykorzystane sekcje 2 (tabela IT w. 44–55),
  4–5, 7, 8 (w. 263–265) i 9.
- AS-IS i DYR: fragmenty o systemach i łączności (znaczniki w tabelach).
- Rozwiązanie zbudowane na tej mapie:
  [[projects/pupilia/Outputs/koncepcja-architektury-aport|koncepcja architektury Aportu]].
- Model pojęć: [[wiki/domain/pupilia-model-dziedziny|model dziedziny]].
