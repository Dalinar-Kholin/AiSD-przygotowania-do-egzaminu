napisz algorytm który dla zadanego drzewa sprawdzi czy wierzchołek u<sub>i</sub> znajduje się na ścieżce z v<sub>i</sub> do korzenia

jak to sprawdzić, w sumie to całkiem prosto, jako input otrzymujemy listę (o,s) gdzie 
o - ojciec, s - syn

w takim razie możemy pierw stworzyć kompletne drzewo, a następnie przejść się po nim dfs dokładnie raz dla każdego wierzchołka określając input oraz output, taki że jest to globalna zmienna liczbowa, która jest przypisywana przy wejściu do wierzchołka oraz przy wyjściu z niego

![[Pasted image 20240525151106.png]]

implementacja

void dfs(int node){  
    input[node]=counter;  
    for (int i = 0; i <pointers[node+1] - pointers[node] ; ++i) {  
        counter++;  
        dfs2(tabOfChild[pointers[node]+i]);  
    }  
    output[node]=counter;  
}

