Zapisz w pseudokodzie operacje łączenia dwóch kopców Fibonacciego.


```
def add(tab,x):
	if tab[x.degree] >0:
		if tab[x.degree].value > x.value:
			tab[x.degree].add(x)
			node = tab[x.degree]
			tab[x.degree]=null
			add(tab,node)
		else:
			x.add(tab[x.degree])
			tab[x.degree]=null
			add(tab,x )


tab = make(trees[], log(n))

for x in fib.trees:
	add(tab,x)
```
