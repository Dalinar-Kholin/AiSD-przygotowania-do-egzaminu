Opisz w jaki sposób wykonywana jest operacja "meld" na kopcach dwumianiowych w wersji eager.


kopiec 2- mianowy składa się z listy drzew 2-mianowych, w kopcu eager operacja eager jest gorliwa i łączy ona 2 kopce tak że jeżeli istnieją 2 drzewa takiego samego stopnia, to łączy je tworząc drzewo stopnia +1, procedura łączy drzewa tak długo aż w kopcu nie zostaną tylko i wyłącznie drzewa o różnych stopniach

łączenie 2 drzew jest trywialne ponieważ pierwsze drzewo jest łączone z korzeniem drugiego - dzieje się tak ponieważ drzewa te mają porządek zgodny z kpcowym a nie BST