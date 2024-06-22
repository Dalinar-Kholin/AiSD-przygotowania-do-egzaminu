Udowodnij, że przynajmniej jedna z operacji min, deletemin lub insert wykonywanych na kolejce priorytetowej wymaga w najgorszym przypadku czasu Ω(logn)


zakładając że operacja może kosztować poniżej, oznaczmy ten czas poprzez $\sigma$, wtedy wykorzystując algorytm

for x in data:
	insert(queue)
wykonamy to w czasie $n\ \sigma$

następnie
res = \[]
for x in range(queue):
	res.append(queue.takeMin)
	queue.deleteMin
wykonamy to w czasie $n\ 2\sigma$ więc poniżej $n\ \log n$ czyli posortowaliśmy dane szybciej niż to możliwe