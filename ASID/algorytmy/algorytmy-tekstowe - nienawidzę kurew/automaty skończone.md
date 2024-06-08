w sumie to wszystkie następne algorytmy się na tym opierają np:
- kmp
- kmr

właściwości
- czas działania: O(n) / nie licząc czasu obliczenia funkcji $\sigma$ 
- czas obliczenia funkcji $\sigma$ jest równy O( m| $\sum$ |)

***co robi funkcja $\sigma(x)$?***
> wyznacza najdłuższy prefix wzorca P względem sufixu tekstu x

 ***po chuj my to robimy?***
>  funkcje sigma można preprocesować dla danego wzorca i spłaszczyć złożoność do liniowej


![[Pasted image 20240607154534.png]]

