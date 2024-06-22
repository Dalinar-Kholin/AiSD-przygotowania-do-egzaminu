Napisz InsertSort w pseudokodzie



```
void insertionSort(int * tab, int len){  
    for (int i = 0; i < len; ++i) {  
        int index = i;  
        while (index!=0 && tab[index]<tab[index-1]){  
            tab[index]+=tab[index-1];  
            tab[index-1]=tab[index]-tab[index-1];  
            tab[index]-=tab[index-1];  
            index-=1;  
        }  
    }  
}
```
