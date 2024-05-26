Procedura buduj − kopiec tworzy kopiec w czasie O(n).

gdzie procedura buduj kopiec polega na rekurencyjnym budowaniu kopca od dołu
tak że pierw tworzymy strukturę drzewa która nie ma zachowanego porządku, a następnie rekurencyjnie tworzymy kopiec tak że traktujemy liście drzewa jako kopce i łączymy je ze sobą, następnie łączymy 3-elementowe drzewa itd...

można zauważyć że takie budowanie drzewa będzie wymagało po każdym połączeniu przywrócenia porządku w nowo powstałym kopcu, korzystając jednak z tego że łączymy 2 kopce to maksymalna liczba swapów potrzebnych do przywrócenia porządku to wysokość nowo powstałego kopca, wiedząc że na najniższym poziomie kopca jest n/2 elementów 
na przedostatnim n/4 elementów, tworzy nam się ciąg 

1 \* n/4 + 2\* n/8 + 3\*n/16....+ (n-1)\* 1/2^n co z zadania 4 wiemy że sumuje się do O(n)





![[Pasted image 20240525162952.png]]
 