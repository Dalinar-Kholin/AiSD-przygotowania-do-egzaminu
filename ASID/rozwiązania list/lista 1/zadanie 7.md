mamy nieskierowany graf ważony, oraz ciąg wierzchołków v1,v2,v3,...,vk
niech D<sub>j</sub> będzie sumą najkrótszych ścieżek między parami wierzchołków pozostałych po usunięciu v0,...,vj
ułóż algorytm obliczający D<sub>0</sub>,D<sub>1</sub>,D<sub>2</sub>,...,D<sub>k</sub> 

### rozwiązanie
można zauważyć że dla D<sub>k</sub> graf będzie pusty, dla D<sub>k-1</sub> będzie zawierał 1 element, można więc po kolei dodawać wierzchołek, puścić ma nim dfs obliczający odległości od danych wierzchołków a następnie aktualizować ścieżki dla wierzchołków które mają z nim połączenie

tak więc obliczanie kolejnych D, polega na obliczeniu D +1 a następnie dodanie wierzchołka i aktualizacja ścieżek dla wierzchołków połączonych z nowo dodanym wierzchołkiem

w ogólności jest to Floyd-Warshall, którego efektywnie rozszerzamy o kolejne wierzchołki 

## dowód poprawności
jakoś turbo formalnie to tego nie zrobię