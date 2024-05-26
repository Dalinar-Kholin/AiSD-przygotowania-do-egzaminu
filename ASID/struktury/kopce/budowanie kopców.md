aby zbudować kopiec pierw trzeba go umieć naprawiać, jak więc to zrobić


**zakładam że korzystamy z kopców gdzie największy element jest u góry, wpp zmienić nierówności i fajrant**

***naprawa kopca***
zakładając że dodaliśmy właśnie element pod index n, wypadało by sprawdzić, czy przypadkiem nasz nowo dodany element nie jest większy od swojego ojca, a jeżeli tak jest to czy od jego ojca też przypadkiem nie jest większy

### budowa kopca
ogółem to są 2 metody budowania kopca(pewnie scam, ale przedstawiamy 2)
#### *po kolei dodawanie następnych elementów do kopca*
całkiem intuicyjna metoda, jednak równie wolna co intuicyjna, ponieważ zakładając że mamy n elementów, oraz że typowo na wstawienie może być potrzebne wysokość kopca, wychodzi nam O(n log n)
całkiem chujowo
#### *budowanie kopca od dołu i scalanie go*
pierw zapełniamy naszą tablicę po kolei elementami kopca nie dbając o jakikolwiek porządek, a następnie zaczynamy rekurencyjne budowanie kopca od dołu, czytaj pierw wszystkie liście traktujemy jako pojedyncze kopce, a następnie zaczynamy je rekurencyjnie łączyć pierw w kopce 3 elementowe - potem 7 itd aż nie osiągniemy całego kopca
jest to całkiem fajne ponieważ zakładając że mamy 2 poprawne kopce, dodanie 1 elementu w wierzchołku i scalenie ich kosztuje nas O(wysokość kopca) co sumarycznie będzie się składało do O(n) - więcej jest w lista 0 zadanie 9 - więc całkiem ładnie zbiliśmy czas






### usuwanie elementu z kopca
w sumie to na to mamy 2 sposoby
albo

#### pierw usuwamy i łatamy dziurę ostatnim elementem kopca
wykonując tą procedurę wykonamy 2 log n porównań, ponieważ, przepychając liczbę w dół, za każdym razem musimy porównać ze sobą dzieci oraz dodatkowo porównać mniejsze dziecko z przepychanym wierzchołkiem

#### przepychamy dziurę w dół kopca
naszą dziurę przepychamy w dół, wiedząc że jest tam dziura wykonujemy tylko jedno porównanie między dziećmi, kiedy już dziura będzie na najniższym poziomie, zastępujemy ją ostatnim elementem kopca i przepychamy ten element w górę, czemu to jest lepsze skoro element może pójść na samą górę i znowu wyjdzie nam 2 log n, dlatego że statystycznie element ten pójdzie 2 poziomy w górę, co daje man log n + 2
całkiem nieźle


