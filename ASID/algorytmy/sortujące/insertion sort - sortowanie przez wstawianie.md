
ideą algorytmu jest to że zaczynamy od lewej strony i co iteracje wstawiamy element na prawo od bariery posortowania do naszej tablicy na odpowiednie miejsce
w sposób taki że dopóki element jest mniejszy od tego na lewo to zmieniamy je miejscami 


***własności***
czas
- dla posortowanych O(n)
- dla nieposortowanych O(n^2)
pamięć
- nie korzysta z dodatkowej pamięci oprócz inputu
- działa 'w miejscu'
***sortuje stabilnie***



![[Pasted image 20240523104251.png]]



implementacja w C

```

void insertionSort(int * tab, int len){  
    for (int i = 0; i < len; ++i) {  
        int index = i;  
        while (index!=0 && tab[index]<tab[index-1]){  
            tab[index]+=tab[index-1];  
            tab[index-1]=tab[index]-tab[index-1];  
            tab[index]-=tab[index-1];  
            index-=1;  
        }  
    }  
}

```