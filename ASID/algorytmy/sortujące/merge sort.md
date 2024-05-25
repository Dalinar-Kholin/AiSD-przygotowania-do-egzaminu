sortowanie przez scalanie
jest przykładem algorytmu dziel i zwyciężaj

dziel - dzielimy tablice na 2 mniejsze
zwyciężaj - oblicz mergeSortem obie podtablice
połącz - scal posortowane tablice

***własności***

- czas O(n log n)
- pamięć O(n) - da się napisać wersje nierekurencyjną tak samo szybką, ale korzystającą z liniowej ilości pamięci
- jeżeli będziemy preferować zawsze lewą stronę tablicy, będzie stabilne
- **nie działa w miejscu**
- najgorszy - średni - najlepszy przypadek = n log n


nierekurencyjna wersja 


```
  

void merge(int arr[], int left, int mid, int right) {
    int n1 = mid - left;
    int n2 = right - mid;
    int* leftArr = (int*)malloc(n1 * sizeof(int));
    int* rightArr = (int*)malloc(n2 * sizeof(int));

    for (int i = 0; i < n1; i++) {
        leftArr[i] = arr[left + i];
    }
    for (int i = 0; i < n2; i++) {
        rightArr[i] = arr[mid + i];
    }

    int i = 0, j = 0, k = left;
    while (i < n1 && j < n2) {
        if (leftArr[i] <= rightArr[j]) {
            arr[k] = leftArr[i];
            i++;
        } else {
            arr[k] = rightArr[j];
            j++;
        }
        k++;
    }
    while (i < n1) {
        arr[k] = leftArr[i];
        i++;
        k++;
    }
    while (j < n2) {
        arr[k] = rightArr[j];
        j++;
        k++;
    }
    free(leftArr);
    free(rightArr);
}
void merge_sort_iterative(int arr[], int n) {
    int width;
    for (width = 1; width < n; width = 2 * width) {
        for (int i = 0; i < n; i = i + 2 * width) {
            int left = i;
            int mid = (i + width < n) ? (i + width) : n;
            int right = (i + 2 * width < n) ? (i + 2 * width) : n;
            merge(arr, left, mid, right);
        }
    }
}


```