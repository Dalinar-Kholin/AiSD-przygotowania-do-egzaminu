Zapisz w pseudokodzie procedurę znajdowania następnika elementu w strukturze van Emde Boasa. Napisz jaką ma ona złożoność.


```
successor(x, V)
	if v.children[hight(x)].max = low(x)
		i = successor(hight(x), sumarry)
		return i.min + i*sqrt(|S|)
	else 
		j = sucessor(low(x), v.children(hight(x)))
		return hight(x) * sqrt(|s|) + j
```
złożoność log log n
nie porywam się na dowody