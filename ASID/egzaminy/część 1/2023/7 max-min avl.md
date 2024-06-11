Jaką wysokość może mieć drzewo AVL o 34 wierzchołkach? Podaj wszystkie możliwe wartości.

drzewo o 34 wierzchołkach może mieć dokładnie 2 wartości

maksymalna wysokość jest osiągana poprzez minimalne drzewo avl o wysokości h

z wykładów wiemy że wysokość minimalnego drzewa AVL jest ograniczona poprzez ciąg Fibonacciego wzorem 
M<sub>h</sub> = F<sub>h+2</sub> -1 ==> gdzie F<sub>h</sub> to liczby Fibonacciego więc szybka matematyka i wiemy
że F<sub>8</sub> = 34 więc idealnie pasuje a więc
M<sub>h</sub> = 8 -1 = 7

a minimalne drzewo AVL o minimalnej wysokości ograniczone jest poprzez pełne drzewo binarne a więc
MIN<sub>h</sub> = 2<sup>h</sup>-1
34<=2<sup>h</sup>-1
h = 6 
MIN<sub>h</sub> = 6

czyli wysokość drzewa jest pomiędzy {6,...,7} 



#max-min-AVL
