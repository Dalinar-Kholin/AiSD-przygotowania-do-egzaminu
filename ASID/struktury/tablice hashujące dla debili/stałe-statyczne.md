yoooooooooooooo
tu się zaczyna zabawa
### co chcemy osiągnąć
słownikiem statycznym chcemy osiągnąć strukturę w której:
- zajmowała O(n) komórek pamięci
- czas konstrukcji jest wielomianowy względem n
- czas find jest O(1)
- NIE MA OPERACJI DELETE ORAZ INSERT

***idea***:
- stosujemy hashowanie 2 poziomowe
- na pierwszym poziomie funkcja rozrzuca elementy do kubełka tak że suma kwadratów elementów w kubełkach jest liniowa ![[Pasted image 20240604213625.png]]
- na 2 poziomie hashujemy niezależnie klucze w każdym kubełku używając tablicy o rozmiarze n<sub>i</sub><sup>2</sup> - hashowanie takie jest bezkolizyjne
- funkcje hashujące są brane losowo z uniwersalnej rodziny funkcji hashujących

***fakt*** - z prawdopodobieństwem co najmniej 1/2 funkcja wybrana losowo z rodziny uniwersalnej umieści n = sqrt(m) w tablicy m elementowej
***uzasadnienie*** - w zbiorze n kluczy jest n<sup>2</sup>/2 par kluczy każda para koliduje z prawdopodobieństwem 1/m stąd oczekiwana liczba kolizji podczas wstawiania n kluczy jest mniejsza niż n<sup>2</sup>/m < 1/2 ---> stosujemy lemat markowa dla t = 1 i fajrant


***lemat*** jeśli do umieszczenia n kluczy w n elementowej tablicy użyjemy losowej funkcji z rodziny funkcji uniwersalnych to mamy prawdopodobieństwo równe 1/2 na to że
![[Pasted image 20240604214727.png]]
dowód jest w skrypcie, pozdrawiam

#### pamięć potrzebna do stworzenia
- nie więcej niż 4n komórek na tablice na 2 poziomie - w razie gdy pierwsza funkcja nie spełnia tego warunku losujemy następną
- 3 komórki na parametry pierwotnej funkcji hashującej
- dla każdej tablicy 2-poziomowej komórka na długość i 2 na parametry co łącznie daje nam 3n komórek
- łącznie mamy O(4n + 3n + 3) = O(n) - spełnione założenia
#### czas tworzenia
- czas oczekiwana liczba losowań funkcji pierwotnej jest nie większa niż 2, sprawdzenie czy funkcja spełnia założenie jest liniowa (wyliczamy ją na każdym elemencie)
- czas losowania funkcji dla 2-poziomowego kubełka jest zależna 
