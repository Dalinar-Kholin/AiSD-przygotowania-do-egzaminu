dla danego diagrafu znajdź pierwszy leksykograficznie porządek topograficzny


### zadnie w sumie całkiem łatwe
otóż wystarczy na początku policzyć ile krawędzi wchodzi do wierzchołka 
z własności diagrafu acyklicznego wiemy że musi istnieć co najmniej 1 wierzchołek o stopniu 0 
a następnie zaczynamy:
- wypisujemy wierzchołek o stopniu 0
- usuwany krawędzie które wychodzą z tego wierzchołka
- podliczamy ponownie krawędzie
- robimy tak aż do wypisania wszystkich wierzchołków
	- jeśli mamy 2 wierzchołki o stopniu 0 wybieramy ten o niższym indexie(aby było leksykograficznie poprawnie)


złożoność
czasowa O(V* E)

dowód poprawności można przeprowadzić indukcyjnie, dodając kolejne wierzchołki o stopniu wchodzącym równym 0

