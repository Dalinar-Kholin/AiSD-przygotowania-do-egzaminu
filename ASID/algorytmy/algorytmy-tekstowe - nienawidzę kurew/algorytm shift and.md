ideaa:
- w trakcie czytania tekstu pamiętamy wszystkie prefixy wzorca które są suffixami textu

> działa dobrze dla krótkich wzorców które mieszczą się w słowie maszynowym - (64 bity) a więc max długość słowa to 64 Bajty


PAMIĘTAĆ ŻE W TYM GÓWNIE LITERY SĄ INDEXOWANE OD 1
![[Pasted image 20240607202948.png]]

jak to działa i dlaczego?
otóż zapamiętujemy maskę bitową wzorca, a następnie przesuwamy wzorzec andując ze słownikiem, w naszym słowniku jest zapisane występownie każdej litery na odpowiednim miejscu, więc w momencie przesunięcia sprawdzamy czy dla prefixu pasuje nam nowa litera
mądre w chuj






implementacja w go
```
func shiftAnd(text, pattern string) { 
    m := len(pattern) - 1  
    var vector uint64 = 1  
    dict := make(map[byte]uint64)  
    var isGucii uint64 = 1 << len(pattern)  
    for i := 0; i < len(pattern); i++ {  
       dict[pattern[i]] |= 1 << (i + 1)  
    }  
    fmt.Printf("%v\n", dict)  
    for i := 0; i < len(text); i++ {  
       vector <<= 1  
       vector &= dict[text[i]]  
       vector |= 1  
       fmt.Printf("%b\n", vector)  
       if vector&isGucii ! 0 {  
          fmt.Printf("znaleziono pod %v, %v\n", i-m, i)  
       }  
    }  
}
```
