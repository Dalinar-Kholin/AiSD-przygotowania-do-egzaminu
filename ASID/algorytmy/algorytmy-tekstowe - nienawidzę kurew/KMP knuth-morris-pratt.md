jest to algorytm podobny do algorytmu automatów skończonych
różnicą jest jednak to że funkcja $\sigma$ która została uproszczona i nazwana $\pi$ która jest wyliczana w O(m) (optymalizacja względem $\sigma$ liczonej w O(m | $\sum$ |))

czym jest funkcja pi mówi jaka powinna być wartość q którą powinniśmy porównywać z obecnym wzorcem, całkiem fajne to jest




kmp zaimplementowane w go
```
func computePi(pattern string) (result []int) {  
    m := len(pattern)  
    result = make([]int, m)  
    result[0] = 0  
    k := 0  
    for q := 1; q < m; q++ {  
       for k > 0 && pattern[k] != pattern[q] {  
          k = result[k-1]  
       }  
       if pattern[k] == pattern[q] {  
          k++  
          result[q] = k  
       }  
    }  
    return  
}  
  
func kmp(text, pattern string) int {  
    n := len(text)  
    m := len(pattern)  
    pi := computePi(pattern)  
    q := 0  
    for x := 0; x < n; x++ {  
       for q > 0 && pattern[q] != text[x] {  
          q = pi[q-1]  
       }  
       if pattern[q] == text[x] {  
          q++  
       }  
       if q == m {  
          fmt.Printf("Pattern found at index %d\n", x-m+1)  
          q = pi[q-1]  
       }  
    }  
    return -1  
}
```