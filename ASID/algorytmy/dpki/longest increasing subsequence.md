jako iż jest to dp - trzeba jakoś zdefiniować tablicę dynamiczną
dp\[i]  ==> długością największego rosnącego ciągu do indexu i

```
def lis(arr):  
    n = len(arr)  
	lis = [1]*n
    for i in range(1, n): 
        for j in range(0, i):  
            if arr[i] > arr[j] and lis[i] < lis[j] + 1:  
                lis[i] = lis[j]+1  
    
	for i in range(n):  
        maximum = max(maximum, lis[i])  
  
    return maximum
```

takie wybieranie można łatwo uogólnić na przykład na wybieranie szybko rosnącego podciągu takiego że

Ciąg $a_0,a_1,\ldots, a_r$​ nazywamy szybko rosnącym, jeżeli dla każdego 0<k≤r0 < k $\leq$ r0<k≤r zachodzi ak≥ak−1+ka_k $\geq$ a_{k-1} + kak​≥ak−1​+k. Napisz algorytm, który dla zadanego ciągu liczb naturalnych znajdzie jego najdłuższy podciąg szybko rosnący.

wystarczy zmienić lekko warunek tak aby 

```
def lis(arr):  
    n = len(arr)  
  
    for i in range(1, n): 
        for j in range(0, i):  
            if arr[i] > arr[j] + lis[j] and lis[i] < lis[j] + 1:  
                lis[i] = lis[j]+1  
    
	for i in range(n):  
        maximum = max(maximum, lis[i])  
  
    return maximum
```
