

### Słownik pojęć SR 2017

* [Proces](#proces)
* [Wykorzystanie wątków u klienta w celu polepszenia działania](#wykorzystanie-wątków-u-klienta-w-celu-polepszenia-działania)
* [Obliczenia w chmurze] (#obliczenia-w-chmurze)


### Proces

* Proces (ang. process) -- w informatyce pojęcie związane z systemami operacyjnymi. Proces jest programem w trakcie działania  i jako taki stanowi jednostkę pracy systemu operacyjnego. Kod programu jest statyczną częścią procesu. Dynamiczna część procesu jest reprezentowana przez stan sprzętowych rejestrów komputera, ze szczególnym uwzględnieniem licznika rozkazów. Podczas pracy proces może się rozgałęziać, tworząc  procesy potomne. Każdy proces potrzebuje zasobów, z których korzysta lub które zużywa. Do najważniejszych zasobów procesu należą pamięć operacyjna, czas procesora i pliki.<br />
[17-03-08 Michał Bronikowski, wersja 1.0]<br />
[17-03-08 zpl, wersja 1.1]<br />



### Wykorzystanie wątków u klienta w celu polepszenia działania
* Chociaż istnieją oczywiste możliwości wykorzystania wątków, aby osiągnąć wysoki poziom wydajności , warto zobaczyć, czy wielowątkowość jest skutecznie wykorzystywana. Wcelu przekonania się w jakim stopniu wiele wątków wpływa na procesor multicore,Blake  wspolnie z innymi autorami w. [2010] rzucił okiem na realizację różnych aplikacji we współczesnym systemach zaprojektowanych na zasadach nowoczesnej Architektury SR. Przeglądarki, podobnie jak wiele innych aplikacji klienckich, są interaktywne. Z natury, dlatego oczekiwany czas bezczynności procesora może być dość wysoki. W celu właściwego pomiaru, w jakim stopniu wykorzystywany jest procesor wielordzeniowy, Blake i wspolautorzy , użyli metryki znanej jako równoległość wątku (TLP). Niech c<sub>i</sub> oznaczają  odpowiednio Ułamek czasu,w którym dokładnie ,,i" wątki są wykonywane jednocześnie.Równowagę poziomu wątka określa się następująco:<br />
<img src="https://latex.codecogs.com/gif.latex?TLP&space;=&space;\frac{\sum_{i=1}^{N}&space;\times&space;c_{i}}{1&space;-&space;\times&space;c_{0}}" title="TLP = \frac{\sum_{i=1}^{N} \times c_{i}}{1 - \times c_{0}}" /></a>  <br />
Gdzie N jest maksymalną liczbą wątków, które (mogą) być  wykonywane w tym samym czasie. W badaniu typowa przeglądarka internetowa miała wartość TLP między 1,5 a 2,5.Co oznacza, że w celu efektywnego wykorzystania równoległości maszyna kliencka powinna mieć dwa lub trzy rdzenie, lub też 2-3 procesory. Te wyniki są interesujące, biorąc pod uwagę, że nowoczesne przeglądarki internetowe tworzą setki wątków, a dziesiątki wątków są aktywne jednocześnie (Pamiętaj, że aktywny wątek niekoniecznie musi działać, może zostać zablokowany Żądanie wejścia / wyjścia do wykonania). Widzimy więc, że wielowątkowość służy do organizowania Aplikacji, ale też, że wielowątkowośc nie prowadzi do dramatycznych osiągnięć, poprzez udoskonalanie  wykorzystywanego sprzętu. Przeglądarki mogą być efektywnie przeznaczone do eksploatacji równoległości co  pokazano, na przykładzie przez Meyerowicza i Bodik [2010]. Dostosowując istniejące algorytmy, autorzy zdołali ustalić
Wielokrotne przyspieszenia.<br />
[21-03-08 Michał Bronikowski, wersja 1.0]<br />
[21-03-08 Michał Bronikowski, wersja 1.1]<br />



### Obliczenia w chmurze
* Idea stojąca za obliczeniami w chmurze opiera się na tym, by odciążyć komputery klienckie i przenieść obliczenia, oprogramowanie, a także część danych na serwery chmury. Jedną z niezaprzeczalnych zalet chmury jest skalowalność, klient potrzebujący więcej mocy może wypożyczyć kolejne maszyny. Chmury dzielimy na 4 warstwy: sprzętu, infrastruktury, platformy i aplikacji. Na najniższej warstwie sprzętowej znajdują się podstawowe elementy, takie jak procesory i dyski twarde. Na kolejnych poziomach pojawia się wirtualizacja i rośnie poziom abstrakcji. Warstwa infrastruktury przypomina warstwę sprzętową, ale jej zasoby są wirtualizowane. Warstwę platformy przyrównać można do systemu operacyjnego, oferuje ona programistom środowisko, na którym można łatwo testować i uruchamiać aplikacje. W ostatniej warstwie aplikacji można korzystać z programów przygotowanych przez dostawcę usług. Programy te są wykonywane na sprzęcie dostawcy. Dostęp do chmury uzyskać można przez różne interfejsy, począwszy od linii poleceń, skończywszy na aplikacji sieciowej. Istnieją różne modele dostępu do obliczeń w chmurze. Wyróżnić można IaaS, PaaS i SaaS. Pierwszy model pokrywa warstwę sprzętu i infrastruktury, drugi obejmuje warstwę platformy, a trzeci skupia się na warstwie aplikacji. Co ciekawe, chmury używane są także w branży rozrywkowej, co można zaobserwować na przykładzie takich serwisów jak  Nvidia GRID. <br />
[24-03-08 Jakub ledwoń, wersja 0.5]<br />