

```python
class Node(object):
    def __init__(self, value):
        self.value=value
        self.leftnode=None
        self.rightnode=None

class bst:
    def __init__(self):
        self.root=None
        
    def append(self, value):
        if self.root==None:
            self.root=Node(value)
        else:
            self.insertnode(value, self.root)
            
               
    def insertnode(self, value, node):
        if value<node.value:
            if node.leftnode!=None:
                self.insertnode(value, node.leftnode)
            else:
                node.leftnode=Node(value)
        else:
            if node.rightnode!=None:
                self.insertnode(value, node.rightnode)
            else:
                node.rightnode=Node(value)
            
    def getminvalue(self):
        if self.root!=None:
            return self.getminnode(self.root)

    
    def getminnode(self,node):
        if node.leftnode!=None:
            return self.getminnode(node.leftnode)
        return node.value
    
tree=bst()
tree.append(50)
tree.append(40)
tree.append(45)
tree.append(60)
tree.append(55)
tree.append(65)


tree.getminvalue()
            
        
               
        
        
```




    40


