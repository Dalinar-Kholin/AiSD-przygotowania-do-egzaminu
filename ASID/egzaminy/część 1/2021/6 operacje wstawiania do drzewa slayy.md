przedstaw pseudokod wstawiania klucza do drzew splay, używając jedynie stałej ilości operacji splay() i stałej liczby operacji niskiego rzędu



```
def insert(node, val):
	newRoot = newNode(val)
	splay(25) // aby zbalansować drzewo pod nowy wierzchołek
	if (node ==null) return newRoot
	if (node.val > val):
		newRoot.left = node.left
		newRoot.right = node
	else:
		newRoot.left = node
		newRoot.right = node.left
	 return newRoot
```