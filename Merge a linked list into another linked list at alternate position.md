```python
class LinkedList(object): 
	def __init__(self): 
		self.head = None

	class Node(object): 
		def __init__(self, d): 
			self.data = d 
			self.next = None

	def push(self, new_data): 
		new_node = self.Node(new_data) 
		new_node.next = self.head 
		self.head = new_node 

	def merge(self, q): 
		p_curr = self.head 
		q_curr = q.head 

		while p_curr != None and q_curr != None: 
			p_next = p_curr.next
			q_next = q_curr.next
			q_curr.next = p_next
			p_curr.next = q_curr
			p_curr = p_next 
			q_curr = q_next 
		q.head = q_curr 

	def printList(self): 
		temp = self.head 
		while temp != None: 
			print(temp.data), 
			temp = temp.next
		print ('') 

llist1 = LinkedList() 
llist2 = LinkedList() 

llist1.push(3) 
llist1.push(2) 
llist1.push(1) 
print ("First Linked List:")
llist1.printList() 

llist2.push(8) 
llist2.push(7) 
llist2.push(6) 
print ("Second Linked List:")
llist2.printList() 

llist1.merge(llist2) 

print ("Modified first linked list:")
llist1.printList() 

print ("Modified second linked list:")
llist2.printList()
```

![](https://github.com/VartikaChaudhary/Python-Data-Structure-Codes/blob/main/MAP.png)
