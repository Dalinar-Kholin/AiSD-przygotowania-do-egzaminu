Udowodnij, że przynajmniej jedna z operacji min, deletemin lub insert wykonywanych na kolejce priorytetowej wymaga w najgorszym przypadku czasu $\Omega(\log n)$


złóżmy że wszystkie te operacje można wykonać w czasie poniżej, wtedy możemy posortować dowolne liczby poniżej n log n, ponieważ:
alg:
for x in zbiór:
	insert into S 
sorted=\[]
i=0
while S != null:
	sorted\[i++]= min(s)
	delMin(s)

w ten sposób w czasie O(n) posortowaliśmy dowolny zbiór
