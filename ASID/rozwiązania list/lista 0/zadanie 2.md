Napisz program, który wypisuje w kolejności rosnącej wszystkie wielokrotności liczby 2024 leżące w zadanym przedziale.

## wejście

W jedynym wierszu wejścia znajdują się dwie liczby naturalne a, b, takie, że 0 ≤ a < b < 1000000000 oraz b-a <= 100000.

### Wyjście

W jedynym wierszu wyjścia ma znaleźć się ciąg wszystkich wielokrotności liczby 2024 z przedziału < a,b > wypisanych w kolejności rosnącej. Elementy ciągu mają być oddzielone spacjami.


# kod

```
int main(void) {  
    long a,b;  
    scanf("%ld %ld",&a, &b);  
    int incremental = 1;  
    for(;a<=b;a+=incremental){  
        if (a%2024==0){  
            printf("%d ",a);  
            incremental=2024;  
        }  
    }    
    return 0;  
}
```

# idea algorytmu

idea algorytmu jest całkiem prosta, pierw chcemy dojść do pierwszej liczby podzielnej przez 2024 a następnie dodajemy 2024 aż a nie będzie > b

# dowód

załóżmy nie wprost że algorytm nie działa, to oznacza że 
- nie zatrzymuje się => sprzeczność, zawsze inkrementujemy, a mamy ustawioną barierę górną algorytmu 
- wypisuje w złej kolejności => zawsze idziemy od dołu do góry więc nie ma możliwości pierw wypisania większej a dopiero potem mniejszej
- wypisuje nie wszystkie => zaczynamy na początku przedziału, a następnie znajdujemy pierwszą podzielną przez 2024 i dodajemy 2024 więc aby jakiejś nie wypisać to musiałaby być w postaci innej niż (a * 2024) +2024, co wiemy że jest niemożliwe
- wypisuje za dużo => każda z liczb którą  sprawdzamy czy jest podzielna przez 2024 więc fałsz
