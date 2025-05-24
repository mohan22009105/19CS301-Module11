# Exp.no: 54
## DOUBLE LINKED LIST-2

### AIM

To type a python function to insert elements at the beginning of the doubly linked list. 

### ALORITHM 

1. Start the program.

2. Create a Node class with data, next (nref), and previous (pref) links.

3. Create a DoublyLinkedList class with start_node set to None.

4. To insert in an empty list:
   Create a node and assign it to start_node if the list is empty.

5. To insert at the start:
   Create a new node.
   Point its nref to current start_node.
   Point current start_node.pref to the new node.
   Update start_node to the new node.

6. print the list:

7. Traverse and print the list.

8. Terminate the program.
   
### PROGRAM

```
class Node:
    def __init__(self, data):
        self.item = data
        self.nref = None
        self.pref = None

class DoublyLinkedList:
    def __init__(self):
        self.start_node = None

    def insert_in_emptylist(self, data):
        if self.start_node is None:
            new_node = Node(data)
            self.start_node = new_node
        else:
            print("list is not empty")
            
    def insert_at_start(self, data):
        if self.start_node is None:
            new_node=Node(data)
            self.start_node=new_node
            print("node inserted")
            return
        new_node=Node(data)
        new_node.nref=self.start_node
        self.start_node.pref=new_node
        self.start_node=new_node
        
    def traverse_list(self):
        if self.start_node is None:
            print("List has no element")
            return
        else:
            n = self.start_node
            while n is not None:
                print(n.item , " ")
                n = n.nref
                
new_linked_list = DoublyLinkedList()
new_linked_list.insert_in_emptylist(40)
new_linked_list.insert_at_start(30)
new_linked_list.insert_at_start(20)
new_linked_list.insert_at_start(10)
new_linked_list.traverse_list()
```

### OUTPUT

![image](https://github.com/user-attachments/assets/12297de1-a2ac-4e1f-84a2-e130ef23110e)

### RESULT
Thus the python program was successfully created.
