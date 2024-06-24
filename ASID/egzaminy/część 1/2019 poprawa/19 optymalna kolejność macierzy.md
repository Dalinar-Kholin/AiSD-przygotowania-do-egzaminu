Opisz podany na wykładzie algorytm dla problemu wyznaczania optymalnej kolejności mnożenia ciągu macierzy.

Jeśli go nie pamiętasz podaj inny o nie gorszej złożoności

```
def opt(a, b, ciag):
	tab[a][b]={0}
	
```

opt(a,b) = min( opt(a,i) + a\*i\*b + op(i+1,b)) for i in range(a,b)
bierzemy minimalny koszt mnożenia 2 mniejszych macierzy i dodajemy koszt wymnożenia tych macierzy
