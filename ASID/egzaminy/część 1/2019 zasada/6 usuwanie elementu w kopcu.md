W której wersji deletemin na kopcu spodziewamy się wykonać mniej porównań i dlaczego? (usuwany element zastępujemy skrajnie prawym liściem z ostatniego poziomu vs przesuwanie dziury na dół).



przesuwając dziurę w dół wykonamy mniej porównań, ponieważ wtedy musimy porównywać tylko dzieci idąc w dół, oraz z ojcem idąc w górę(średnia liczba porównań to 2)
więc otrzymujemy log n + 2 porównań
a przy zastępowaniu w pesymistycznym przypadku musimy porównywać nasz wierzchołek z oboma dziećmi aż do liścia, co daje nam 2 log n porównań