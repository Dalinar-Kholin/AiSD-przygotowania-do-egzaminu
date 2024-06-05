wytłumaczone jak dla debila - mowa o mnie

#### co tak naprawdę chcemy osiągnąć
tablice hashowania są rozwiązaniem problemu związanego z wybraniem wartości na podstawie klucza w czasie O(1), jak można to osiągnąć?
 - wybieramy jakąś funkcje(hashującą) która dla danego uniwersum kluczy zwraca zawsze wyniki z uniwersum {0, m-1} takie że dla dowolnego klucza z uniwersum szansa na trafienie indexu i jest równa 1/m
 - funkcja musi być szybko obliczana, ponieważ przy każdym sprawdzeniu elementu będziemy się do niej odwoływać

### implementacja
chcielibyśmy ograniczyć nasz słownik do jakiegoś rozmiaru(raczej nie rozmiaru uniwersum kluczy) tak aby nasz słownik optymalizował zajmowane miejsce na czas obliczeń

przyjmując założenie
- słownik rozmiaru m
+
otrzymujemy na mocy
- statystyka to kurwa
- funkcje hashujące nie są idealne
-->
dla istniejącego w słowiku x oraz elementu y który dodajemy h(x) == h(y) → jest to ***kolizja*** 

***dlaczego kolizje są chujowe***
 - spowalniają czas wyszukiwana w słowniku
 - trzeba się nimi osobno zajmować i rozpatrywać jak się nimi zająć
 - tyle wystarczy


### zajmowanie się kolizjami

mamy tak naprawdę 2 sposoby aby zająć się kolizjami, obydwie są średnie

#### ***listy elementów***

zamiast trzymać tabelę w której będziemy trzymali wszystkie wartości, trzymamy wskaźniki na listy w których znajdują się nasze elementy

kiedy dwa elementy mają taki sam hash, oba trafiają do listy elementów pod tym samym indeksem

**rezultat** → teraz wyszukanie elementu nie jest w czasie stałym tylko w czasie zależnym od wypełnienia tej listy, tak że 
 - średni koszt **search** wynosi  Θ(1+n/m) gdzie n - liczba elementów pamiętanych w słowniku
 - n/m nazywane jest też ***współczynnikiem wypełnienia tablicy hashującej***
 - warto zauważyć że gdy n = O(m), to średni koszt operacji Search(oraz wszystkich innych) jest Θ(1).




#### ***adresowanie otwarte***

w adresowaniu otwartym ***trzymamy tylko tablicę m elementów*** i w razie kolizji ***obliczamy ponownie wartość hasha*** na podstawie zasad

aby to udało się spełnić potrzebujemy charakterystycznej funkcji hashującej tak że

h : U x {0,1,2 ... ,m-1} → {0,1,2, ... , m-1} - h jest permutacja zbioru {0,1,2,...,m-1} 
to jest całkiem ważne założenie, ponieważ **gwarantuje nam że zawsze znajdziemy miejsce**

***A***) metoda liniowa
 - h(x,i) = (h'(x) + i) mod m ***! funkcja h musi spełniać zasadę permutacji zbioru !***
 - wiemy że h jest permutacja zbioru m więc wyliczamy kolejne hashe aż nie znajdziemy wolnego miejsca tak że h(x,0) → h(x,1) → ... → h(x,m-1) 
zalety:
- łatwe do implementacji
- łatwe do wytłumaczenia
- nie trzeba martwić się o wybór parametrów
wady:
- może powodować powstawianie zlepków → powstają całkowicie zajęte obszary w tablicy co znacząco spowalnia szybkość słownika 

***B***) metoda kwadratowa
- h(x,i) = (h'(x) + c<sub>1</sub>i + c<sub>2</sub>i<sup>2</sup>) mod m ***! trzeba tak dobrać parametry funkcji c<sub>1</sub> i c<sub>2</sub> aby spełniona była zasada permutacji !***
- tak jak poprzednio iterujemy po i aż nie znajdziemy wolnego miejsca
zalety:
- nie widzę XD
wady 
- trzeba wybierać odpowiednio parametry aby funkcja była poprawna inaczej możemy nie znaleźć miejsca w słowniku
- również powoduje tworzenie się zlepków
***C***) podwójne hashowanie
- h(x,i) = (h'(x) + i\*h''(x)) mod m ***! dla dowolnego x h''(x) powinno być względnie pierwsze z m !*** - gdzie h' i h'' to pomocnicze funkcje hashujące 
- również iterujemy po hashach aż nie znajdziemy wolnego
zalety:
- nie powoduje powstawania zlepków 
- KLo ją poleca, co już coś znaczy
wady:
- trzeba wybrać pomocnicze funkcje hashujące




### usuwanie elementów z tablicy
w przypadku <span style="color:green"><b> usuwania</b></span> elementu można po prostu zaznaczyć że index pod którym jest element jest wolny i fajrant
