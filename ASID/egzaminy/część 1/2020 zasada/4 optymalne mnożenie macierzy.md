w algorytmie wyznaczającym optymalną kolejność mnożenia macierzy, opartym na programowaniu dynamicznym wyliczania jest wartość $m_{ij}$ równa optymalnemu kosztowi obliczenia iloczynu macierzy $M_I \ X \dots \ X\ M_j$
podaj sposób obliczenia wartości $m_{ij}$



obliczenie optymalnej wartości $m_{ij}$ sprowadza się do iteracyjnego sprawdzenia minimalnego kosztu pomnożenia optymalnych macierzy dla danych przedziałów

$m_{ij}$ = $min(for\ k=i\ k<=j\ | \ m_{ik} + m_{kj} + d(k))$
gdzie $d(k)$ jest równe kosztowi pomnożenia macierzy powstałych w skutek $m_{ik}$ oraz $m_{kj}$ 