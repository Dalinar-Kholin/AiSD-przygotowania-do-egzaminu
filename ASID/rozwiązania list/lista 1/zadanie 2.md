aaaaaaaaaaaaaaaaaaaaaaaaaaaaa
aaaaaaaaaaaaaaaaaaaaaaa
aaaaaaaaaaaaaaaaaaa
aaaaaaaaaaaaaaaa

mamy napisać w pseudokodzie procedury przywracania porządku w kopcu minmaxowym znajdującym się w jednej tablicy, jak to dokładnie wygląda zapraszam do Notatki #kopceJakoKolejkiMin-Max 

mamy do zaimplementowania 3 operacje, z czego dwie są tożsame 

- przywracanie porządku
- usuwanie minimum
- usuwanie maximum


### przywracanie porządku
 przywracanie porządku na takim grafie zacząłbym od jednego jego końca i szedł w stronę 2, na każdym wierzchołku po kolei wykonując operacje scalania kopców
#### przywrócenie porządku dla 1 elementu 
pierw trzeba sprawdzić czy znajdujemy się na poziomie min, czy max, następnie w zależności od tego sprawdzić czy nie powinniśmy znaleźć się na poziomie naszego ojca

### Operacje przywracania porządku

# na razie GTP, nie chce mi się tego robić jak jasny chuj


#### 1. Wstawianie elementu

- **Krok 1:** Dodaj nowy element na końcu kopca (na końcu tablicy).
- **Krok 2:** Sprawdź, na którym poziomie znajduje się nowy element (min lub max).
- **Krok 3:** Jeśli nowy element znajduje się na poziomie min:
    - Jeśli nowy element jest większy od swojego rodzica, zamień go z rodzicem i kontynuuj przywracanie porządku jak dla poziomu max.
    - Jeśli nowy element jest mniejszy od swojego rodzica, kontynuuj przywracanie porządku na poziomie min.
- **Krok 4:** Jeśli nowy element znajduje się na poziomie max:
    - Jeśli nowy element jest mniejszy od swojego rodzica, zamień go z rodzicem i kontynuuj przywracanie porządku jak dla poziomu min.
    - Jeśli nowy element jest większy od swojego rodzica, kontynuuj przywracanie porządku na poziomie max.

#### 2. Usuwanie elementu

- **Krok 1:** Zastąp korzeń (najmniejszy lub największy element) ostatnim elementem kopca.
- **Krok 2:** Usuń ostatni element kopca (który teraz znajduje się na początku).
- **Krok 3:** Sprawdź, czy korzeń znajduje się na poziomie min czy max.
- **Krok 4:** Jeśli korzeń znajduje się na poziomie min:
    - Porównaj nowy korzeń z jego dziećmi i wnukami, aby znaleźć najmniejszy element.
    - Zamień korzeń z najmniejszym z tych elementów.
    - Kontynuuj przywracanie porządku dla poddrzewa zawierającego zamieniony element.
- **Krok 5:** Jeśli korzeń znajduje się na poziomie max:
    - Porównaj nowy korzeń z jego dziećmi i wnukami, aby znaleźć największy element.
    - Zamień korzeń z największym z tych elementów.
    - Kontynuuj przywracanie porządku dla poddrzewa zawierającego zamieniony element.