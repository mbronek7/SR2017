

### Słownik pojęć SR 2017

* [Proces](#proces)
* [Wykorzystanie wątków u klienta w celu polepszenia działania](#wykorzystaniewatkow)


### Proces

* Proces (ang. process) -- w informatyce pojęcie związane z systemami operacyjnymi. Proces jest programem w trakcie działania  i jako taki stanowi jednostkę pracy systemu operacyjnego. Kod programu jest statyczną częścią procesu. Dynamiczna część procesu jest reprezentowana przez stan sprzętowych rejestrów komputera, ze szczególnym uwzględnieniem licznika rozkazów. Podczas pracy proces może się rozgałęziać, tworząc  procesy potomne. Każdy proces potrzebuje zasobów, z których korzysta lub które zużywa. Do najważniejszych zasobów procesu należą pamięć operacyjna, czas procesora i pliki.<br />
[17-03-08 Michał Bronikowski, wersja 1.0]<br />
[17-03-08 zpl, wersja 1.1]<br />



### Wykorzystanie wątków u klienta w celu polepszenia działania
* Chociaż istnieją oczywiste możliwości wykorzystania wątków, aby osiągnąć wysoki poziom wydajności , warto zobaczyć, czy wielowątkowość jest skutecznie wykorzystywana. Wcelu przekonania się w jakim stopniu wiele wątków wpływa na procesor multicore,Blake  wspolnie z innymi autorami w. [2010] rzucił okiem na realizację różnych aplikacji we współczesnym systemach zaprojektowanych na zasadach nowoczesnej Architektury SR. Przeglądarki, podobnie jak wiele innych aplikacji klienckich, są interaktywne. Z natury, dlatego oczekiwany czas bezczynności procesora może być dość wysoki. W celu właściwego pomiaru, w jakim stopniu wykorzystywany jest procesor wielordzeniowy, Blake i wspolautorzy , użyli metryki znanej jako równoległość wątku (TLP). Niech c<sub>i</sub> oznaczają  odpowiednio Ułamek czasu,w którym dokładnie ,,i" wątki są wykonywane jednocześnie.Równowagę poziomu wątka określa się następująco:<br />
TLP =(&sum<sub>i</sub> i * c<sub>i</sub>) / 1 - c<sub>0</sub>
Gdzie N jest maksymalną liczbą wątków, które (mogą) być  wykonywane w tym samym czasie. W badaniu typowa przeglądarka internetowa miała wartość TLP między 1,5 a 2,5,Co oznacza, że w celu efektywnego wykorzystania równoległości maszyna kliencka powinna mieć dwa lub trzy rdzenie, lub też 2-3 procesory. Te wyniki są interesujące, biorąc pod uwagę, że nowoczesne przeglądarki internetowe tworzą setki wątków, a dziesiątki wątków są aktywne jednocześnie (Pamiętaj, że aktywny wątek niekoniecznie musi działać, może zostać zablokowany Żądanie wejścia / wyjścia do wykonania). Widzimy więc, że wielowątkowość służy do organizowania Aplikacji, ale też, że wielowątkowośc nie prowadzi do dramatycznych osiągnięć, poprzez udoskonalanie  wykorzystywanego sprzętu. Przeglądarki mogą być efektywnie przeznaczone do eksploatacji równoległości co  pokazano, na przykładzie przez Meyerowicza i Bodik [2010]. Dostosowując istniejące algorytmy, autorzy zdołali ustalić
Wielokrotne przyspieszenia.<br />
[21-03-08 Michał Bronikowski, wersja 1.0]<br />

