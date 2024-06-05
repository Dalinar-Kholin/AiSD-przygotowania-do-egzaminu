Podaj definicję problemu plecakowego z powtórzeniami i przedstaw pseudowielomianowy algorytm rozwiązujący ten problem. Uzasadnij stwierdzenie, że jest on pseudowielomianowy.

problem plecakowy z powtórzeniami - jakie przedmioty możemy spakować do plecaka o rozmiarze k tak aby wartość przedmiotów była jak największa, zakładając że każdy przedmiot na swoją wagę i wartość oraz możemy go wziąć dowolną ilość razy

algorytm
```
dp= [float("-inf")]*k  
przedmioty = wczytanie przedmiotów  
for x in range(n):  
    for y in range(k):  
        if dp[y]< dp[y-x.rozmiar]+ x.cena:  
            dp[y]=dp[y-x.rozmiar]+ x.cena  
  
print(max(dp))
```

jak możemy zauważyć złożoność czasowa tego algorytmu to n\*k czyli złożoność czasowa nie jest uzależniona od rozmiaru danych wejściowych, tylko od wartości tych danych
