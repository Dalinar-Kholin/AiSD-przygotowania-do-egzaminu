Algorytm dynamiczny dla problemu LCS, poznany na wykładzie, oblicza wartości macierzy \(M\) (rozmiaru \(n \times m\)), gdzie \(n\) i \(m\) są długościami ciągów wejściowych. Napisz, czemu równe są wartości \(M_{ij}\) tej macierzy, a następnie zapisz w pseudokodzie procedurę, która na podstawie tej macierzy wyznacza LCS ciągów wejściowych.


--->
wartości i,j w macierzy rozwiązań równe są LCS pierwszych i liter pierwszego ciągu oraz pierwszych j liter 2 ciągu

aby na podstawie tej macierzy wyznaczyć LCS możemy iść prostą ideą

zaczynamy od komórki i,j

jeżeli A\[i] = B\[j] ==>
	print(A\[i])
	i -=1, j-=1
jeżeli A\[i] != B\[j]
	jeżeli M\[i-1]\[j] = M\[i]\[j-1]
		 i-=1
	else
		jeżeli M\[i-1]\[j]> M\[i]\[j-1]
			i-=1
		else
			j-=1

i w sumie to tyle