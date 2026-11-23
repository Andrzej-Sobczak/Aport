---
title: "Słownik pojęć: sprzedaż w sklepie i kanały Pupilii"
type: artifact
artifact_type: glossary
knowledge_area: domain
---

# Słownik pojęć: sprzedaż w sklepie i kanały Pupilii

## Kontekst

Słownik dotyczy sieci sklepów zoologicznych Pupilia: sprzedaży w sklepie
stacjonarnym, jej powiązań ze sprzedażą internetową oraz planowanych systemów
(Aport, AsAI, OMS, usługa dostępności). Korzystają z niego
[[wiki/domain/pupilia-proces-sprzedazy-as-is|proces sprzedaży AS-IS]] i dokumenty
projektu Aport.

**Zatwierdzenie:** Andrzej Sobczak, ekspert ds. procesów i cyfryzacji,
2026-11-22 — słownik w treści z tego dnia. Pytania z sekcji „Rozbieżności
i pytania” pozostają otwarte; ich rozstrzygnięcie zmieni treść i wymaga
zachowania zatwierdzonej wersji.

Słownik zawiera pojęcia, które występują w źródłach. Przy pojęciach, których znaczenie zależy
od czasu, podano, czy opis dotyczy stanu obecnego (**Dziś**), czy planu (**Plan**). Wypowiedzi dyrektorki bez podjętej
decyzji oznaczono jako **Kierunek**, a wypowiedzi pracowników o tym, jak
ma być, jako **Postulat**. Oznaczenia źródeł są takie same jak
w pozostałych dokumentach Pupilii:

- **AS-IS**: `raw/inbox/pupilia_wywiad_4_sprzedaz_w_sklepie_AS-IS.md` (znacznik czasu);
- **TO-BE**: `raw/inbox/pupilia_wywiad_sprzedaz_w_sklepie_TO-BE.md` (znacznik czasu);
- **DYR**: `raw/inbox/pupilia_wywiad_dyrektorka.md` (znacznik czasu);
- **OPIS**: `raw/inbox/Pupilia_opis_dzialalnosci_wyczyszczona_1_0.md` (numer wiersza).

## Pojęcia

### Role i jednostki

| Termin | Znaczenie w tym kontekście | Synonimy i skróty | Źródło i miejsce |
|---|---|---|---|
| Doradca klienta | Dziś: pracownik sklepu, który obsługuje kasę, salę, towar, dostawy i telefon. Plan: korzysta z Aportu na służbowym tablecie | doradczyni, kasjerka, pracownik sklepu | AS-IS 00:01:49, 00:35:48; DYR 00:42:33; OPIS w. 208 |
| Kierownik sklepu | Dziś: prowadzi grafik, przyjmuje dostawy, kontaktuje się z centralą, zatwierdza korekty w kasie i korekty stanu, widzi stany innych sklepów | szef | AS-IS 00:01:12, 00:27:55, 00:54:03 |
| Zastępca kierownika | Dziś: ma te same uprawnienia do korekt w kasie co kierownik | zastępczyni | AS-IS 00:06:47, 00:51:53 |
| Właściciel kategorii | Osoba w centrali odpowiedzialna za kategorię towarów. Plan: razem z kierownikiem dobiera ofertę lokalną | osoba odpowiedzialna za daną kategorię | AS-IS 00:16:26; DYR 00:13:53; OPIS w. 82 |
| COK | Centrum Obsługi Klienta: kontakt telefoniczny, e-mailowy i w mediach społecznościowych. Plan: prowadzi sprawy w CRM, czynne pn–sb 8:00–20:00 | Centrum Obsługi Klienta, obsługa klienta, infolinia, dział obsługi klienta | OPIS w. 11, 190–192; AS-IS 00:32:56, 00:55:43 |

### Oferta i produkt

| Termin | Znaczenie w tym kontekście | Synonimy i skróty | Źródło i miejsce |
|---|---|---|---|
| Wariant handlowy (SKU) | Jednostka ewidencji asortymentu. Ta sama receptura w opakowaniach 3 kg i 12 kg to dwa SKU. Fabryczny wielopak ma własny identyfikator | SKU, pozycja handlowa, wariant | OPIS w. 91; DYR 00:17:53 |
| EAN | Kod identyfikujący wariant handlowy; w sklepie skanuje się go w kasie | kod kreskowy, kod | OPIS w. 99; AS-IS 00:04:43 |
| Karta produktu | Plan: zatwierdzony opis produktu z PIM (cechy, skład, zdjęcia, instrukcje), z właścicielem i wersją. W serwisie WWW pokazuje też cenę, dostępność i sposoby otrzymania towaru | karta PIM | OPIS w. 95–97, 164, 242; DYR 00:18:40 |
| Oferta podstawowa / lokalna / testowa | Plan: części oferty sklepu liczone jako udział w liczbie aktywnych wariantów; w sklepie standardowym 70/25/5%, w dużym 60/30/10% | asortyment testowy, próby | OPIS w. 82–89; DYR 00:13:53, 00:14:41 |
| Marka własna | Produkty marek Pupilii; ich udział w ofercie rośnie | — | OPIS w. 7; DYR 00:00:45 |
| Zestaw klienta | Lista produktów i ilości w koszyku. Nie tworzy nowego SKU | — | OPIS w. 91 |
| Stały zestaw | Plan: zapisane przez klienta SKU i ilości. Ponowienie tworzy nowe zamówienie z aktualną ceną, które klient zatwierdza. Nie jest subskrypcją; o subskrypcji zarząd zdecyduje po pilotażu | — | OPIS w. 151; DYR 00:25:03 |
| Propozycja koszyka | Plan: koszyk przygotowany przez doradcę w Aporcie, z identyfikatorem sklepu i pracownika. Klient zatwierdza go w serwisie WWW lub aplikacji | — | OPIS w. 153; DYR 00:25:40 |

### Zapas i dostępność

| Termin | Znaczenie w tym kontekście | Synonimy i skróty | Źródło i miejsce |
|---|---|---|---|
| Stan na kasie | Dziś: liczba sztuk w ewidencji sklepu widoczna w POS. Bywa niezgodna ze stanem fizycznym i nie uwzględnia odłożeń | stan w systemie, stan magazynowy | AS-IS 00:18:16, 00:22:08 |
| Ewidencja zapasu sklepu | Plan: prowadzona w POS i aktualizowana sprzedażą. Nie pomniejsza wydzielonej puli | — | OPIS w. 119, 300 |
| Wydzielona pula | Plan: fizycznie oddzielony towar sklepu przeznaczony na zamówienia internetowe z odbiorem w tym sklepie. Przesunięcie do puli potwierdza się w Aporcie. Towar z puli nie jest sprzedawany w kasie. Kierunek: skład puli ustala kierownik z logistyką i sprzedażą | pula sklepowa | OPIS w. 115–119; DYR 00:30:57, 00:31:45 |
| Dostępność (internetowa) | Plan: zapas dopuszczony do sprzedaży internetowej pomniejszony o blokady, aktywne rezerwacje i alokacje. Towar w transporcie i zwroty czekające na ocenę jej nie zwiększają | — | OPIS w. 123–127 |
| Dostępność oferty podstawowej na półce | Miernik: udział dostępnych pozycji wśród wymaganych pozycji oferty podstawowej, mierzony w próbie sklepów i okresów | — | OPIS w. 341; DYR 00:16:17 |
| Odłożenie | Dziś: telefoniczna umowa, że sklep przetrzyma towar dla klienta. Towar leży na zapleczu z karteczką; w systemie nic się nie zmienia; nie ma przedpłaty | odłożenie towaru, rezerwacja (potocznie) | AS-IS 00:20:41–00:25:01; DYR 00:07:38, 00:29:34 |
| Rezerwacja | Plan: blokada całego koszyka i zdolności realizacji, tworzona przy przejściu do płatności i ważna 15 minut | — | OPIS w. 133 |
| Alokacja | Plan: przypisanie zapasu do opłaconego zamówienia, powstające z rezerwacji po potwierdzeniu płatności | — | OPIS w. 135, 297 |
| Blokada | Plan: wyłączenie zapasu ze sprzedaży, np. przy wycofaniu partii. Kierunek: o zakresie blokady decyduje dział jakości | — | OPIS w. 125, 299; DYR 00:46:14 |
| Dostawa do sklepu (zatowarowanie) | Dostawa towaru z magazynu centralnego do zapasu sklepu, z dokumentem wysyłki. Dziś: przy przyjęciu zdarzają się pomyłki wariantu. Plan: przyjęcie przez skanowanie i porównanie z dokumentem wysyłki; uszkodzenia, niedobory i nadwyżki trafiają do rozstrzygnięcia. Kierunek: przy braku sklep przyjmuje potwierdzoną część. Nie mylić z „Dostawą paczki do sklepu” | dostawa, zatowarowanie | AS-IS 00:20:02; OPIS w. 212; DYR 00:44:07 |
| Zgłoszenie rozbieżności | Kierunek: informacja pracownika, że stan w systemie nie zgadza się z rzeczywistością albo z dostawą, opisana bez korekty stanu | rozbieżność | DYR 00:44:07, 00:45:31; TO-BE 00:14:29 |
| Korekta stanu | Zmiana ewidencji przez osobę uprawnioną, z powodem. Dziś robi ją kierownik po wyjaśnieniu sprawy | — | AS-IS 00:53:20–00:54:39; OPIS w. 214; DYR 00:45:31 |
| Przesunięcie międzysklepowe | Dziś: wniosek w systemie, realizowany przy zwykłym zatowarowaniu z magazynu centralnego; nie stosuje się go dla pojedynczego klienta | przesunięcie | AS-IS 00:29:55; OPIS w. 214 |
| Zamówienie sklepowe | Dziś: zamówienie towaru dla sklepu do najbliższej dostawy. Kierownik może je zwiększyć pod dużego klienta, ale system nie zapisuje tego jako zamówienia pod klienta | domówienie | AS-IS 00:43:32; OPIS w. 212 |

### Zamówienie i realizacja

| Termin | Znaczenie w tym kontekście | Synonimy i skróty | Źródło i miejsce |
|---|---|---|---|
| Zamówienie internetowe | Dziś: zamówienie ze sklepu internetowego, realizowane wyłącznie z magazynu centralnego. Plan: prowadzone w OMS, także z odbiorem w sklepie | — | OPIS w. 26, 123; AS-IS 00:32:15 |
| Odbiór z zapasu sklepu | Plan: zamówienie internetowe kompletowane z wydzielonej puli wybranego sklepu. Czas przygotowania do 2 godzin | odbiór w sklepie | OPIS w. 160, 174–176; DYR 00:28:41 |
| Dostawa paczki do sklepu | Plan: magazyn centralny pakuje zamówienie i wysyła paczki do sklepu; mają dotrzeć w ciągu 2 dni roboczych | odbiór w sklepie | OPIS w. 162, 184; DYR 00:28:41 |
| Kompletacja | Zebranie pozycji zamówienia. Plan w sklepie: zadanie w Aporcie, skanowanie pozycji, odłożenie towaru w strefie odbiorów | — | OPIS w. 109, 176 |
| Gotowość do odbioru | Plan: przy odbiorze z zapasu sklepu następuje po pełnej kompletacji, przy dostawie paczki do sklepu — po przyjęciu wszystkich paczek. Sam status przewoźnika nie oznacza gotowości | — | OPIS w. 160–162, 184; DYR 00:35:14 |
| Kod odbioru | Plan: jednorazowy kod wysyłany z powiadomieniem o gotowości | — | OPIS w. 176, 257 |
| Termin realizacji | Plan: wiążący termin podany przed płatnością i utrwalony w OMS. Kierunek: terminowość ocenia się według terminu podanego na początku, a nie po zmianie | obiecany termin, zobowiązanie | OPIS w. 168, 342; DYR 00:58:17 |
| Zdolność realizacji | Plan: miejsce w limicie zleceń sklepu albo w planie magazynu. Sklep ma limity liczby, masy i objętości paczek. Przekroczenie któregokolwiek wyłącza nowe terminy | limit zleceń sklepu | OPIS w. 133, 186; DYR 00:32:29 |
| Strefa odbiorów | Plan: miejsce w sklepie, w którym leży towar przygotowany do wydania | — | OPIS w. 176 |

### Klient

| Termin | Znaczenie w tym kontekście | Synonimy i skróty | Źródło i miejsce |
|---|---|---|---|
| Konto klienta | Plan: wspólne konto dla zakupów w sklepie i w internecie, z listami zakupowymi, stałymi zestawami, zgodami i zgłoszeniami. Konto nie jest wymagane do zakupu | wspólne konto | OPIS w. 141; DYR 00:22:55 |
| Identyfikator klienta | Plan: identyfikator podawany lub skanowany w kasie, żeby przypisać zakup do konta. Nie daje dostępu do historii i nie zastępuje uwierzytelnienia | — | OPIS w. 141–143; DYR 00:23:40 |
| Rozpoznany zakup | Zakup przypisany do konta klienta. Dziś rozpoznaje się tylko zakupy internetowe | rozpoznany klient | OPIS w. 28, 141, 339 |
| Profil zwierzęcia | Plan: imię, gatunek, etap życia, masa i preferencje. Klient może go zmienić lub usunąć. AsAI korzysta z profilu tylko za zgodą klienta | — | OPIS w. 145; DYR 00:24:19 |
| Stały klient | Dziś: klient znany pracownikom z wcześniejszych wizyt, obsługiwany z pamięci, bez zapisu w systemie. Także klient biznesowy z regularnymi dużymi zamówieniami (hodowla, hotel dla psów) | — | AS-IS 00:42:55, 00:56:20 |

### Sprawy posprzedażowe

| Termin | Znaczenie w tym kontekście | Synonimy i skróty | Źródło i miejsce |
|---|---|---|---|
| Anulowanie, odstąpienie, reklamacja, zwrot środków | Plan: cztery odrębne procesy, każdy z własnymi statusami i odpowiedzialnością | — | OPIS w. 194; DYR 00:38:07 |
| Zwrot towaru | Dziś: przyjęcie w sklepie pełnowartościowego towaru kupionego w sklepie, według regulaminu, zatwierdzane kodem kierownika. Plan: także zwrot zamówienia internetowego w sklepie, rejestrowany w Aporcie; towar trafia do miejsca oceny | zwrot | AS-IS 00:51:53; OPIS w. 196 |
| Zgłoszenie sklepu do centrali | Plan: sprawa skierowana przez sklep do logistyki, jakości lub wsparcia IT, np. różnica w dostawie. Kierunek: sklep widzi, kto prowadzi sprawę i co ustalono. Nie jest sprawą klienta w CRM; system nie jest wskazany | zgłoszenie | OPIS w. 212, 220; DYR 00:47:42 |
| Reklamacja | Dziś: papierowy formularz, skan wysyłany e-mailem do centrali, odpowiedź na skrzynkę kierownika | — | AS-IS 00:49:44–00:51:14 |
| Sprawa | Plan: rejestr kontaktów i ustaleń z klientem w CRM. Kierunek: pracownik sklepu widzi, kto prowadzi sprawę i co ustalono | zgłoszenie (klienta, w CRM), numer sprawy | OPIS w. 192; DYR 00:38:52, 00:47:42; TO-BE 00:19:20 |

### Systemy i miary

| Termin | Znaczenie w tym kontekście | Synonimy i skróty | Źródło i miejsce |
|---|---|---|---|
| POS | System kasowy: sprzedaż fiskalna, ruchy towaru i ewidencja zapasu sklepu. Po audycie zapadnie decyzja o jego rozbudowie albo wymianie | kasa, system kasowy, kasa fiskalna | OPIS w. 48, 300, 309; AS-IS 00:59:30; DYR 00:43:18 |
| Aport | Plan: aplikacja WWW do pracy sklepów i współpracy z centralą (zadania, dostawy, kompletacja, zwroty, pulpit kierownika). Nie jest kasą, księgą ani rejestrem zapasu | — | OPIS w. 200–220 |
| Asystent w Aporcie | Plan: asystent AI dla pracowników. Wyszukuje wiedzę produktową i procedury, a w odpowiedzi podaje źródło i wersję treści | — | OPIS w. 224–226; DYR 00:49:13 |
| AsAI | Plan: asystent AI dla klientów w serwisie WWW, później w aplikacji. Nie rezerwuje towaru i nie składa zamówień | asystent klientów | OPIS w. 230–253; DYR 00:50:48 |
| OMS / usługa dostępności / PIM / CRM | Plan: OMS prowadzi zamówienia i ich statusy; usługa dostępności — dostępność, rezerwacje i alokacje; PIM — treści produktów; CRM — kontakty i sprawy klientów | — | OPIS w. 291–307 |
| Wynik zarządczy sklepu | Plan: wynik sklepu obejmujący też zamówienia internetowe z propozycji jego doradcy. Sprzedaż pozostaje rozliczona w kanale zakupu. Zasady ustalą controlling i sprzedaż internetowa | — | OPIS w. 153; DYR 00:26:30 |
| Wynik sklepu (dziś) | Dziś: utarg z paragonów i faktur w kasie. Z niego liczy się plan sprzedaży i premię sklepu | utarg, raport dobowy | AS-IS 00:17:10, 01:02:47 |
| Porównywalne sklepy | Sklepy działające co najmniej 13 miesięcy, porównywane pod względem sprzedaży netto w tych samych okresach | — | OPIS w. 335; DYR 00:09:04 |

## Rozbieżności i pytania

1. **„Rezerwacja”.** W planie to 15-minutowa blokada koszyka przed płatnością,
   która po płatności przechodzi w alokację [OPIS w. 133–135]. W wywiadach
   pracownicy tym samym słowem nazywają telefoniczne odłożenie towaru
   [AS-IS 00:25:01; TO-BE 00:10:45]. Dyrektorka mówi o „odłożeniu”
   [DYR 00:29:34]. *Propozycja:* odłożenie telefoniczne nazywać „odłożeniem”,
   a słowo „rezerwacja” stosować tylko w znaczeniu z OPIS. Pytanie: czy przyjąć
   takie nazewnictwo?
2. **Odłożenie a odbiór zamówienia.** Dyrektorka wprost je rozróżnia: odłożony
   towar klient kupuje w kasie, a zamówienie odbiera już opłacone [DYR 00:07:38].
   Pracownicy chcą, żeby odłożenia były widoczne w Aporcie jak rezerwacje
   [TO-BE 00:10:45]. Czy odłożenie ma stać się osobnym obiektem w systemie
   i w jakim: w usłudze dostępności, w POS czy w Aporcie? Decyzja nie zapadła
   [DYR 00:29:34].
3. **„Dostępność”** ma trzy znaczenia: dostępność internetowa liczona według
   wzoru [OPIS w. 125], miernik dostępności na półce [OPIS w. 341] i potoczny
   „stan na kasie” [AS-IS 00:18:16]. Pracownicy pytają, czy stan pokazuje towar
   „do wzięcia, czy już odłożony” [TO-BE 00:08:11]. Do ustalenia: którą
   dostępność ma pokazywać Aport przy sprawdzaniu innego sklepu?
4. **„Wariant”.** Pracownicy mówią „wariant smakowy” albo „gramatura”
   [AS-IS 00:04:43]. Wariant handlowy (SKU) obejmuje także wielkość opakowania
   [OPIS w. 91]. W źródłach nie ma sprzeczności, ale w rozmowie łatwo pomylić
   te znaczenia. W dokumentach używać nazwy „wariant handlowy (SKU)”.
5. **Identyfikacja klienta w sklepie.** OPIS przewiduje identyfikator, który
   nie daje dostępu do historii [w. 143]. Pracownicy wymieniają kod z aplikacji,
   numer telefonu [TO-BE 00:04:38] i kartę klienta [TO-BE 00:10:45] i chcą
   na ich podstawie sprawdzać ostatnie zakupy. Pytanie: jakie formy identyfikatora
   są planowane i czy pracownik sklepu ma widzieć historię zakupów klienta?
6. **Potwierdzenie odbioru.** Według OPIS jest to jednorazowy kod odbioru
   [w. 176]. Pracownicy mówią o „numerze z SMS-a albo kodzie w telefonie”
   [TO-BE 00:10:45]. Dyrektorka zaznacza, że sam numer zamówienia służy
   do odnalezienia sprawy, a uprawnienie trzeba sprawdzić [DYR 00:36:02, 00:52:17].
7. **Propozycja koszyka a zapis wyboru na koncie.** OPIS i dyrektorka mówią
   o propozycji koszyka [OPIS w. 153; DYR 00:25:40]. Doradczyni chce „zapisać karmę
   na koncie” klientki, kierownik chce, żeby klientka mogła „wejść w tę poradę”,
   a analityk podsumowuje to jako „poradę zapisaną w sklepie” [TO-BE 00:04:38].
   AsAI ma osobną „propozycję zestawu” [OPIS w. 248].
   Czy to ta sama rzecz? Od odpowiedzi zależy, co liczy się do wyniku
   zarządczego sklepu.
8. **„Zwrot”.** Dziś to słowo oznacza każdy zwrot przy kasie [AS-IS 00:51:53].
   Plan rozdziela anulowanie, odstąpienie, reklamację i zwrot środków [OPIS w. 194].
   W dokumentach TO-BE trzeba wskazywać, o który proces chodzi.
9. **„Zamówienie”.** W AS-IS to także zamówienie sklepowe do dostawy
   [AS-IS 00:43:32], a „zamówienie pod klienta” dziś nie istnieje [AS-IS 00:30:35].
   W TO-BE samo „zamówienie” oznacza zamówienie internetowe w OMS.
10. **Nieznane terminy z wywiadu TO-BE:** „Tropek” [TO-BE 00:04:38], „cena
    klubowa” [TO-BE 00:16:04], „karta klienta” i „stały rabat” dla klienta
    biznesowego [TO-BE 00:10:45]. Nie występują w OPIS ani w wywiadzie
    z dyrektorką.
11. **„Zgłoszenie”** ma trzy znaczenia: sprawa klienta w CRM, zgłoszenie sklepu
    do centrali i zgłoszenie rozbieżności stanu. W dokumentach pisać nazwę pełną.
12. **„Dostawa do sklepu”** oznacza zatowarowanie sklepu, a „dostawa paczki do
    sklepu” — realizację zamówienia klienta. Potoczne „odbiór w sklepie” dotyczy
    tylko zamówień: odbioru z zapasu sklepu i dostawy paczki do sklepu.

Pytania zebrano w
[[projects/pupilia/Outputs/pytania-do-interesariuszy|liście pytań do interesariuszy]]
projektu Aport (sprawy nazewnictwa: sekcja „Do decyzji w zespole projektu”);
odpowiedzi są zapisywane tam.
