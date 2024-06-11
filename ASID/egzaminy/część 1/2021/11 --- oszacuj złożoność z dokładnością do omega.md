oszacuj z dokładnością do $\Omega$ złożoność poniższego fragmentu kodu 


```
res = 0
for x in range(1,n):
	j=i
	while (j%2==0) j/=2
	res +=j
```

pytanie można zredukować do pytania jaka jest suma zer w sufixach liczb w ciągu 1,...,n
wiemy że jedna na 2 liczby ma 1 zera na końcu
jedna na 4 ma 2 zera na końcu
jedna na 8 na 3 zera 

n/2 + 2* n/4 + 3* n/8 ..... daje O(n)