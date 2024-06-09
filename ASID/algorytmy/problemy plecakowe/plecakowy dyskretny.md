problem plecakowy-dyskretny:

> jaka jest największa wartość przedmiotów które możemy zapakować do plecaka o wielkości k, gdy każdy przedmiot ma przypisaną wartość i wagę, każdy przedmiot możemy wziąć tylko raz


idea rozwiązania:
definiujemy optymalne plecaki od 0 do len(items) w których dla każdej wagi będzie optymalna wartość plecaka, teraz sprawdzenie czy opłaca się wziąć przedmiot polega na sprawdzeniu co jest większe - wartość ***poprzedniego plecaka*** dla tej wagi bez tego przedmiotu, czy wartość ***poprzedniego plecaka*** dla tej wagi minus waga przedmiotu plus jego wartość $max(\ dp[iterator-1][w],\  dp[iterator-1][w-itemWeight]+itemValue)$

dlaczego nie weźmiemy żadnego przedmiotu 2 razy?
> patrząc na to że rozpatrujemy tylko poprzedni plecak nie ma porównywania do aktualnego więc nigdzie nie ma możliwości rozpatrzenia tego samego przedmiotu 2 razy

algorytm:
```
func main() {  
    amount := 0  
    weight := 0  
    fmt.Scanf("%d %d", &amount, &weight)  
    items := make([]item, amount)  
  
    for x := 0; x < amount; x++ {  
       fmt.Scanf("%d %d", &items[x].weight, &items[x].value)  
    }  
    dp := make([][]int, amount+1)  
    for x := range len(dp) {  
       dp[x] = make([]int, weight+1)  
    }  
    for x := range weight {  
       dp[0][x] = 0  
    }  
  
    for iterator := range len(items) {  
       iterator += 1  
       for w := range weight + 1 {  
          itemValue := items[iterator-1].value  
          itemWeight := items[iterator-1].weight  
          if itemWeight > w {  
             dp[iterator][w] = dp[iterator-1][w]  
          } else {  
             dp[iterator][w] = max(dp[iterator-1][w], dp[iterator-1][w-itemWeight]+itemValue)  
          }  
       }  
    }  
    for _, x := range dp {  
       fmt.Printf("%v\n", x)  
    }  
    fmt.Printf("%v", slices.Max(dp[len(items)]))   
}
```