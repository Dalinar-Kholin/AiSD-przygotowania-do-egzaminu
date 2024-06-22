Napisz procedury realizujące operacje słownikowe na drzewie splay, wykonujące co najwyżej stałą liczbę operacji splay i stałą liczbę operacji niskiego rzędu.

operacje słownikowe to insert, delete, find


insert:
```
def insert(root, value):
	node = makeNode(value)
	if root==null:
		return node
	splay(root,value)
	if root.val < value:
		node.left = root
		node.right = root.right
	else: 
		node.left = root.left
		node.right = root
	retuen node
```

delete:
```
def delete(root, val):
	if root == null:
		return 
	splay(root, val)
	if root.val != val:
		return root
	t1 = root.right
	t2 = root.left
	splay(t1, +0.inf)
	t1.right = t2
	free(root)
	return t1
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