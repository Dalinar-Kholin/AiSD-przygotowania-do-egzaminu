Opisz algorytm tworzenia kopca, którego złożoność określa równanie $T(n) = O(\sum_{i=1}^nlog\ i)$. Czy jest to najszybszy możliwy algorytm tworzenia kopca? Odpowiedź uzasadnij.


opis algorytmu:
> po kolei dodajemy do kopca kolejne wartości od 0 do n-1
> jako iż czas dodania wartości do kopca to log n otrzymujemy n log n


czy da się szybciej?
> oczywiście że się da,
> zamiast dodawać wartości po kolei budujemy kopce rekurencyjnie od dołu od liści aż do korzenia zawsze łącząc 2 kopce nowym wierzchołkiem
> dlaczego jest to szybsze, ponieważ na podstawie spostrzeżenia możemy zobaczyć że tworzy nam się ciąg
> więcej pod ![[zadanie 9]]
> 