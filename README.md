

### Słownik pojęć SR 2017

* [Proces](#proces)
* [Wykorzystanie wątków u klienta w celu polepszenia działania](#wykorzystanie-wątków-u-klienta-w-celu-polepszenia-działania)
* [Obliczenia w chmurze](#obliczenia-w-chmurze)


### Proces

* Proces (ang. process) -- w informatyce pojęcie związane z systemami operacyjnymi. Proces jest programem w trakcie działania  i jako taki stanowi jednostkę pracy systemu operacyjnego. Kod programu jest statyczną częścią procesu. Dynamiczna część procesu jest reprezentowana przez stan sprzętowych rejestrów komputera, ze szczególnym uwzględnieniem licznika rozkazów. Podczas pracy proces może się rozgałęziać, tworząc  procesy potomne. Każdy proces potrzebuje zasobów, z których korzysta lub które zużywa. Do najważniejszych zasobów procesu należą pamięć operacyjna, czas procesora i pliki.<br />
[17-03-08 Michał Bronikowski, wersja 1.0]<br />
[17-03-08 zpl, wersja 1.1]<br />



### Wykorzystanie wątków u klienta w celu polepszenia działania
* Wątki wykorzystuje się w celu wykonywania wielu rzeczy jednocześnie. Wątek z definicji jest podstawową jednostką wykorzystywaną przez procesor. Procesor w jednej chwili może wykonywać tyle wątków ile ma rdzeni. Procesor  w ciągu każdej sekundy przełącza sie pomiędzy uruchomionymi wątkami, dzięki temu użytkownik ma wrażenie, ciągłości wykonywania wszytkich włączonych aktualnie procesów. Wyodrębniamy też wątki poziomu użytkownika. Wykorzystuje je się w celu przeniesienia części operacji na maszynę użytkownika. Największą zaletą tego rozwiązania jest zmniejszenie kosztów związanych z wykonywaniem obliczeń przez nasz serwer, również wzrasta maksymalna ilość użytkownikow, którzy mogą korzystać z naszej aplikacji w tym samym czasie. Mozna przeżucić wszystkie obliczenia na maszyne klienta i w ten sposób unikniemy opóźnień w interakcji klient-serwer, ponieważ dla serwera obliczenia nie będą obciążeniem. Dobrym przykładem użycia takiego rozwiązania z powodzeniem są nowoczesne przeglądarki internetowe, które tworzą setki wątków, z których dziesiątki są aktywne jednocześnie i te związane z obliczeniami wykorzytywane są po stronie klienta. Użytkownik zamykając nowe okno od razu ujrzy efekt a sam proces jest wygaszany w tle.<br />
[21-03-08 Michał Bronikowski, wersja 1.0]<br />
[21-03-08 Michał Bronikowski, wersja 1.1]<br />
[21-03-08 Michał Bronikowski, wersja 2.0]<br />



### Obliczenia w chmurze
* Idea stojąca za obliczeniami w chmurze opiera się na tym, by odciążyć komputery klienckie i przenieść obliczenia, oprogramowanie, a także część danych na serwery chmury. Sam termin można wyśledzić już w latach 90, ale jego spopularyzowanie przypisuje się korporacji Amazon, który zaczął świadczyć takie usługi w roku 2006.  Jedną z niezaprzeczalnych zalet chmury jest skalowalność, klient potrzebujący więcej mocy może wypożyczyć kolejne maszyny. Chmury dzielimy na 4 warstwy: sprzętu, infrastruktury, platformy i aplikacji. Na najniższej warstwie sprzętowej znajdują się podstawowe elementy, takie jak procesory, pamięć i dyski twarde. Na kolejnych poziomach pojawia się wirtualizacja i rośnie poziom abstrakcji. Warstwa infrastruktury przypomina warstwę sprzętową, ale jej zasoby są wirtualizowane. Warstwę platformy przyrównać można do systemu operacyjnego, oferuje ona programistom środowisko, na którym można łatwo testować i uruchamiać aplikacje. W ostatniej warstwie aplikacji można korzystać z programów przygotowanych przez dostawcę usług. Programy te są wykonywane na sprzęcie dostawcy. Warto zauważyć, że im większa warstwa, tym bardziej faktyczne maszyny stają się mniej widoczne dla klienta. Ten brak transparentności może przeszkadzać przy szacowaniu złożoności aplikacji. Pojawiają się też wątpliwości na temat bezpieczeństwa plików w chmurze i zagrożenia dla naszej prywatności. Dostęp do chmury uzyskać można przez różne interfejsy, począwszy od linii poleceń, skończywszy na aplikacji sieciowej. Istnieją różne modele dostępu do obliczeń w chmurze. Wyróżnić można IaaS, PaaS i SaaS. Pierwszy model pokrywa warstwę sprzętu i infrastruktury, drugi obejmuje warstwę platformy, a trzeci skupia się na warstwie aplikacji. Co ciekawe, chmury używane są także w branży rozrywkowej, co można zaobserwować na przykładzie takich serwisów jak  Nvidia GRID. <br />
[24-03-08 Jakub ledwoń, wersja 0.5]<br />
