```python
class Node: 
	def __init__(self, data): 
		self.data = data 
		self.left = None
		self.right = None

def areIdentical(node1, node2): 
	 if node1 is None and node2 is None: 
		return True
	 if node1 is None or node2 is None: 
		return False
	 return (node1.data == node2.data and areIdentical(node1.left , node2.left) and areIdentical(node1.right, node2.right) ) 

def isSubtree(First, Second): 
	 if Second is None: 
		return True
	 if First is None: 
		return False
	 if (areIdentical(First, Second)): 
		return True
 	 return isSubtree(First.left, Second) or isSubtree(First.right, Second) 

First = Node(26) 
First.right = Node(3) 
First.right.left = Node(3) 
First.left = Node(10) 
First.left.left = Node(4) 
First.left.left.right = Node(30) 

Second = Node(10) 
Second.right = Node(6) 
Second.left = Node(4) 
Second.right.right = Node(50) 

if isSubtree(First, Second): 
	print ("Tree 2 is subtree of Tree 1")
else : 
	print ("Tree 2 is not a subtree of Tree 1")
```

![](https://github.com/VartikaChaudhary/Python-Data-Structure-Codes/blob/main/CBT.png)
