O ile co najwyżej może

1. Zmniejszyć się
2. Zwiększyć się liczba drzew w kopcu Fibonacciego zawierającym n kluczy wskutek wykonania jednej operacji "delete min"?

1. Mamy n = 2^k + 1 pojedynczych drzew stopnia 1, wiec przy operacji deletemin dostaniemy 2^k drzew stopnia 1, które po merge staną się 1 drzewem k-tego stopnia. Więc z n drzew dostaliśmy 1 drzewo. Odp to | n - 1 |
2. Mamy 1 drzewo stopnia logn składające się z n kluczy, wykonujemy delete min na korzeniu. Korzen w kopcu Fib moze miec maksymalnie log n dzieci (dowod na wykladzie), więc jak obetniemy nasz korzen dostaniemy maksymalnie log n drzew. Więc z 1 drzewa dostalismy logn drzew. Odp to | log n - 1 |
