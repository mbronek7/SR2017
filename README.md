

### Słownik pojęć SR 2017

* [Proces](#proces)
* [Wykorzystanie wątków u klienta w celu polepszenia działania](#wykorzystanie-wątków-u-klienta-w-celu-polepszenia-działania)
* [Obliczenia w chmurze](#obliczenia-w-chmurze)


### Proces

* <p align="justify">Proces (ang. process) -- w informatyce pojęcie związane z systemami operacyjnymi. Proces jest programem w trakcie działania  i jako taki stanowi jednostkę pracy systemu operacyjnego. Kod programu jest statyczną częścią procesu. Dynamiczna część procesu jest reprezentowana przez stan sprzętowych rejestrów komputera, ze szczególnym uwzględnieniem licznika rozkazów. Podczas pracy proces może się rozgałęziać, tworząc  procesy potomne. Każdy proces potrzebuje zasobów, z których korzysta lub które zużywa. Do najważniejszych zasobów procesu należą pamięć operacyjna, czas procesora i pliki.<br /></p>
[17-03-08 mbr, wersja 1.0]<br />
[17-03-08 zpl, wersja 1.1]<br />


 
### Wykorzystanie wątków u klienta w celu polepszenia działania
* Wątki wykorzystuje się w procesach w celu wykonywania wielu rzeczy jednocześnie. Wątek z definicji jest podstawową jednostką sterowania w procesie. Procesor może jednocześnie wykonywać tyle wątków, ile ma rdzeni. Procesor w każdej sekundzie wielokrotnie przełącza się pomiędzy wykonywanymi wątkami. Dzięki czemu użytkownik ma wrażenie, ciągłości wykonywania wszystkich aktualnie działających wątków. W systemach rozproszonych część przetwarzania może być wykonywana po stronie użytkownika.Wykorzystywanych w tym celu wątków nie należy mylić z <b> wątkami poziomu użytkownika</b> (w odróżnieniu od wątków jądrowych).Wątki działające <b>u użytkownika</b>, tj. po stronie aplikacji klienta, są stosowane w celu odciążenia
serwera. Największą zaletą tego rozwiązania jest zmniejszenie kosztów związanych z wykonywaniem obliczeń przez nasz serwer. Umożliwia to obsługiwanie przez serwer większej liczby użytkowników którzy mogą korzystać z naszej aplikacji w tym samym czasie. Można przerzucić znaczna ilość obliczeń na maszynę klienta i w ten sposób unikać opóźnień w interakcji klient-serwer. Dobrym przykładem udanego użycia takiego rozwiązania są nowoczesne przeglądarki internetowe, które tworzą wątki,z których część jest aktywna jednocześnie przy czym chodzi tu o wątki działające po stronie klienta. Na przykład użytkownik, zamykający nowe okno od razu ujrzy efekt, lecz związany z tym proces (i jego wątki) jest stopniowo wygaszany w tle.<br />
[17-03-21 mbr, wersja 1.0]<br />
[17-03-25 mbr, wersja 2.0]<br />
[17-03-30 zpl, wersja 2.1]<br />


### Obliczenia w chmurze
* Idea stojąca za obliczeniami w chmurze opiera się na tym, by odciążyć komputery klienckie i przenieść obliczenia, oprogramowanie, a także część danych na serwery chmury. Sam termin można wyśledzić już w latach 90, ale jego spopularyzowanie przypisuje się korporacji Amazon, który zaczął świadczyć takie usługi w roku 2006.  Jedną z niezaprzeczalnych zalet chmury jest skalowalność, klient potrzebujący więcej mocy może wypożyczyć kolejne maszyny. Chmury dzielimy na 4 warstwy: sprzętu, infrastruktury, platformy i aplikacji. Na najniższej warstwie sprzętowej znajdują się podstawowe elementy, takie jak procesory, pamięć i dyski twarde. Na kolejnych poziomach pojawia się wirtualizacja i rośnie poziom abstrakcji. Warstwa infrastruktury przypomina warstwę sprzętową, ale jej zasoby są wirtualizowane. Warstwę platformy przyrównać można do systemu operacyjnego, oferuje ona programistom środowisko, na którym można łatwo testować i uruchamiać aplikacje. W ostatniej warstwie aplikacji można korzystać z programów przygotowanych przez dostawcę usług. Programy te są wykonywane na sprzęcie dostawcy. Warto zauważyć, że im większa warstwa, tym bardziej faktyczne maszyny stają się mniej widoczne dla klienta. Ten brak transparentności może przeszkadzać przy szacowaniu złożoności aplikacji. Pojawiają się też wątpliwości na temat bezpieczeństwa plików w chmurze i zagrożenia dla naszej prywatności. Dostęp do chmury uzyskać można przez różne interfejsy, począwszy od linii poleceń, skończywszy na aplikacji sieciowej. Istnieją różne modele dostępu do obliczeń w chmurze. Wyróżnić można IaaS, PaaS i SaaS. Pierwszy model pokrywa warstwę sprzętu i infrastruktury, drugi obejmuje warstwę platformy, a trzeci skupia się na warstwie aplikacji. Co ciekawe, chmury używane są także w branży rozrywkowej, co można zaobserwować na przykładzie takich serwisów jak  Nvidia GRID. <br />
[24-03-08 Jakub ledwoń, wersja 0.5]<br />
