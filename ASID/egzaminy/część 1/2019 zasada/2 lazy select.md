W algorytmie LazySelect znajdującym medianę ciągu C wyznaczana jest losowa próbka H.

W tym celu n^3/4 razy losujemy (ze zwracaniem) elementy ciągu C.

Załóżmy, że C składa się z n różnych elementów.

a) Co się stanie jeśli za każdym razem do H został wylosowany ten sam element?

b) Co jeśli do H trafiły dokładnie dwa różne elementy?

Algorytm:
![[Pasted image 20240612182055.png]]

rozwiązanie
> z tego co wiem to po prostu, przeprowadzimy losowanie jeszcze raz i fajrant

> jeżeli warunki poprawności algorytmu nie zostaną złamane, to nic się nie stanie, algorytm pozwala na istnienie wielu takich samych elementów w zbiorze