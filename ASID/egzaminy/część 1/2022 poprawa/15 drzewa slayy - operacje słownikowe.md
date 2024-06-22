Napisz procedury realizujące operacje słownikowe na drzewie splay wykonujące co najwyżej stałą liczbę operacji splay i stałą liczbę operacji niskiego rzędu.

insert
delete 
find


insert:
```
def insert(node,k):
	newRoot = newNode(k) 
	if node==null:
		return newRoot
	splay(k)
	if(k > node.val):
		newRoot.left = node
		newRoot.right = node.right
	else:
		newRoot.left = node.letf
		newRoot.right = node	
```

find:
```
def find(root, value, prev):
	if root ==null:
		splay(root,prev)
		return root
	if root.val == value:
		splay(root, value)
	if root.val > value:
		return find(root.left, value, root.value)
	else:
		return find(root.rigth, value, root.value)
```
delete:
```
def del(root, k):
	if root==null:
		return null
	splay(root, k)
	if root.value != k:
		return root
	else:
		if root.left == null:
			return root.right
		splay(root.right, +0.inf) //ustawi na roota największy wierzchołek
		root.right.left = root.left
		free(root)
		return root.right 
```