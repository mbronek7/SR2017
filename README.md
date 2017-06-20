

### Słownik pojęć SR 2017

* [System Rozproszony](#system-rozproszony)
* [Proces](#proces)
* [Wykorzystanie wątków u klienta w celu polepszenia działania](#wykorzystanie-wątków-u-klienta-w-celu-polepszenia-działania)
* [Obliczenia w chmurze](#obliczenia-w-chmurze)
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

### System Rozproszony

 <p align="justify"> System rozproszony -- zestaw połączonych ze sobą niezależnych komputerów. Urzytkownik takiego systemu najczęściej nie jest w stanie stwierdzić czy system z którego aktualnie korzysta jest jedną zwartą logicznie całością, czy właśnie rozproszonymi modułami. Poszczególne komputery współdzielą swoje zasoby. Systemy rozproszone wyróżniają się : 
<ul>
<li>Spójnym i jednolitym interfejsem</li>
<li>Skalowalnością (łatwością rozszerzenia)</li>
<li>Sprawnością wykorzystywania zasobów</li>
<li>Dużą wydajnością</li>
<li>Odpornością na błędy</li>
<li>Przezroczystość</li>
</ul>
</p><br />
[17-05-14 mbr, wersja 1.0]
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
 <p align="justify">Idea stojąca za obliczeniami w chmurze opiera się na tym, by odciążyć komputery klienckie i przenieść obliczenia, oprogramowanie, a także część danych na serwery chmury. Sam termin można wyśledzić już w latach 90, ale jego spopularyzowanie przypisuje się korporacji Amazon, który zaczął świadczyć takie usługi w roku 2006.  Jedną z niezaprzeczalnych zalet chmury jest skalowalność, klient potrzebujący więcej mocy może wypożyczyć kolejne maszyny. Chmury dzielimy na 4 warstwy: sprzętu, infrastruktury, platformy i aplikacji. Na najniższej warstwie sprzętowej znajdują się podstawowe elementy, takie jak procesory, pamięć i dyski twarde. Na kolejnych poziomach pojawia się wirtualizacja i rośnie poziom abstrakcji. Warstwa infrastruktury przypomina warstwę sprzętową, ale jej zasoby są wirtualizowane. Warstwę platformy przyrównać można do systemu operacyjnego, oferuje ona programistom środowisko, na którym można łatwo testować i uruchamiać aplikacje. W ostatniej warstwie aplikacji można korzystać z programów przygotowanych przez dostawcę usług. Programy te są wykonywane na sprzęcie dostawcy. Warto zauważyć, że im większa warstwa, tym bardziej faktyczne maszyny stają się mniej widoczne dla klienta. Ten brak transparentności może przeszkadzać przy szacowaniu złożoności aplikacji. Pojawiają się też wątpliwości na temat bezpieczeństwa plików w chmurze i zagrożenia dla naszej prywatności. Dostęp do chmury uzyskać można przez różne interfejsy, począwszy od linii poleceń, skończywszy na aplikacji sieciowej. Istnieją różne modele dostępu do obliczeń w chmurze. Wyróżnić można IaaS, PaaS i SaaS. Pierwszy model pokrywa warstwę sprzętu i infrastruktury, drugi obejmuje warstwę platformy, a trzeci skupia się na warstwie aplikacji. Co ciekawe, chmury używane są także w branży rozrywkowej, co można zaobserwować na przykładzie takich serwisów jak  Nvidia GRID. <br /></p>
[24-03-08 Jakub ledwoń, wersja 0.5]<br />

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
</ul><br />
[20.06.2017 Wojciech Goska, wersja 1.0]
[20.06.2017 Wojciech Goska, wersja 1.1]<br />

