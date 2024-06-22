Podaj wzór rekurencyjny na liczbę porównań wykonywanych przez algorytm "magicznych piątek", w którym ciąg wejściowy dzielimy na podciągi długości siedem (zamiast 5). Czy taki algorytm nadal wykonuje liniową liczbę porównań? Odpowiedź uzasadnij.


czy algorytm dalej jest liniowy?
=> otóż moim zdaniem jak najbardziej, ponieważ w tym przypadku, dzielimy nasz ciąg na podciągi wielkości 7, a następnie każdy z podciągów sortujemy w czasie stałym(tak samo jak w przypadku 5) zwiększa nam się tylko stała przy O(n), a następnie spośród przedziałów wybieramy liczbę pod indexem 3 i spośród wszystkich tych liczb wybieramy medianę, również możemy posortować te wartości w czasie stałym a następnie wybrać z nich środkową liczbę, jak widzimy wszystkie operacje są wykonywane po sobie w czasie O(n) więc algorytm również zostaje w czasie O(n)

liczba porównań
=> przypał jest przypał