porównanie operacji meld na eager i lazy w kopcach 2-mianowych oraz w kopcu fibonacciego
 
### kopce 2-mianowe

***eager***
w tej wersji jako iż zależy nam aby utrzymywać prawidłową strukturę, operacja meld wykonywana jest po każdej operacji i kosztuje nas ona O(log n) ponieważ połączenie 2 drzew 2-mianowych jest możliwe w czasie O(1) a maksymalna ilość drzew w tablicy to log n

***lazy***
w tej wersji kopiec jest leniuszkiem i nie chce mu się za bardzo robić, więc aby połączyć h i h' dodaje po prostu h' do listy pierwotnej i fajrant
czas O(1)
prawdziwe łączenie list wykonywane jest dopiero przy operacji delete min, kiedy to łączone są wszystkie drzewa mające taką samą ilość dzieci


***kopce fibonacciego***

podobnie jak kopce lazy fib jest leniuszkiem i nie chce mu się przeprowadzać skomplikowanego łączenia drzew i zamiast tego, dodaje wierzchołek do listy pierwotnej i fajrant
czas O(1) - tak samo jak w wersji lazy łączenie drzew wykonuje się dopiero przy del min

