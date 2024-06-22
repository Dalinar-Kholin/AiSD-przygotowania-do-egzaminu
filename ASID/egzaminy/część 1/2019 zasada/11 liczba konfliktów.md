
Jaka jest oczekiwana liczba kolizji gdy do umieszczenia 30 różnych kluczy w tablicy 300 elementowej użyjemy funkcji losowo wybranej z uniwersalnej rodziny funkcji haszujących?

Odpowiedź uzasadnij.


mamy 30 kluczy które mogą między sobą parami kolidować, daje nam to 30 po 2 ==> $\frac{30^2-30}{2}$
mamy 300 kubełków gdzie każdy jest tak samo prawdopodobny że zostanie wybrany - dzięki temu że korzystamy z f funkcji z RUFH tak więc oczekiwana liczba kolizji to
$\frac{30^2-30}{2} * \frac{1}{300}$ = około 1,5 kolizji
