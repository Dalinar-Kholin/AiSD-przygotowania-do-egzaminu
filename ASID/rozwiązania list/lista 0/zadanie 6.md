
korzystamy z tego że możemy mnożenie a^b rozbić na mnożenia a^2^i \* a^2^i' \* a^2^i'' itd


long long int szybkiePotegowanie(int a, int b){  
    long long int result = 1;  
    for (;b>0;) {  
        if(b&1){  
            result*=a;  
        }  
        a*=a;  
        b>>=1;  
    }  
    return result;  
}


szacunkowo widzimy że liczba mnożeń wykonanych przez ten algorytm w najgorszym przypadku jest równa  

- 2 log(b) -> wykonujemy każde mnożenie w if 
gdzie najlepszy przypadek to 
- log(b) + 1 → wykonujemy tylko mnożenie  w ostatnim obrocie


***pokaż że dla każdego k istnieje takie n że wartości x^n mogą być obliczone przy użyciu mniej niż d(n) - k mnożeń***

gdzie d(n) = szacunkowa liczna mnożeń wykonywanych przez algorytm dla a^n


możemy zauważyć że jeżeli weźmiemy liczbę n która w zapisie binarnym składa się z samych jedynek wtedy liczba wykonanych mnożeń będzie maksymalna, jednocześnie jeżeli weźmiemy n + 1 to liczba mnożeń będzie minimalna a wtedy wystarczy podzielić tą liczbę przez n aby otrzymać ten sam wynik

Tak więc weźmy dowolne k, oraz liczbę n która w zapisie binarnym składa się z  k+1 jedynek
zamiast obliczyć a^n, obliczamy a^(n+1)
liczba mnożeń dla a^n = 2 log(n)
liczba mnożeń dla a^(n+1) = log(n) + 1
gdzie wiemy że log(n) =k+1 
wynik a^(n+1)/n = a^n
o k mnożeń mniej, jednocześnie ten sam wynik