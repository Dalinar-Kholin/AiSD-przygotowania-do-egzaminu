***algorytm***
dzielimy nasz zbiór liczb na zbiory 5 - elementowe
wybieramy spośród nich medianę
spośród tych median wybieramy medianę
dzielimy zbiór na niemniejsze liczby niż znaleziona mediana i na liczby większe niż znaleziona mediana, k - tej liczby szukamy w odpowiednim zbiorze


złożoność
nasza złożoność opisuje się wzorem
![[Pasted image 20240622144230.png]]
gdzie
T(n/5) - znajdowanie mediany wśród mediany median
T(7n/10) - dalsze wyszukiwanie elementu - dowód za chwilę
O(n) - podzielenie zbiorów i znalezienie median

***dowód na T(7n/10)***
zakładając że mamy wszystkie różne elementy wiemy że w naszym zbiorze jest dokładnie 
$\frac{1}{2}(\frac{n}{5})$ zbiorów gdzie $\frac{3}{5}$ elementów jest mniejszych od mediany, co daje nam łącznie $\frac{3n}{10}$ elementów mniejszych od mediany i w tożsamy sposób możemy otrzymać $\frac{3n}{10}$ elementów większych od mediany, więc nasz zbiór zawsze ograniczymy do co najmniej $\frac{7n}{10}$

dlaczego to jest liniowe
![[Pasted image 20240622145001.png]]
