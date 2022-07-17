
# Tree Problem Solution

## Problem 1:

Data Set - (32, 17, 3, 56, 33, 6, 10, 25, 67, 82, 77, 2, 8)

Solution:


                                    32
                                /        \
                              17          56
                             /  \        /  \
                            3    25     33   67
                           / \                 \
                          2   6                 82
                             / \               /
                            8   10            77


## Problem 2:

Solution:

    class Node:
        def __init__ (self, data):
            self.left = None
            self.right = None
            self.data = data

        def insert (self, data):
            if self.data is None:
                self.data = data
            else:
                if data < self.data:
                    if self.left is None:
                        self.left = Node(data)
                    else:
                        self.left.insert(data)
                elif data > self.data:
                    if self.right is None:
                        self.right = Node(data)
                    else:
                        self.right.insert(data)

        def display_tree(self, *args):

            for ar in args:
                self.data = ar

            if self.data is not None:
                print (self.data)
                
                if self.left is not None:
                        self.left.display_tree(self.left.data)
                if self.right is not None:
                        self.right.display_tree(self.right.data)
                else: 
                    return
            else:
                return




    tree = Node(5)
    tree.insert(4)
    tree.insert(3)
    tree.insert(7)
    tree.insert(1)
    tree.insert(10)
    tree.insert(11)
    tree.insert(2)
    tree.insert(15)
    tree.insert(6)

    tree.display_tree()

    """ Expected output (NOTE: Output may be in a slightly different order depending on how you implement the "insert" function)
    5
    4
    3
    1
    2
    7
    6
    10
    11
    15 """


<br>
<br>

## Home Page
- [Back to Home](Tutorial.md)
