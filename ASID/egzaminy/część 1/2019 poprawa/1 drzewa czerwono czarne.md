Rozważamy modyfikację drzewa czerwono-czarnego, w którym warunek “czerwony wierzchołek nie ma czerwonego ojca” jest zastąpiony warunkiem “czerwony wierzchołek, który ma czerwonego ojca nie ma czerwonego dziadka”.

Jaka jest największa wysokość takiego drzewa zawierającegon wierzchołków?

Jak zapewne wiesz oszacowanie asymptotyczne jest niewystarczające.

> Przyjrzyjmy się proponowanej modyfikacji drzewa czerwono-czarnego. Standardowe drzewo czerwono-czarne przestrzega zasady, że czerwony wierzchołek nie może mieć czerwonego ojca. W nowej wersji drzewa, zasada ta jest zmieniona na: "czerwony wierzchołek, który ma czerwonego ojca, nie ma czerwonego dziadka".

Przeanalizujmy, jak ta modyfikacja wpływa na strukturę drzewa:

1. **Standardowe drzewo czerwono-czarne**: Wysokość drzewa czerwono-czarnego wynosi O(log⁡n)O(\log n)O(logn), gdzie nnn to liczba wierzchołków. Dzieje się tak dlatego, że drzewo jest ściśle zbalansowane dzięki ograniczeniom kolorowania i rotacji.
    
2. **Nowe drzewo czerwono-czarne**: Nowe ograniczenie oznacza, że możemy mieć sytuacje, w których sekwencje czerwonych wierzchołków mogą być dłuższe, ale z ograniczeniem, że co drugi wierzchołek w takiej sekwencji musi być czarny.
    

Rozważmy najgorszy przypadek dla nowego drzewa. Najdłuższa możliwa ścieżka, jaką możemy mieć, to naprzemienne sekwencje czarnych i czerwonych wierzchołków. Możemy mieć maksymalnie dwie czerwone krawędzie między każdą parą czarnych wierzchołków.

Oznacza to, że dla każdego czarnego wierzchołka, najwyżej dwa poziomy czerwonych wierzchołków mogą występować.

Formalnie, jeśli hhh to wysokość drzewa w nowych warunkach, to liczba czarnych wierzchołków na ścieżce od korzenia do liścia wynosi ⌊h3⌋\lfloor \frac{h}{3} \rfloor⌊3h​⌋. Ponieważ drzewo czerwono-czarne musi mieć co najmniej jedną czarną krawędź w każdej ścieżce od korzenia do liścia, a liczba czarnych wierzchołków kkk jest równa ⌊h3⌋\lfloor \frac{h}{3} \rfloor⌊3h​⌋, mamy:

2⌊h3⌋≤n2^{\lfloor \frac{h}{3} \rfloor} \leq n2⌊3h​⌋≤n

Ponieważ ⌊h3⌋≈h3\lfloor \frac{h}{3} \rfloor \approx \frac{h}{3}⌊3h​⌋≈3h​ dla dużych nnn, możemy zapisać:

2h3≤n2^{\frac{h}{3}} \leq n23h​≤n

Stąd:

h3≤log⁡2n\frac{h}{3} \leq \log_2 n3h​≤log2​n

h≤3log⁡2nh \leq 3 \log_2 nh≤3log2​n

Tak więc największa wysokość drzewa w nowych warunkach wynosi O(log⁡n)O(\log n)O(logn), ale dokładnie jest to ⌊3log⁡2n⌋\lfloor 3 \log_2 n \rfloor⌊3log2​n⌋.

Wnioskując, maksymalna wysokość drzewa zawierającego nnn wierzchołków wynosi ⌊3log⁡2n⌋\lfloor 3 \log_2 n \rfloor⌊3log2​n⌋.