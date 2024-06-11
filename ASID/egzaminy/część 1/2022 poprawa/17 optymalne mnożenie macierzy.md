W algorytmie wyznającym optymalną kolejność mnożenia macierzy opartym na programowaniu dynamicznym wyliczane są wartości $m_{i,j}$ równe optymalnemu kosztowi obliczenia iloczynu macierzy $M_i , ... , M_j$. Podaj w jaki sposób korzystając z wartości $m_{i,j}$ można wyznaczyć optymalną kolejność mnożenia macierzy.


$m_{ij}$ wyliczane jest iteracyjnie tak że 
$m_{ij}$ = $min(for\ x\ in\ m_{i,\ x}+\ koszt\ wymnozenia\ tych\ macierzy+ m_{x+1,\ j})$
gdzie zakładamy że $m_{ix},\ m_{x+1,j}$ są optymalnym kosztem obliczenia tych macierzy
