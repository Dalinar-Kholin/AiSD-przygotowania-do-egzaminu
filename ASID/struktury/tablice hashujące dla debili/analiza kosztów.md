przy założeniu że 
z = n/m < 1
oczekiwana liczba prób zakończonych fiaskiem jest 
liczba prób <= 1 / 1 - z

Załóżmy, że utworzyliśmy słownik i teraz wykonujemy wiele operacji Search. Jeżli
tablica jest zajęta w 50%, to średnia liczba prób przy poszukiwaniu zakończonym niepowodzeniem
jest nie większa od 2; gdy tablica zajęta jest w 90%, to liczba ta jest nie większa od 10.

***wniosek 1***→wstawienie elementu do tablicy wymaga średnio 1/1-z prób

***PRAWDOPODOBIEŃSTWA(to kurwy)*** 
hashowanie, jest tożsame z problemami z dyskretnej, czytaj mamy m kul które rozrzucamy losowo do n urn
- ile kul należy się spodziewać w najpopularniejszej urnie
- ile kul można wrzucić aby najprawdopodobniej w każdej urnie była 1 kula
jeżeli mamy m urn i n kul:
- jeśli m <= sqrt(n) to z prawdopodobieństwem 1/2 nie ma kolizji