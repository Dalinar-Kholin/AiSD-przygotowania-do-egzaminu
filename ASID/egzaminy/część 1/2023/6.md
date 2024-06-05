![[Pasted image 20240605004215.png]]
algorytm ten polega na wstawianiu elementu do kopca, a następnie naprawianiu go, i tak dla każdego elementu
naprawa kopca kosztuje O(log n) dla n elementów n log n

nie jest to najbardziej optymalny algorytm ponieważ istnieje 2 podejście do budowy kopców w sposób rekurencyjny, gdzie jego złożoność czasowa to O(n)

sposób rekurencyjny, pierw wpisujemy wszystkie dane do tablicy, nie zważając ma własność porządku, następnie wszystkie liście kopca traktujemy jako kopce 1 elementowe, potem zaczynamy rekurencyjnie łączyć te kopce, możemy zauważyć że ze struktury kopca na ostatnim poziomie nie będziemy musieli naprawiać nic, na 2 co najwyżej 1, na 3 2 itd
patrząc na ilość wierzchołków na danym poziomie tworzy nam się ciąg 
1\* n/2 + 2 \* n/2^2 + 3 \* n/2^3 + ... + n \* n/2^n
co daje nam O(n)

ponieważ możemy rozpisać te ciągi na
po wyciągnięciu n przed nawias zostaje nam ciąg
1/4 + 1/8 ... + 1/2^n = 1/2
	1/8 + ... + 1/2^n = 1/4
		+ ... + 1/2^n = 1/8
			+ ..+ 
			sumuje się do 1
	