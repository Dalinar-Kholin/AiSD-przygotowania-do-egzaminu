jaki jest koszt budowy 2-poziomowego słownika statycznego

- wybieramy funkcje hashującą z rodziny UFH w czasie O(1) statystycznie 2 próby
- losujemy dla każdego kubełka swoją funkcje z rodziny UFH w czasie O(1) \* n - liczba kubełków
- hashujemy każdy element w czasie stałym i wrzucamy do odpowiedniego kubełka i tam znowu hashujemy - wszystkow w czasie O(1) - powtarzamy n razy

sumując wszystko wychodzi O(n)