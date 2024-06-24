(a)Napisać procedurę wstawiania elementu do struktury van Emde Boasa w pseudokodzie i (b)napisać jej złożoność z uzasadnieniem.


```
def insert(x, V);
	if x< v.min
		swap(x, v.min)
	if(summaty(hight(x)) == None):
		insert(hight(x), summary)
		v.children[hight(x)].min = low(x)
	else
		insert(low(x), v.children(hight(x)))
	if x > v.max
		v.max = x
```

dlaczego to działa w log log n
ponieważ wykonujemy wstawianie tylko raz, na zbiorze równym $\sqrt n$ 