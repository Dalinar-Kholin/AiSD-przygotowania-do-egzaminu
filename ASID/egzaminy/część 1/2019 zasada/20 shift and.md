W algorytmie Shift-And wykonywane są operacje logiczne na słowach maszynowych.

Wytłumacz w jaki sposób?

pierw definiujemy bibliotekę masek dla danej litery, które zawiera 1 na każdej pozycji w patternie gdzie występuje dana litera, następnie definiujemy vektor wyników w który ma długość patternu + 1
w każdym kroku algorytmu dodajemy jeden na początku przesuwany pattern w lewo i andujemy go z maską dla litery którą akurat sprawdzamy
jeżeli jedynka dotrze do | pattern | +1 pozycji oznacza to że wzorzec się zgadza