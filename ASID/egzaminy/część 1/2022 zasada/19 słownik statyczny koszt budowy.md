jaki jest koszt budowy 2-poziomowego słownika statycznego

koszt budowy słownika statycznego jest liniowy względem ilości elementów ponieważ

- pierw trzeba wylosować funkcje z rodziny uniwersalnych funkcji hashujących statystycznie powinniśmy podjąc około 2 prób tak aby funkcja która nam się wylosuje tak rozdzieliła elementy do koszyków aby $(\sum_{i=0}^{n}\ k_{i}^2) = 4n$ gdzie $k_{i}$ to ilość elementów w i-tym koszyczku
- następnie w czasie liniowym rozdzielamy elementy do koszyków, w każdym koszyku losując taką funkcję z rodziny uniwersalnych funkcji hashujących aby nie było żadnych kolizji, długość koszyka jest kwadratowa względem ilości elementów, więc wylosowanie takiej funkcji to też statystycznie 2 próby

łącznie mamy:
- liniowe czas na rozdzielenie elementów do koszyków 
- liniowy czas względem rozdzielenia elementów w koszyku

łącznie O(n)