W kopcu umieszczono n kluczy 1, 2, 3,..., n.

W korzeniu znajduje się 1.

Na jakiej maksymalnie wysokości znajduje się klucz k? 1<=k<=n


zakładając że korzeń znajduje się na wysokości 0, korzeń o numerze k może znajdować się maxymalnie na wysokości 

k<= log n   ==>  k - możemy stworzyć kopiec gdzie będziemy ustawiali po kolei od 1...k, i otrzymamy taką wysokość
dlaczego nie da się umieścić wyżej ==> załóżmy że ustawiliśmy element k na poziomie k+1 ==> jest co najmniej k kluczy mniejszych niż k ---> sprzeczność z danymi
k> log n  ==> log n ==> wysokość kopca jest ograniczona przez log n