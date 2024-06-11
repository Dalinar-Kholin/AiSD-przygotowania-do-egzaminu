ile liczb wypluje funkcja 

```
While (n >2) {
  i = 0
  while (n > i * i) {
    i++
  }
  drukuj i
  n = i
}
```

> sqrt* ==> iteracyjny pierwiastek -- jednak nie :c

Zauważmy, że wewnętrzny while trwa logn razy, a po każdym obrocie zewnętrznego while n staje się równy i, czyli $\sqrt{n}$. Czyli mamy równanie rekurencyjne $T(n) = T(\sqrt{n}) + O(\sqrt{n}$. Z Master Theorem oraz z doświadczenia związanego z strukturą van Emde Boasa, wiemy że rozwiązanie tego równania to $\log { \log{n}}$
