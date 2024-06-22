Zauważyłeś, że Quicksort (z deterministycznym pivotem) zachowuje się zadziwiająco regularnie na ciągach z pewnej rodziny A.

Otóż okazało się, że w trakcie wszystkich wywołań rekurencyjnych proderura Partition dokonuje podziału ciągu wejściowego na podciągi o długościach nie mniejszych niż 1/3 i nie większych niż 2/3 długości ciągu wejściowego.

W jakim czasie działa Quicksort na ciągach z rodziny A?


dalej będzie to n log(n)
dzielenie na 1/3 jest wystarczające aby złożoność była logarytmiczna
