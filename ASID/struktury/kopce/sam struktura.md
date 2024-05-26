aby struktura była kopcem musi spełniać kilka w miarę prostych do spełnienia warunków
***struktura***
- wszystkie liście znajdują się na głębokości d, lub d-1 - co implikuje że drzewo jest pełne lub prawie pełne
- wszystkie liście na na poziomie d-1 leżą na prawo od wierzchołków - implikuje że żadem liść nie będzie izolowany, oraz że blok liści na poziomie d, będzie przesunięty na lewo
- położony najbardziej na prawo wierzchołek z poziomu d-1 jest jedynym wierzchołkiem na tym poziomie który może mieć 1 liścia
- warunek 2 i 3 gwarantuje nam nie dość że blok liści na poziomie d będzie przesunięty na lewo z warunku 2 to jeszcze będzie pełny z warunku 3
***uporządkowanie***
- każdy klucz jest mniejszy/większy(zależy od rodzaju kopca) od swojego ojca

***przechowywanie kopców***
kopce są o tyle fajne że mogą być bardzo wygodnie przechowywane w tablicach, ponieważ mają bardzo fajne cechy takie jak
Ojciec wierzchołka n = floor(n/2), ew operacja n>>1
lewe dziecko 2\*n
prawe dziecko (2\*n )+1
wszystkie wierzchołki na poziomie głębokości n => 2^n ---- 2^(n-1)
