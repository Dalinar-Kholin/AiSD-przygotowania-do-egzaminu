dowód poprawności algorytmu mnożenia chłopskiego


weźmy 2 dowolne liczby x i y

teraz wiemy że jeżeli
 - y parzyste to 2x +y/2 = x \* y
 - y nieparzyste to 2x + y/2 + x = x\*y
teraz rozkładają po kolei liczby w tabeli
weźmy dla przykładu 55 23


| x   | y   |
| --- | --- |
| 55  | 23  |
| 110 | 11  |
| 220 | 5   |
| 440 | 2   |
| 880 | 1   |
55 \* 23 = 110 \* 11 + 110 = 220 \* 5 +220 +110 = itd rozkładamy liczby
widzimy że liczba y zbiega do 1 więc algorytm się kończy

oraz widzimy że skoro cały czas dzielimy y przez 2 to złożoność czasowa O(log(min(x,y))) możemy sobie wybrać bo mnożenie jest przemienne

pamięciowo O(1) działamy na 3 zmiennych, wynik, x, y
