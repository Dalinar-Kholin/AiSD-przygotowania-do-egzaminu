gówno - ale całkiem zmyślne

- działa w czasie O(n log n)
- jest rekurencyjne

idea algorytmu
- definiujemy sobie w = PT <== jest to konkatenacja
- numerujemy wszystkie podsłowa w o długości m w sposób jednoznaczny takie że takie same podsłowa otrzymują takie same numery a różne podsłowa różne numery
- wypisujemy wszystkie pozycje większe od m, na których zaczynają się podsłowa o takim samym numerze co podsłowo zaczynające się na pozycji 1(wzorzec)

praktyka
- zaczynamy od podłów długości 1 - sortujemy liniowo litery występujące w słowie

![[Pasted image 20240608164012.png]]