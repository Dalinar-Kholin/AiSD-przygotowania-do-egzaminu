podaj optymalny pod względem ilości porównań algorytm znajdujący 2 największy element ciągu


> - porównaj parami liczby $n_k$ oraz $n_{k+1}$, wiadomo że pośród liczb które wygrały swoje porównania będzie liczba 2 co do wielkości
> - wśród liczb które wygrały swoje porównania powtórz algorytm
> - powtarzaj aż nie zostaną 2 liczby, wtedy zwróć tą mniejszą

> wykonuje n + log n - 2 porównań
> 