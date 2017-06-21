

### Słownik pojęć SR 2017

* [System rozproszony](#system-rozproszony)
* [Proces](#proces)
* [Wykorzystanie wątków u klienta w celu polepszenia działania](#wykorzystanie-wątków-u-klienta-w-celu-polepszenia-działania)
* [Obliczenia w chmurze](#obliczenia-w-chmurze)
* [BitTorrent](#bittorrent)
* [MD5](#md5)
* [Spójność FIFO](#spójność-FIFO)
* [Plotkowanie](#plotkowanie)
* [Elixir](#elixir)
* [DII](#dii)
* [OMA](#oma)
* [Corba](#corba)
* [NFS](#nfs)
* [Algorytm tyrana](#algorytm-tyrana)
* [Zwielokrotnianie](#zwielokrotnianie)
* [Rozproszona pamięć współdzielona](#rozproszona-pamięć-współdzielona)
* [Spójność ścisła](#spójność-ścisła)
* [Właściwości ACID](#właściwości-acid)
* [Przezroczystość](#przezroczystość)
* [Otwartość](#otwartość)
* [Maszyna wirtualna](#maszyna-wirtualna)
* [Algorytmy synchronizacji czasu](#algorytmy-synchronizacji-czasu)
* [Architektura klient-serwer](#architektura-klient-serwer)
* [Serwer iteracyjny, a współbieżny](#serwer-iteracyjny-a-współbieżny)
* [Serwer stanowy, a bezstanowy](#serwer-stanowy-a-bezstanowy)
* [Serwer obiektowy](#serwer-obiektowy)
* [Model TCP/IP](#model-tcp\ip)

### System rozproszony

 <p align="justify"> System rozproszony -- zestaw połączonych ze sobą niezależnych komputerów. Użytkownik takiego systemu najczęściej nie jest w stanie stwierdzić, czy system, z którego aktualnie korzysta, jest jedną zwartą logicznie i fizycznie całością, czy właśnie rozproszonymi modułami. Poszczególne komputery dzielą swoje zasoby. Systemy rozproszone wyróżniają się : 
<ul>
<li>spójnym i jednolitym interfejsem,</li>
<li>skalowalnością (łatwością rozszerzenia),</li>
<li>sprawnością wykorzystywania zasobów,</li>
<li>dużą wydajnością,</li>
<li>odpornością na błędy,</li>
<li>przezroczystością.</li>
</ul>
</p><br />
[17-05-14 mbr, wersja 1.0]
[17-06-20 mbr, wersja 1.1]
<br />

### Proces

 <p align="justify">Proces (ang. process) -- w informatyce pojęcie związane z systemami operacyjnymi. Proces jest programem w trakcie działania  i jako taki stanowi jednostkę pracy systemu operacyjnego. Kod programu jest statyczną częścią procesu. Dynamiczna część procesu jest reprezentowana przez stan sprzętowych rejestrów komputera, ze szczególnym uwzględnieniem licznika rozkazów. Podczas pracy proces może się rozgałęziać, tworząc  procesy potomne. Każdy proces potrzebuje zasobów, z których korzysta lub które zużywa. Do najważniejszych zasobów procesu należą pamięć operacyjna, czas procesora i pliki.<br /></p>
[17-03-08 mbr, wersja 1.0]<br />
[17-03-08 zpl, wersja 1.1]<br />


 
### Wykorzystanie wątków u klienta w celu polepszenia działania
 <p align="justify">Wątki wykorzystuje się w procesach w celu wykonywania wielu rzeczy jednocześnie. Wątek z definicji jest podstawową jednostką sterowania w procesie. Procesor może jednocześnie wykonywać tyle wątków, ile ma rdzeni. Procesor w każdej sekundzie wielokrotnie przełącza się między wykonywanymi wątkami. Dzięki czemu użytkownik ma wrażenie ciągłości wykonywania wszystkich aktualnie działających wątków. W systemach rozproszonych część przetwarzania może być wykonywana po stronie użytkownika. Wykorzystywanych w tym celu wątków nie należy mylić z <b> wątkami poziomu użytkownika</b> (w odróżnieniu od wątków jądrowych). Wątki działające <b>u użytkownika</b>, tj. po stronie aplikacji klienta, są stosowane w celu odciążenia serwera. Największą zaletą tego rozwiązania jest zmniejszenie kosztów związanych z wykonywaniem obliczeń przez serwer. Umożliwia to obsługiwanie przez serwer większej liczby użytkowników którzy mogą korzystać w tym samym czasie. Można przerzucić znaczną część obliczeń na maszynę klienta i w ten sposób unikać opóźnień w interakcji klient-serwer. Dobrym przykładem udanego użycia takiego rozwiązania są nowoczesne przeglądarki internetowe, które tworzą wątki, z których część jest aktywna jednocześnie przy czym chodzi tu o wątki działające po stronie klienta. Na przykład użytkownik, zamykający nowe okno od razu ujrzy efekt, lecz związany z tym proces (i jego wątki) jest stopniowo wygaszany w tle.<br /></p>
[17-03-21 mbr, wersja 1.0]<br />
[17-03-25 mbr, wersja 2.0]<br />
[17-03-30 zpl, wersja 2.1]<br />


### Obliczenia w chmurze
 <p align="justify">Pomysł obliczeń w chmurze opiera się na tym, by odciążyć komputery klientów i przenieść obliczenia, oprogramowanie, a także część danych na serwery chmury. Sam termin można napotkać już w latach 90. XX wieku, ale jego spopularyzowanie przypisuje się korporacji Amazon, która zaczęła świadczyć takie usługi w roku 2006.  Jedną z niezaprzeczalnych zalet chmury jest skalowalność, klient potrzebujący więcej mocy może wypożyczyć kolejne maszyny. Chmury dzielimy na 4 warstwy: sprzętu, infrastruktury, platformy i aplikacji. W najniższej warstwie sprzętowej znajdują się podstawowe elementy, takie jak procesory, pamięć operacyjna i dyski twarde. Na kolejnych poziomach pojawia się wirtualizacja i rośnie poziom abstrakcji. Warstwa infrastruktury przypomina warstwę sprzętową, ale jej zasoby są wirtualizowane. Warstwę platformy można porównać do systemu operacyjnego, udostępnia ona programistom środowisko, w którym można łatwo testować i uruchamiać aplikacje. W ostatniej warstwie aplikacji można korzystać z programów przygotowanych przez dostawcę usług. Programy te są wykonywane na sprzęcie dostawcy. Warto zauważyć, że im wyższa warstwa, tym bardziej mniej rzeczywiste maszyny stają się  widoczne dla klienta. Ten brak przezroczystości może przeszkadzać przy szacowaniu złożoności aplikacji. Pojawiają się też wątpliwości dotyczące bezpieczeństwa plików w chmurze i zagrożenia prywatności. Dostęp do chmury można uzyskać przez różne interfejsy, poczynając od poleceń teksotwych, a kończąc na interfejsie aplikacji sieciowej. Istnieją różne modele dostępu do obliczeń w chmurze. Wyróżnić można IaaS (Infrastructure as a Service), PaaS (Platform as a Service) i SaaS (Software as a Service). Pierwszy model obejmuje warstwę sprzętu i infrastruktury, drugi warstwę platformy, a trzeci skupia się na warstwie aplikacji. Co ciekawe, chmury są używane także w branży rozrywkowej, za przykład może służyć usługa Nvidia GRID. <br /></p>
[17-03-24 Jakub Ledwoń, wersja 0.5]<br />
[17-03-29, zpl, wersja 0.6] <br />

### BitTorrent 
 <p align="justify">BitTorrent jest zgodnym z P2P protokołem, służącym dystrybucji pików w Internecie. Fragmenty plików są przesyłane bezpośrednio pomiędzy użytkownikami, którzy mogą jednocześnie pobierać te części, których nie posiadają, jak i wysyłać te, które już wcześniej pobrali. Jest to stosunkowo nowy protokół, ponieważ jego pierwsza wersja została upubliczniona w 2001 roku. Początkowo wymagał istnienia dodatkowego serwera – trackera, na którym przechowywane były informacje o stanie i lokalizacji pików na komputerach klienckich, ale nowsze wersje protokołu dzięki technologiom DHT i PeX wyeliminowały ten obowiązek. Protokół wykorzystywany jest zarówno przez użytkowników prywatnych, którzy dzielą się rożnymi dobrami, jak i poprzez firmy, które odciążają w ten sposób swoje główne serwery, przekazując ciężar wysyłania plików na konsumentów. Protokół BitTorrent został zaimplementowany w wielu aplikacjach i jest powszechnie używany. <br /></p>
[17-06-21 Jakub Ledwoń, wersja 1.0]<br />

### MD5
 <p align="justify">MD5 to kryptograficzny algorytm skrótu używany głównie do weryfikacji plików. MD5 został opublikowany w 1992 jako następca algorytmu MD4. MD5 jest funkcją, która dla podanego ciągu danych generuje 128-bitowy skrót. Przeważnie zmiana paru bajtów pliku powoduje wygenerowanie całkowicie różnego skrótu, lecz algorytm jest podatny na kolizje i nie jest zalecane stosowanie go w sytuacjach, które wymagają wzmożonego bezpieczeństwa. Dzisiejsze komputery domowe potrafią wygenerować kolizję w ciągu ułamka sekundy. <br /></p>
[17-06-21 Jakub Ledwoń, wersja 1.0]<br />

### Spójność FIFO
 <p align="justify">Spójność FIFO (w źródłach angielskojęzycznych możemy też spotkać skrót PRAM) jest jednym z pierwszych opracowanych modeli spójności i cechuje się łatwością implementacji. W tym modelu dane do procesów mogą docierać prawie z dowolną kolejnością, z jednym tylko wyjątkiem. Dane z jednego procesu muszą dotrzeć do drugiego w takiej samej kolejności, w jakiej zostały zapisane w pierwszym. Oznacza to, że nieistotne jest, czy trzeci proces odczyta najpierw operacje z drugiego procesu, czy z pierwszego. <br /></p>
[17-06-21 Jakub Ledwoń, wersja 1.0]<br />

### Plotkowanie
 <p align="justify">Protokół plotkowania jest jednym ze sposobów wykorzystywanych przez systemy (w tym rozproszone) do komunikacji. Etymologia terminu jest w tym przypadku dość intuicyjna i ma swoje źródło w popularnym ludzkim zwyczaju. Zazwyczaj proces wybiera odbiorcę „plotki” losowo spośród listy pozostałych rozmownych procesów i przekazuje mu wybraną informację. Wszystkie plotkujące procesy co jakiś czas dzielą się nowymi informacjami, co skutkuje samoaktualizującą się bazą informacji. Ze względu na element losowości nie możemy jednak założyć niezawodności. Algorytmy oparte na tej idei wykorzystywane są na przykład w routingu, a także do zwalczania entropii. <br /></p>
[17-06-21 Jakub Ledwoń, wersja 1.0]<br />

### Elixir
 <p align="justify">Elixir jest jednym z obowiązujących w Polsce systemów rozliczeń międzybankowych, działającym od 1994 roku. W 2004 roku całkowicie wyparł system Sybir, który był oparty na fizycznej wymianie papierowych dokumentów. System Elixir jest wykorzystywany podczas większości przelewów detalicznych z racji na to, że banki przeważnie nie pobierają opłat za tego typu przelewy. Nie jest systemem typu rzeczywistego, każdego dnia roboczego obsługuje 3 sesje wyjścia i wejścia, których to konkretne godziny różnią się w zależności od banku. Przelew musi zosstać obłużony przez seje wyjścia banku źródłowego, a później przez sesję wejścia banku docelowego. Część banków wdrożyła też system Express Elixir, który realizuje przelew międzybankowy w ciągu kilku sekund. Transakcje wysokokwotowe są natomiast najczęściej obsługiwane przez SORBNET2 – system czasu rzeczywistego. <br /></p>
[17-06-21 Jakub Ledwoń, wersja 1.0]<br />


### DII
 <p align="justify"> DII (<i>ang.  Dynamic Invocation Interface</i>) -- to Interfejs Dynamicznych Wywołań, który jest częśćią implementacji OMA. Interfejsy obiektów dzielimy na znane w trakcie etapu kompliacji i dynamiczne. Interfejsy dynamiczne pozwalają klientom używać obiektów CORBA, których typy nie były znane w czasie kompilacji.</p><br />
 [17-05-14 mbr, wersja 1.0]<br />
 
### OMA
 <p align="justify"> OMA (<i>ang. Object Management Architecture</i>) -- architektura zarządzania obiektami definiuje obiektową bazę danych, której skłądowymi są obiekty, interfejsy i protokoły tworząca obiektową architekturę systemu rozproszonego. główną częścią OMA jest Corba.</p><br />
 [17-05-14 mbr, wersja 1.0]<br />
 
### Corba
 <p align="justify"> CORBA (<i>ang. Common Object Request Broker Architecture</i>) -- jest to system pozwalający na komunikacje pomiędzy modułami pracującymi w różnych architekturach systemowych. Obiekty moga też być zaimplementowane w róznych technologiach np.: Python i Java. Corba przypomina program napisany obiektowo. Każdy obiekt ma swój własny interfejs ,który jest interpretowany w czasie wykonywania, a współdzielone są metody.W szczególności system oparty na CORBA jest zbiorem obiektów, które oddzielają serwery od klientów przy pomocy dobrze określonego interfejsu programistycznego. Podsumowując Corba jest zbiorem specyfikacji, które określają standardowe metody dostępu do zdalnych obiektów i komunikacji pomiędzy nimi, niezależnie od systemu operacyjnego, języka programowania oraz położenia w sieci.</p><br />
 [17-05-14 mbr, wersja 1.0]<br />
 
### NFS
  <p align="justify"> NFS (<i>ang. Network File System</i>) -- protokół zdalnego udostepniania plików. Pozwala użytkownikowi współdzielic swoje pliki poprzez sieć internetową, wiele komputerów uzyskuje dostęp do informacji zawartych na jednej stacji roboczej. Jedną z korzyści jest możliwość posiadania przez kilka komputerów wspólnego katalogu z aktualizacjami oprogramowania, dzięki czemu nie ma potrzeby pobierania ich na każdym z komputerów oddzielnie. Gdy użytkownik łączy się z serwerem przez NFS jądro wysyła wywołanie RPC do demona NFS na serwerze. To wywołanie przekazuje nazwę pliku i ID użytkownika oraz jego grupy. Potem następuje ustalania praw dostępu użytkownikowi, poprzez porównanie informacji o ID użytkownika i jego grupy, które są zawarte na serwerze. Pozwala to uniemożliwić nieuprawnionym użytkownikom odczytywanie lub modyfikowanie plików.</p><br />
 [17-05-14 mbr, wersja 1.0]<br />

### Algorytm tyrana
<p align="justify"> Algorytm tyrana (<i>ang. bully algorithm</i>) jest to tak zwany algorytm elekcji (<i>ang. election algorithm</i>) i służy do wyboru koordynatora, czyli procesu nadzorującego inne procesy. 

Zasada działania algorytmu:

Gdy bieżący koordynator przestaje odpowiadać na żądania innych procesów, proces <i>p</i> wysyła komunikat do wszystkich procesów z wyższym priorytetem. Jeśli nie dostanie odpowiedzi zostaje koordynatorem. W przeciwnym przypadku odpowiadający proces, jeśli już tego nie robił, przejmuje zadanie ustalenia koordynatora i cykl się powtarza. Algorytm wyłania jeden aktywny proces, który zostaje koordynatorem i wysyła do pozostałych procesów informacje o tym.<br /></p>
[13.06.2017 Mateusz Sroka, wersja 1.0]<br />

### Zwielokrotnianie
<p align="justify"> Zwielokrotnianie (<i>ang. replication</i>) to mechanizm stosowany w systemach rozproszonych, polegający na utrzymywaniu wielu kopii tych samych danych na niezależnych serwerach, w celu zwiększenia dostępności i efektywności przetwarzania tych danych. Jednym z głównych problemów generowanych przez to podejście jest problem spójności danych. Użytkownik wprowadza zmiany tylko na jednej kopi, jednak wszystkie inne również powinny zostać szybko zaktualizowane. By rozwiązać te problemy stworzono wiele modeli spójności danych. <br /></p>
[13.06.2017 Mateusz Sroka, wersja 1.0]<br />

### Rozproszona pamięć współdzielona
<p align="justify"> Rozproszona pamięć współdzielona (<i>ang. distributed shared memory, DSM</i>) to architektura pamięci, w której wiele odseparowanych jednostek pamięci może być adresowanych jako jedna logiczna przestrzeń adresowa. Jej głównym celem jest zapewnienie w jak najbardziej przezroczysty sposób dostępu do wspólnych danych przez procesy na różnych procesorach. DSM wymaga zastosowania metod synchronizacji takich jak semafory. Komunikacja przy takiej pamięci odbywa się poprzez przekazywanie komunikatów pomiędzy procesami, przez co wydajność dostępu do takiej pamięci jest gorsza niż w przypadku dostępu bezpośredniego. Dwa główne sposoby wspierania DSM to wsparcie systemowe, gdzie zarządzaniem dostępem do pamięci zajmuje się bezpośrednio jądro oraz wsparcie biblioteczne, gdzie procesy uzyskują dostęp za pomocą wywołań bibliotecznych. <br /></p>
[13.06.2017 Mateusz Sroka, wersja 1.0]<br />

### Spójność ścisła
<p align="justify"> Spójność ścisła (<i>ang. strict consistency</i>) - model spójności polegający na tym, że każda próba odczytania jakichś danych zwraca wartość ostatniego zapisu do tych danych. W praktyce jednak taka sytuacja jest bardzo trudna lub niemożliwa do uzyskania. Jedną z implementacji tego modelu jest centralny serwer przetwarzający wszystkie komunikaty. Takie rozwiązania są jednak wysoce nieefektywne, dlatego zwykle stosuje się inne, mniej restrykcyjne, modele. <br /></p>
[13.06.2017 Mateusz Sroka, wersja 1.0]<br />

### Właściwości ACID
<p align="justify"> Właściwości ACID to podstawowe własności transakcji, czyli operacji na współdzielonych danych. Są to kolejno: atomowość (<i>ang. atomicity</i>), spójność (<i>ang. consistency</i>), izolacja (<i>ang. isolation</i>), trwałość (<i>ang. durability</i>).

Atomowość czyli traktowanie transakcji jako niepodzielnej części, która musi być wykonana w całości i bez przerwań, od początku do końca. Z zewnątrz transakcja wygląda jak pojedyncza instrukcja, a wszystkie jej pośrednie działania są ukryte przed użytkownikiem.

Spójność zapewnia, że dane spełniające zdefiniowane własności przed transakcją będą je spełniać także po niej.

Izolacja zapewnia, że wynik wykonujących się współbieżnie transakcji będzie taki sam, jak gdyby te wykonywały się sekwencyjnie - jedna po drugiej. W zależności od metod kontroli współbieżności, skutki niedokończonej transakcji mogą nie być widoczne dla innych transakcji.

Trwałość oznacza, że w momencie pomyślnego ukończenia transakcji nie da się cofnąć jej zmian i zostają one zachowane nawet w przypadku wystąpienia awarii lub błędów. <br /></p>
[13.06.2017 Mateusz Sroka, wersja 1.0]<br />

### Przezroczystość
<p align="justify"> Przezroczystość (<i>ang. transparency</i>), w systemach rozproszonych, możemy rozumieć jako dbanie o wygodę ich użytkownika przez ukrywanie tych aspektów implementacji systemów, które nie są użytkownikowi potrzebne do osiągnięcia określonego celu, tak aby miał wrażenie że wszystko dzieje się w jednolitym systemie, na komputerze, z którego użytkownik w danej chwili korzysta.<br />
Wyróżniamy osiem głównych rodzajów przezroczystości:
<ul>
<li>Przezroczystość dostępu</li>
<li>Przezroczystość położenia</li>
<li>Przezroczystość wędrówki</li>
<li>Przezroczystość zwielokrotniania</li>
<li>Przezroczystość skalowania</li>
<li>Przezroczystość współbieżności</li>
<li>Przezroczystość trwałości</li>
<li>Przezroczystość awarii</li>
</ul><br /></p>
[20.06.2017 Wojciech Goska, wersja 1.0]<br />
[20.06.2017 Wojciech Goska, wersja 1.1]<br />

### Otwartość
<p align="justify"> Otwartość (<i>ang. openness</i>), w systemach rozproszonych, charakteryzuje system, oferujący elementy, które z łatwością można wykorzystać czy zintegrować z zupełnie innym, nowym systemem, dzięki czemu jest on podatny na rozszerzenia oraz możliwość rozbudowy zarówno pod względem sprzętowym, jak i oprogramowania. Otwartość umożliwia nam dołączyć do naszego systemu kolejne urządzenie, bez martwienia się o jego oprogramowanie, ponieważ warstwa pośrednia zapewnia nam protokoły i interfejsy potrzebne do jego obsłużenia.<br /></p>
[20.06.2017 Wojciech Goska, wersja 1.0]<br />

### Maszyna wirtualna
<p align="justify"> Maszyna wirtualna (<i>ang. virtual machine</i>) to ogólna nazwa dla programów, które tworzą środowisko uruchomieniowe dla innych programów. Maszyna wirtualna obsługuje wszystkie odwołania uruchomionej aplikacji, w ten
sposób "udając" że jest ona wykonywana na rzeczywistym sprzęcie. W maszynie wirtualnej możemy uruchomić program, system czy nawet kolejną maszynę wirtualną. Niestety, wszystko to działa kosztem zwiększonego wykorzystania procesora i pamięci
operacyjnej, ponieważ poza uruchamianymi programami, sama maszyna wirtualna również korzysta z tychże zasobów.<br /></p>
[20.06.2017 Wojciech Goska, wersja 1.0]<br />

### Algorytmy synchronizacji czasu

 <p align="justify">Wybrane algorytmy synchronizacji czasu:
 <ol>
 <li><b>Algorytm Cristiana</b></li>
 <ul><li>Algorytm przeznaczony głównie dla systemów, w których jedna maszyna jest serwerem czasu, a reszta maszyn powinna być z nim zsynchronizowana</li>
 <li>Okresowo każda maszyna wysyła komunikat do serwera czasu, pytając o bieżący czas. Serwer odsyła, jak szybko może wiadomość ze swoim aktualnym czasem</li></ul>
 <li><b>Algorytm z Berkeley</b></li><ul><li>Serwer czasu jest aktywny. Serwer czasu okresowo
 wypytuje każdą maszynę, aby poznać jej czas</li><li>Na podstawie odpowiedzi serwer wylicza średni czas i
wysyła komunikaty do innych maszyn, aby odpowiednio
zmieniły swój czas lub zwolniły zegar do momentu, aż
zostanie osiągnięta właściwa jego wartość</li></ul>
<li><b>Algorytm uśredniania</b></li><ul><li>Każda maszyna rozsyła co pewien okres informację o
swoim czasie. Rozpoczyna jednocześnie zbierać
informacje od innych maszyn. Gdy zbierze wszystkie,
oblicza na ich podstawie nowy czas np. stosując
uśrednianie</li><li> Algorytm jest rozproszony</li><li>Algorytm uwzględnia czasy przesyłania komunikatów</li><li>Algorytm odrzuca skrajne wartości</li></ul>
 </ol></p><br/>[Szymon Kopa 1.0]</br>
 
 ### Architektura klient-serwer

 <p align="justify">
 
 ### Serwer iteracyjny, a współbieżny

 <p align="justify">
 <ul>
 <li><b>Serwer iteracyjny</b> samodzielnie obsługuje zlecenia klientów zwracając im ewentualnie wyniki. Innymi słowy
serwer zmuszony jest do obsługi zleceń jedno po drugim, przy czym zanim rozpocznie kolejne zadanie musi
zakończyć wykonywanie poprzedniego</li>
<li><b>Serwer współbieżny</b> pozbawiony jest niedogodności powodującej, że każde kolejne żądanie musi oczekiwać
w kolejce do momentu gdy zostaną obsłużone poprzednie. W tym przypadku serwer po odebraniu zlecenia
od klienta przekazuje wykonanie zlecenia innemu wątkowi lub procesowi. Po tym jak przekaże zlecenie
może natychmiast przystąpić do obsługi innych zleceń. Z architekturą serwerów współbieżnych wiąże się
m.in. kwestia miejsca kontaktowego z serwerem. Miejscem takim jest zazwyczaj pewien dobrze znany
wszystkim klientom port (tzw. punkt końcowy – ang. <i>endpoint</i>). Po skontaktowaniu się klienta przez taki port
z serwerem klient otrzymuje np. nowy port do komunikacji z procesem obsługującym jego zlecenie, tym
samym zwalnia punkt końcowy na rzecz nowych klientów serwera.</li>
 </ul>
 </p>
<br/>[Szymon Kopa 1.0]<br/>

### Serwer stanowy, a bezstanowy

 <p align="justify">
 <ul>
 <li><b>Serwer bezstanowy</b> charakteryzuje się głównie tym, że nie przechowuje danych o swoich klientach.
Również zmiana stanu samego serwera niekoniecznie wpływa na zmianę stanu jego klientów. Przykładem
może być tu prosty serwer plików lub serwer siec</li>
<li>Przeciwieństwem serwera bezstanowego jest <b>serwer pełnostanowy</b>, który przechowuje informacje o swoich
klientach np. w celu odesłania im w przyszłości jakichś danych. Również tutaj za przykład może posłużyć
rozproszony systemem plików, tym razem jednak taki, który przechowuje informacje o klientach w celu
zapewnienia im w przyszłości szybszego dostępu do danych.
Zasadniczą niedogodnością w przypadku serwerów pełnostanowych są awarie, które powodują utratę stanu
i wymuszają konieczność jego odtwarzania.</li>
 </ul>
  </p>
<br/>[Szymon Kopa 1.0]<br/>

### Serwer obiektowy

 <p align="justify">
 <b>Serwer obiektowy</b> (ang. <i>object server</i>) jest środowiskiem do
przechowywania i zarządzania obiektami, także tymi rozproszonymi. Każdy
obiekt posiada pewien kod, w postaci zaimplementowanych metod, oraz stan w
postaci danych. Sposób zarządzania tymi obiema częściami zależy w dużej
mierze od serwera obiektowego, którego implementacja określa np. to ile wątków
ma działać w ramach jednego obiektu, czy dla każdego wywołania ma być
używany osobny wątek, czy obiekty powinny mieć dostęp do wspólnych
segmentów pamięci itp.
 </p>
<br/>[Szymon Kopa 1.0]<br/>

### Model TCP/IP

<p align="justify">Model TCP/IP (<i>ang. Transmission Control Protocol/ Internet Protocol</i>)- model struktury protokołów komunikacyjnych, zakładający podział warstwy komunikacyjnej na cztery kolejne, współpracujące warstwy tj. : warstwa aplikacji, warstwa transportowa, warstwa Internetu oraz warstwa dostępu do sieci. Model ten został stworzony przez amerykańską agencję rządową DARPA (<i>ang. Defence Advanced Research Projects Agency</i>) w latach 70. i pierwotnie miał pomagać w tworzeniu odpornych na ataki sieci komputerowych.	<br /><br />
Więcej informacji o protokołach TCP, IP oraz o wielu innych można znaleźć <a href="http://www.networksorcery.com/">tutaj</a><br /></p>
[21.06.2017 Wojciech Goska, wersja 1.0]<br />
