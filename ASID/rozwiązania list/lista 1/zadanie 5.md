ułóż algorytm który dla acyklicznego diagrafu znajdzie długość najdłuższej drogi w G, następnie zmodyfikuj go tak aby wypisywał tą drogę

# samo znalezienie długości
puszczamy dfs po grafie z wszystkich wierzchołków które mają stopień 0, następnie wybieramy ten który znalazł najdłuższą ścieżkę

### dowód poprawności
załóżmy że najdłuższa ścieżka nie wychodzi a wierzchołka który ma stopień wchodzący 0
 - skoro graf jest acykliczny to można dodać wierzchołek go poprzedzający i uzyskać dłuższą ścieżkę - mamy sprzeczność, więc musi wychodzić z wierzchołka o stopniu 0
 - sprawdzamy wszystkie wierzchołki o stopniu 0 więc nie ma możliwości że go pominiemy


### odtwarzanie ścieżki
puszczamy jeszcze raz dfs tym razem z ustaloną największą długością i w każdej iteracji dodajemy aktualny wierzchołek do listy, kiedy długość będzie równa tej najdłuższej printujemy listę wierzchołków i kończymy program
