Zakładając, że dla wykonania ciągu operacji Union i Find wykorzystujemy, rozważaną na wykładzie, drzewiastą strukturę danych, w której operacje Union wykonujemy w sposób zbalansowany, a operacje Find wykonujemy z kompresją ścieżek, jaki jest koszt zamortyzowany i koszt najgorszego przypadku instrukcji Find?

koszt najgorszego przypadku find:
> kosztem najgorszego przypadku będzie O(log n)w przypadku gdy pierw wykonamy wszystkie instrukcje union, a następnie find, dlaczego log n, ponieważ wiemy że drzewa są budowane w sposób zbalansopwany, w takim przypadku największy rząd wierzchołka to log n, a koszt operacji find to trasa do swojego wierzchołka, który ma rząd log n więc koszt to log n


koszt zamortyzowany:
> log * n + 1
> nawet mnie nie pytajcie dlaczego funkcje Ackermana i te sprawy
