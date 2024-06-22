![[Pasted image 20240612185247.png]]

Dla konkretnego h'(k) możemy rozwiązać, jedynie 100 kolizji, potem rozwiązanie kolizji zapętla się.

Dlaczego?

Ponieważ h(k, i) = (h'(k) + 100i + 1000i^2) mod 10000

jeśli zmieniamy jedynie i, to h'(k) jest stałe stąd rozważamy tylko (100i + 1000i^2) mod 10000

Stąd

100(i + 10^2) mod 10000 = (i + i^2) mod 100

Możemy zauważyć, że po 100 rozwiązanych konfliktach kolejne próby ich rozwiązania skończą się nieskończonym zapętleniem.