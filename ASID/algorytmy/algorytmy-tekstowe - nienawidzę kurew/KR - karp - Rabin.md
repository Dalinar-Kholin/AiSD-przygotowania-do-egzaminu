algorytm ten polega na pierw przypisaniu całemu alfabetowi różnych wartości a następnie hashowanie po kolei kolejnych liczb przesuwając okno o 1 liczbę, jeżeli hash wartości jest zgodny z hashem wzorca sprawdzamy literka po literce czy wartości są takie same
- algorytm ten usprawnia sprawdzanie wzorca
- w najgorszym przypadku działa w czasie O((n-m+1)m) czyli nie uciekliśmy wcale tak daleko on algorytmu naiwnego
- w czasie średnim O(m+n)
- łatwo go uogólnić na wyszukiwanie wzorca w wielu wymiarowych tablicach


implementacja w wenszu

```
def check(t, p) -> bool:  
    for x in range(len(p)):  
        if t[x] != p[x]:  
            return False  
    return True

def rybka(P, T, d, q):  
    n= len(T)  
    m = len(P)  
    ps = 0  
    ts = 0  
    h = (d**(len(P)-1)) %q # h służy temu aby sobie preprocesować potęgę d razy którą musimy ponmożyć element aby go odjąć  
  
    for x in range(len(P)):  
        ps = (d*ps + ord(P[x])) % q  
        ts = (d*ts + ord(T[x])) % q  
  
  
    for x in range(0, len(T)-len(P)+1):  
        if ts == ps:  
            if check(T[x:x+m], P):  
                print("wzorzec pod pozycją",x)  
        if x < n-m:  
            ts = (d*(ts - (ord(T[x])*h)) + ord(T[x+len(P)])) % q  
            if ts < 0: 
                ts += q
    print(ps)  
  
  
rybka("nessa", "nessasesasaternessaanessaa", 26,67)
```

haszujemy od początku, czyli pierw dodajemy liczbę do aktualnego wzorca, a potem wymnażamy wzorzec razy |alfabet| więc po przejściu całego wzorca będzie podniesiona do odpowiedniej potęg, potem aby ją odjąć od wzorca wystarczy odpowiednią liczbę przemnożyć razy preprocesowaną liczbę równą |alfabet|<sup>m</sup>
liczba q to liczba pierwsza > |alfabet| aby nasze wyniki nie odleciały poza długość słowa maszynowego w razie długich wzorców
