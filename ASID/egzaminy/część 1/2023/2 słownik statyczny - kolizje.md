Czy w przypadku konstrukcji słownika statycznego opartego na haszowaniu dwupoziomowym dla zestawu 𝑛 kluczy, jeśli wylosowana pierwotna funkcja haszująca umieściła w pierwszym kubełku sqrt(n)​ kluczy, czy należy zmienić tę funkcję?


→ no imo funkcja ta może zostać ponieważ chcemy aby
suma kwadratów elementów w kubełku była < niż 4n
więc zakładając że w pierwszym kubełku wpadło sqrt(n) co daje nam plus n do wyniku to wiemy że każdy kubełek jest równie prawdopodobny więc jeśli każdy element wpadanie do osobnego kubełka to wciąż będziemy mieli sume kwadratów mniejszą niż 4n co spełnia założenia czyli funkcja jest poprawna