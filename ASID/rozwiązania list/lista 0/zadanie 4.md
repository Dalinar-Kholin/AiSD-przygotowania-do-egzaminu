Oszacuj z dokładnością do Θ złożoność poniższego fragmentu programu:

Θ → w tym przypadku jest liniowe mimo że wygląda na kwadratowe


res ← 0
for i ← 1 to n do
	j←i
	while (j jest parzyste) j ← j/2
		res ← res + j


to zadanie jest całkiem ciekawe ponieważ patrząc na rozkład binarny liczby możemy powiedzieć ile iteracji w pętli while się wykona ponieważ dzielenie przez 2 można porównać do przesuniącia liczby >>1, liczba nie jest podzielna gdy ma 1 na końcu zapisu binarnego

otóż gdy zapiszemy sobie liczbę binarną np

10101100110 -> wykona się jedno dzielenie, po 1 przesunięciu będzie 1 na końcu 
10101101000 → wykonają się 3 dzielenia bo 3 zera na końcu 

wiedząc to możemy spojrzeć na rozkład liczb binarnych od 1 do n

00001
00010
00011
00100
00101
00110
00111
01000
01001
01010
01011
01100
01101
01110
01111
...
n
co można zauważyć?
otóż to że liczby są bardzo charakterystycznie rozłożone
jedna na 4 jest podzielna przez 2
jedna na 8 jest podzielna przez 4
jedna na 2^K jest podzielna przez 2^(K-1)

wiedząc to możemy zauważyć że w takim razie nasza środkowa pętla while wykona się 

1 raz w 1/4 przypadków
2 razy w 1/8 przypadków
3 razy w 1/16 przypadków
(n-1) razy w 1/2^n przypadków

co daje nam ciąg 
1\*n/4 + 2\* n/8 + 3 \* n/16 + .... + (n-1) \* n/2\*n = 1 \*n
wyciągamy n przed nawias i otrzymujemy ciąg

suma po k=1 do n  (n-1)/2^n co daje wynik 1 


teraz pytanie dlaczego?

odpowiedź jest w sumie całkiem prosta

```
1/2 + 2/4 + 3/8 + 4/16 + ...

= 1/2 + 1/4 + 1/8 + 1/16 + ...    (= 1)
      + 1/4 + 1/8 + 1/16 + ...    (= 1/2)           
            + 1/8 + 1/16 + ...    (= 1/4)
                  + 1/16 + ...    (= 1/8)
                        ....       ....
```

wiemy że 1/2 + 1/4 + ... 1/8 = 1
więc ta suma ciągów złączy się do 1 + 1

***więc na koniec cały algorytm wykona się liniowo względem n***









 
