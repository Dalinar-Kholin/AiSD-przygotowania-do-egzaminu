W algorytmie wyznaczającym optymalną kolejność mnożenia macierzy, opartym na programowaniu dynamicznym, wyliczana jest wartość $m_{ij}$ równa optymalnemu kosztowi obliczenia iloczynu macierzy $M_i \times \dots \times M_j$. Podaj sposób obliczenia wartości $m_{ij}$.

$m_{ij}$ wyliczane jest iteracyjnie tak że 
$m_{ij}$ = $min(for\ x\ in\ m_{i,\ x}+\ koszt\ wymnozenia\ tych\ macierzy+ m_{x+1,\ j})$
gdzie zakładamy że $m_{ix},\ m_{x+1,j}$ są optymalnym kosztem obliczenia tych macierzy
