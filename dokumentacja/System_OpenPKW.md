#OpenPKW

**"Projekt ma za zadanie stworzyć w pełni działający system do obsługi głosowania w ramach prawnych Rzeczpospolitej Polskiej. Projekt zakłada opracowanie, stworzenie i udostępnienie projektu na licencjach otwartych."**

**Projekt wspierany jest przez prawników, którzy dbają o zgodność systemu z obowiązującymi aktami prawnymi regulującymi system wyborczy w Polsce, wolontariuszy, hakerów i programistów, mających za zadanie postawienie systemu i zaimplementowanie go na dostępnych PKW systemach oraz przekazanie systemu do przetestowania organom bezpieczeństwa i wreszcie wszelkich ludzi, mających styczność z procedurami demokratycznymi, którzy projekt konsultują.**

Cytaty z "Deklaracji założycielskiej OpenPKW".


# Założenie podstawowe

- cały system **MUSI** być zgodny z odpowiednimi przepisami [**polskiego prawa wyborczego**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/prawo_wyborcze.md), a szczególnie:
  * Kodeks Wyborczy  
  * Inne ustawy / rozporządzenia dotyczące procedur wyborczych i "okołowyborczych"  
  * Aktualne Uchwały PKW.  

- Cały system **MUSI** wytrzymać ruch generowany przez wszystkie organy i instytucje wyborcze zaangażowane w daną akcję wyborczą. W tym - **najważniejsze** - generowany przez Obwodowe Komisje Wyborcze w noc wyborczą. 
- Ważną rzeczą wydaje się więc obliczenie pożądanych mocy obliczeniowych, przepustowości łączy internetowych, dostępu do baz danych itp. 
- Skalowalność systemu. 
- Obsługa wielu różnych akcji wyborczych w tym samym czasie. 
- Wymagane co najmniej dwa, główne i zapasowe centra zbierania danych.  
  - wymagana możliwość przełączania pomiędzy centrami zbierania danych.
  - wymagana możliwość rozbudowy centrum zbierania danych w trakcie akcji wyborczej (nocy wyborczej) bez utraty danych.
[**Przykładowe liczby wyborcze.**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Wybory_statystyka.md)  

Na podstawie analizy prawa wyborczego oraz materiałów źródłowych z ogłoszonych przez PKW [**przetargów**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Przetargi_PKW_2013_1014.md) na "informatyzację wyborów" cały system OpenPKW powinien składać się z 2 głównych modułów/działów/zadań:

# A. System Wyborczy OpenPKW.
(system centralny)  
# B. Kalkulator wyborczy.
(system lokalny)

oraz:  
dodatkowych projektów systemów, programów i aplikacji powstających (na razie - być może w przyszłości po odpowiednich zmianach w prawie wejdą w skład SW) obok Systemu Wyborczego OpenPKW a mianowicie:

**C. Programy mobilne.**  
Ten moduł tworzony jest nie do końca w zgodzie z przepisami prawa wyborczego a wykorzystywany może być przez różnorodne organizacje do sprawdzania poprawności (kontroli) wyborów w tym z możliwością archiwizacji zdjęć protokołów. Również instystucje i organizacje (np. lokalne Komitety Wyborcze, partie polityczne, organizacje PR, media itp.) mogą wykorzystać to oprogramowanie do szybkiego przekazania części danych z protokołów koisji wyborczych, potrzebnych do nieoficjalnego obliczenia wyników wyborów.

**D. e-Wybory.** - Moduł na razie wyłącznie do rozważań analitycznych oraz luźnych dyskusji. Może ostatecznie coś z tego wyrośnie a PKW pójdzie po rozum do głowy.  
 * Gosowanie nad budżetami obywatelskimi - nowe zadanie dla OpenPKW. [**Gosowania obywatelskie**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Modul_D_OpenPKW.md)  


**Dalszy, szczegółowy podział wynika wyłącznie z potrzeb państwowych organów wyborczych wszystkich szczebli i rodzajów oraz z funkcjonalności oprogramowania i baz danych wykorzystywanych w procesie przygotowania i przeprowadzenia wyborów oraz agregacji i ogłoszenia wyników wyborów.**

Do głównych zadań przedstawionych wyżej modułów należy:

# Ad. A.  
* A.1. zbieranie i przetwarzanie danych przed wyborczych zgodnie z przedstawionym graficznie (draw.io) [**procesem**] 
(https://www.draw.io/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fopenpkw%2Fopenpkw%2Fmaster%2Fdokumentacja%2Fprocesy%2Fprzed_wyborami.xml).
  * A.1.1. ułatwienie podziału kraju na okręgi wyborcze
  * A.1.2. wspomaganie podziału gmin na obwody wyborcze / podział (gminnych) obwodów wyborczych na okręgi wyborcze
  * A.1.3. wspomaganie powołania komisji wyborczych ([**obwodowych / terenowych / okręgowych (rejonowych**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Struktura_komisji_wyborczych.md))  
  * A.1.4. wspomaganie tworzenia i ułatwienie rejestracji komitetów wyborczych (komitet wyborczy wyborców; komitet wyborczy partii politycznej; komitet wyborczy koalicji partii politycznych)
  * A.1.5. wspomaganie zgłaszania oraz rejestracji kandydatów
  * A.1.6. wykorzystanie Systemu Rejestrów Państwowych w pracach przygotowawczych przed dniem wyborów w tym pomoc w tworzeniu [**spis wyborców**] (http://info.pkw.gov.pl/spis-wyborcow-pe/spis-wyborcow.html) uprawnionych do głosowania ([**rejestr wyborców**] (http://info.pkw.gov.pl/rejestr-wyborcow-pe/rejestr-wyborcow.html) / [**stałe zamieszkiwanie**] (http://info.pkw.gov.pl/stale-zamieszkiwanie-pe/stale-zamieszkanie.html) / PESEL / TERYT itp.)
  * A.1.7. generowanie i aktualizacja plików definicyjnych ([**pliki KLK**] (https://github.com/openpkw/openpkw/blob/master/pliki%20klk/README.md) oraz JSON) na podstawie [**meldunków wyborczych**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Slownik%20pojec.md) (przedwyborczych) z gmin
  * A.1.8. stworzenie wzoru karty wyborczej na podstawie uchwały PKW oraz danych o zarejestrowanych kandydatach (listach kandydatów) i komitetach wyborczych
  * A.1.9. stworzenie bazy danych (wzorów) dokumentów wyborczych.

* A.2. odebranie danych w noc wyborczą z komisji obwodowych, przetworzenie i przygotowanie do pobrania przez komisje wyborcze wyższego rzędu, przyjęcie danych w komisji wyższego rzędu, przetworzenie i przygotowanie danych dla PKW.
  * A.2.1. Pomoc w pracach: Komisji Terenowej, Rejonowej, Okręgowej które: 
    * A.2.1.1. kontrolują spływ protokołów z Obwodów,
    * A.2.1.2. wczytują z zewnętrznych nośników protokół Obwodowy do systemu (o ile zachodzi taka potrzeba)
    * A.2.1.3. walidują i zatwierdzają poprawność protokołów lub odrzucają protokół i kierują go do poprawek
    * A.2.1.4. wspomaganie obliczania i generowania protokołów na podstawie danych z Obwodowych Komisji.
    * A.2.1.5. Pomoc w ogłoszeniu wyników wyborów w gminie, powiecie, województwie, Okręgu
    * A.2.1.6. Przygotowanie Komisarzowi Wyborczemu Obwieszczenie o zbiorczych wynikach wyborów.
  * A.2.2. Pomoc w pracach Państwowa Komisja Wyborcza, która:
    * A.2.2.1. obserwuje spływ protokołów z Obwodów
    * A.2.2.2. kontroluje spływ protokołów z Terenowych, Rejonowych, Okręgowych Komisji Wyborczych
    * A.2.2.3. wczytuje z zewnętrznych nośników protokół Okręgowy do systemu (o ile zachodzi taka potrzeba)
    * A.2.2.4. waliduje i zatwierdza poprawność protokołów lub odrzuca protokół i kieruje do poprawek
    * A.2.2.5. oblicza i generuje protokół zbiorczy na podstawie protokołów Okręgowych Komisji.
    * A.2.2.6  ogłasza wyniki zbiorcze na terenie całego kraju.   

* A.3. Opracowanie i uruchomienie stałej/aktualnej wizualizacji bieżącej akcji wyborczej
   * A.3.1.  przyjęcie, agregacja i aktualizacja frekwencji z "godzin sprawozdawczych"  

* A.4. Zapewnienie stałego dostępu do danych archiwalnych (gromadzących dane z zakończonych akcji wyborczych i ich wizualizacje). Struktura bazy [**archiwalnej PKW**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/bazaKBW.md)
   * A.4.1. Stwworzenie serwera archiwizacji plików binarnych (obrazy oryginałów (podpisanych i wywieszonych) protokołów oraz obrazów ich korekt, skany dokumentów, itp. itd.)

Podział zadania A na [**moduły programistyczne**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Modul_A_OpenPKW.md).

[**Diagram**] (https://www.draw.io/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fopenpkw%2Fopenpkw%2Fmaster%2Fdokumentacja%2Fprocesy%2FSW_OpenPKW.xml) przedstawiający pożądaną strukturę całego "Systemu Wyborczego OpenPKW".  
W pliku [**README.md**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/README.md) w katalogu Dokumentacja jest dokłdny i aktualizowany na bieżąco spis wszystkich plików dotyczących dokumentacji oraz wszystkich gotowych diagramów dla poszczególnych moduów SW OpenPKW.

# Ad. B.

Komisja Obwodowa po zamknieciu lokalu o godz. 21:00 ręcznie wypełnia brudnopis protokołu zgodnie z przedstawionym graficznie (draw.io) [**procesem A - przed otwarciem urny**] 
(https://www.draw.io/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fopenpkw%2Fopenpkw%2Fmaster%2Fdokumentacja%2Fprocesy%2FObwodowa_komisja_A.xml) 
oraz [**procesem B po otwarciu urny**] (https://www.draw.io/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fopenpkw%2Fopenpkw%2Fmaster%2Fdokumentacja%2Fprocesy%2FObwodowa_komisja_B.xml) a następnie korzysta z:

* B.1. program do instalacji lokalnej (np. maszyny bez dostępu do internetu itp.)

* B.2. strona HTML (rozbudowany obecny prototyp kalkulatora w html) frontend?  

oba punkty zgodne z przedstawionym graficznie (draw.io) [**procesem**] (https://www.draw.io/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fopenpkw%2Fopenpkw%2Fmaster%2Fdokumentacja%2Fprocesy%2FObwodowa%2520komisja%2520wyborcza.xml)  

Podział zadania B na [**moduły programistyczne**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Modul_B_OpenPKW.md).

# Ad. B.1. 

* B.1.1. oprogramowanie dla localhost zgodne z [**propozycją funkcjonalności**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/oper_kalkulator.md)
    * B.1.1.1. pobieranie plików *.klk [**przykład plików**] (https://github.com/openpkw/openpkw/tree/master/pliki%20klk)
    * B.1.1.2. generowanie/pobieranie certyfikatów, loginów, haseł, kodów jednorazowych.
    * B.1.1.3. wpisanie danych do formularza / walidacja poprawności - walidacja [**prezydent2015**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/walidacja_prezydent_2015.md) ; walidacje [**dotychczasowe**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/walidacja_podstawy.md)
    * B.1.1.4. drukowanie "zestawień błędów" / poprawianie protokołu ([**PKW 09.03.2015 pkt.9.2.**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/zmiana_filozofii_PKW.md))
    * B.1.1.5. wysłanie poprawnego protokołu / zapisanie na zewnętrznych nośnikach
    * B.1.1.6. wydruk protokołów zgodnych z wzorami z Uchwał PKW - protokoły prezydent 2015: [**Obwodowy**] (http://pkw.gov.pl/g2/oryginal/2015_01/6d4a07c19783328b29a9e28e7be64ba3.pdf) ; [**Okręgowy**] (http://pkw.gov.pl/g2/oryginal/2015_01/0451db43c39dee8e139fd75615fe1af5.pdf) ; [**PKW**] (http://pkw.gov.pl/g2/oryginal/2015_01/b4303675cc97bcc62959ee934c899a50.pdf).
    * B.1.1.7. rozwiązanie problemu "zwartości" wydrukowanego protokołu 
      * B.1.1.7.1. barkod drukowany na dole każdej  strony - taki sam w całym wydruku [**przykład**] (https://op.openpkw.pl/attachments/6/barkod_przyklad.jpg)
      * B.1.1.7.2. QRkod - przyszłościowa [**propozycja**] (https://github.com/adamkowalewski/OtwartaPlatformaWyborcza/blob/master/brainstorming.md) na razie niezgodna z PKW.
      * B.1.1.7.3. opracowanie i wdrożenie modułu generowania kodów jednorazowych - pierwsza informacja pojawia się w Uchwale PKW z 9 marca 2015 patrz [**PKW 09.03.2015 pkt.4.**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/zmiana_filozofii_PKW.md)
    * B.1.1.8. wysyłka danych frekwencji wyborczej w godzinach sprawozdawczych [**Moduł F.1**] (https://www.draw.io/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fopenpkw%2Fopenpkw%2Fmaster%2Fdokumentacja%2Fprocesy%2FSW_OpenPKW_F1.xml)

# Ad. B.2.
Wszystkie funkcjonalności zgodne z podpunktami z A.1. ale wykonypane "poprzez" dostęp do dedykowanej strony internetowej.

# Ad.C.
Oprogramowanie to **NIE** będzie w całości zgodne z wytycznymi PKW.

Podział zadania C na [**moduły programistyczne**] (https://github.com/openpkw/openpkw/blob/master/dokumentacja/Modul_C_OpenPKW.md).

* C.1. aplikacja mobilna (co najmniej Android i IOS) umożliwiający szybkie przekazanie cześci danych liczbowych z protokołu. (draw.io) [**przykład**] (https://www.draw.io/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fadamkowalewski%2FOtwartaPlatformaWyborcza%2Fmaster%2Fpaper%2520browser%2FOPW_client.xml)  
    * B.1.1. implementacja możliwości przesłania danych SMS ze starszych modeli telefonów.
* C.2. aplikacja mobilna do dodatkowej weryfikacji danych liczbowych przekazanych z protokołów w postaci zdjęć samych protokołów (Rafał Reguła).  
* C.3. oprogramowanie serwerowe 
    * przetworzenie danych, ich agregacja i udostępnienie danych zbiorczych/wizualizacja.
    * archiwizacja danych przeszłych akcji wyborczych.

# Ad. D.
Moduł wymaga wstępne analizy strukturalnej, prawnej, organizacyjnej i każdej innej. Trzeba się zastanowić nad prawdopodobnymi beneficjentami takich systemów. Problemy PR i sposoby przekonania PKW.

D.1. - elektroniczne systemy automatycznego zliczania głosów z kart wyborczych.

D.2. - internetowe systemy głosowania.
