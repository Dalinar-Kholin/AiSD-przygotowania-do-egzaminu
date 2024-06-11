do kopca wstawiono klucze 1,2,3... 2<sup>k-1</sup> wypisz klucze które na pewno nie znajdą się w liściach



lemat element k nie może być niżej niż k-ty poziom ==> 
załóżmy nie wprost że element trafił do poziomu k+1, ale ==> że ponad nim jest k liczb większych od niego, ale żadna liczba w zbiorze się nie powtarza więc sprzeczność

=> wszystkie klucze mniejsze równe k-2, ponieważ tworząc kopiec od korzenia do liścia po kolei dfs możemy umieścić (k-1)-ty element w liściu, jednocześnie wiemy że żaden element mniejszy od niego z lematu nie może trafić do liścia 