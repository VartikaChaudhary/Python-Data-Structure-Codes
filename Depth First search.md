```python

from collections import defaultdict
 
class Tree:
 
    def __init__(self):
        self.tree = defaultdict(list)
 
    def addNode(self, u, v):
        self.tree[u].append(v)
 
    def DFSVisited(self, v, visited):
        visited.add(v)
        print(v, end=' ')
 
        for neighbour in self.graph[v]:
            if neighbour not in visited:
                self.DFSVisited(neighbour, visited)
 
    def DFS(self, v):
        visited = set()
        self.DFSVisited(v, visited) 

n = Tree()
n.addNode(0, 1)
n.addNode(0, 2)
n.addNode(1, 2)
 
print("Following is DFS from (starting from vertex 1)")
n.DFS(1)
print("\n")
```

![Output of Depth First Search Code](https://github.com/VartikaChaudhary/Python-Data-Structure-Codes/blob/main/DFS.png)
