pod stabilnym sortowaniem kryje się całkiem nieintuicyjne pojęcie, ponieważ nie oznacza ono że sortowanie niezależnie od danych wykonuje się w podobnym czasie, tylko to że


***Sortowanie jest stabilne, jeśli zachowuje kolejność elementów o tej samej wartości w oryginalnym zbiorze danych. Oznacza to, że jeśli dwa elementy są równe w porównaniu, to ich kolejność względem siebie nie zmienia się po sortowaniu.***


co oznacza że jeżeli mam przypadek gdzie sortujemy struktury, np

\[(1,a),(4,b), (2,c),(3,a), (2,a)]

to sortowanie stabilne
wypluje

\[(1,a), (2,c), (2,a),(3,a),(4,b)]

a niestabilne
\[(1,a), (2,a), (2,c),(3,a),(4,b)]

ponieważ w oryginalnej tablicy element (2,c) występuje przed (2,a) to w tablicy rezultatów powinien się on znaleźć przed (2,a)

przykłady algorytmów sortujących stabilnie

- bubble sort
- insertion sort
- merge sort