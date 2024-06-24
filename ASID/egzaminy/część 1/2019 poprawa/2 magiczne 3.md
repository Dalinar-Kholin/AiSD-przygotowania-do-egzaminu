Jaka jest pesymistyczna złożoność algorytmu magicznych piątek, w którym ciąg jest dzielony na trójki elementów, a nie na piątki?

pod podzieleniu możemy zobaczyć że spośród $\frac{1}{2}$ elementów zbioru ma $\frac{2}{3}$ więc mamy n takich przypadków więc otrzymujemy że $\frac{1}{2} *\frac{2n}{3}$  = $\frac{n}{3}$ elementów jest mniejszych od mediany
więc rekursja wygląda tak
$T(n) = T(\frac{n}{3}) + T(\frac{2n}{3}) + O(n)$ = n log n ==> a = c
T(n/3) - wybór mediany median
T(2/3) - zredukowany wybór
O(n) - podział i wybór median