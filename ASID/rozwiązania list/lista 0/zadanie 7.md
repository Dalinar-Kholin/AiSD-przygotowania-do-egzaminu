mamy podany algorytm obliczający dany problem i mamy napisać wydajniejszy

while |A| > 1{
	a = random from A
	A = A/a
	b = random from A
	A=A/b
	A = A U {a-b}
}
return ostatni element w zbiorze % 2

zobaczmy jak będzie wyglądał wynik po tym jak rozpiszemy go na drzewo operacji, wiedząc z MDL że a - b %2 = (a%2 -b%2) %2, więc wszystkie nasze operacje na drzewie będą nad ciałem mod2

![[Pasted image 20240523154529.png]]


wiemy też że operacja odejmowania nad ciałem mod2 jest równa operacji Xor, dodatkowo wiemy że kolejność wykonywania xor nie ma znaczenia, nie musimy więc losować elementów, tylko możemy po kolei xorować ze sobą cały zbiór, jako wynik otrzymując parzystość tego zbioru
