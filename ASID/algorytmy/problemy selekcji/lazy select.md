idea jest całkiem prosta i w sumie to zajebista w swojej prostocie
otóż 

chcemy wybrać taki zbiór elementów, aby dało się go posortować w czasie liniowym oraz, mediana tego zbioru była medianą całego zbioru\

aby to zrobić chcemy wybrać takie 2 elementy że między nimi znajduje się mediana oraz że posortowanie ciągu między nimi jest liniowe

pojawia się pytanie, jak to zrobić
a ja mówię proste

> wybieramy losowo ze zbioru $n^{3/4}$ elementów(elementy mogą się powtarzać) --> ich wybranie jest w czasie stałym

mając taki posortowany zbiór, nazwijmy go C
chcemy teraz wybrać l, h tak aby z dużym prawdopodobieństwem znajdowała się między nimi mediana

>chcemy aby moc zbioru,  powstałego między l, h był $\frac{n}{\log n}$, w wyniku czego możemy go posortować dowolnym algorytmem liniowo

a więc aby wybrać l, h sortujemy R, a następnie wybieramy elementy na pozycji $l = \lfloor n^{3/4}/2-\sqrt n \rfloor$  $h = \lfloor n^{3/4}/2 + \sqrt n \rfloor$
w ten sposób C zawiera $2\sqrt n$ próbek wokół mediany w zbiorze R
wszystko zostało tak dobrane aby prawdopodobieństwo oraz czasy wykonywania się zgadzały

![[Pasted image 20240622124314.png]]


dlaczego są takie warunki stopu?
> $l_d > n/2$ - nasz zbiór C nie będzie zawierał mediany, tożsame z $l_u>n/2$
> jeżeli |C| > $4n^{3/4}$ wtedy nie wykona się liniowo więc też trzeba powtórzyć

algorytm ten nazywa się algorytmem las Vegas XDDD