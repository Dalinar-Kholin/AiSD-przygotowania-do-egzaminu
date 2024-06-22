opisz redukcję typu dziel i zwyciężaj użytą w FFT

problem obliczenia wielomianu stopnia n-1 w n punktach redukuje się do obliczenia wielomianu stopnia n/2 -1 w n/2 punktach



redukcja polega na podzieleniu liczb na te o parzystych potęgach i nieparzystych potęgach, na podstawie parowania rekurencyjnych obu tablic wyników jesteśmy w stanie obliczyć pierwotną tablicę
tak że

y\[x] = {
	if x \< $\frac{n}{2}$  : $y_e[x]+ \omega^xy_0[x]$  
	if x  >= $\frac{n}{2}$ : $y_e[x-\frac{n}{2}] - \omega^{x-\frac{n}{2}}y_0[x-\frac{n}{2}]$
}
gdzie
$y_e$ = FFT(parzyste)
$y_0$ = FFT(nieparzyste)
$\omega$ = $e^{\frac{2\pi i}{2}}$   