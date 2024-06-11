Podczas budowy dwupoziomego słownika statycznego korzystamy z faktu, że umieszczając k kluczy przy użyciu losowej funkcji z uniwersalnej rodziny funkcji haszujących w tablicy o rozmiarze k^2 oczekiwana liczba kolizji wynosi ... .No własnie - ile wynosi?? Odpowiedź uzasadnij.

> prawdopodobieństwo na kolizje to $\frac{1}{k^2}$ liczba możliwych par kluczy to $\frac{k^2-k}{2}$<$\frac{k^2}{2}$, otrzymujemy że liczba skolidowanych kluczy to $\frac{1}{k^2} * \frac{k^2}{2}$ = $\frac{1}{2}$

$\frac{k^2-k}{2}$ bierze się z dwumianu newtona, wybieramy 2 klucze ze zbioru k kluczy
