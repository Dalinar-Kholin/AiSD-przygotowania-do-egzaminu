dla drzewa binarnego T napisz funkcje rekurencyjne które obliczą
a) liczbę wierzchołków
b) maksymalną odległość między wierzchołkami

struktura drzewa
```
typedef struct tree{  
    int value;  
    struct tree* l;  
    struct tree* r;  
} tree;
```


### ppa
ogółem to chcemy aby każdy liść zwracał nam 0, a każdy węzeł ile ma dzieci plus 1
co daje nam kod
```
int sizeOfTree(tree* node){  
    if (node==NULL){  
        return 0;  
    }  
    int rSize = sizeOfTree(node->r);  
    int lSize = sizeOfTree(node->l);  
    return lSize + 1 + rSize;  
}
```

### ppb
chcemy sprawdzić czy sumowana wysokość naszych poddrzew plus 1 jest większa od  największego dystansu w którymś z naszych poddrzew
```
typedef struct res{  
    int height;  
    int maxDistance;  
}res;

#define MAX(a,b) (a>b? a : b)  
  
res* maxDistance(tree * node){  
    if (node==NULL){  
        return calloc(1, sizeof(res));  
    }  
    res * rRes = maxDistance(node->r);
    res * lRes = maxDistance(node->l);
    
    int acctHeight = MAX(rRes->height, lRes->height) +1; 
    int childMaxDistance= MAX(rRes->maxDistance, lRes->maxDistance);  
    
    res* result = calloc(1,sizeof(res));  
    
    result->height=acctHeight;  
    result->maxDistance=  MAX(childMaxDistance,(rRes->height+lRes->height + 1));  
    free(rRes);  
    free(lRes);  
    return result;  
}
```

złożoność 
czasowa O(n)
pamięciowa O(n) - w ppb kosztuje nas alokowanie kolejnych res


# dowody poprawności poprzez indukcje są trywialne

