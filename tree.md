# Tree

## Introduction
Binary trees are datastructures comprised of "Nodes". Each Node will link to no more than 2 other nodes. They will do so depending on the value inside that node.  We often visualize and use nodes with integers and numbers:

The following example is a Binary Tree. Refer to this example throughout the rest of our reading. 

               9                    Root node:          9
            /     \                 Leaf node(s):       2, 4, 7, 11
           3       10                
          / \        \
         2   5        12
            / \      /
           4   7    11

In real world programming, Binary trees are used for search operations such as sorting, traversing, or deleting data in a more efficient matter.
<br>
<br>

## Roots and Leaves
### Roots
The "Root" of a node refers to the top most node in the entire binary tree. In the preceeding example above, we see that our node "9" would be referred to as the root node. You almost have to imagine flipping the tree upside down to view it as an actual tree that sprouts outward.
<br>


### Leaves
The "Leaves" of our tree is essentially and node that only connects to one other node. As mentioned before, imagine flipping the tree upside down so the Root is on the bottom and sprouts upward.. Our "Leaf" nodes would be "2, 4, 7, and 11"
<br>

### Parent and Child
"Parent" nodes are essentially and node that is not a root or leaf and has connected nodes branching from it.  "Child" nodes are the nodes branching off of the parent nodes. So from our above example, we can see that node "3" is a parent node that connects 2 other nodes below it. Nodes "2" and "5" are the child nodes of node "6".
<br>
<br>

## Constructing a Tree
Now that we have learned the different parts of a binary tree and what is called what, it is crucial that we now discuss how to set up a binary tree and how it is constructed.

The first thing we begin with is our root. And this will be whatever the first value passed in is.  The next number to be placed in will then compare itself to the root If it is larger than the root, it will move to the right of the node. If it is smaller, it will move to the left of the node. This system repeats over and over with each node passed in. the node will keep moving to the right or left of the node until it finds a blank/empty space. See the following section to see our original example build step by step.
<br>
<br>


## Example
Let's say we recieve a data set of the following numbers: (9, 10, 3, 5, 2, 4). 
We will being with or root and following two numbers.

Our tree now looks like this:

            9
          /   \
         3     10

If we were to get another number as "5". It would follow this path.

- 5 is less than our root 9 and moves down to the next number: 3
- 5 is greater than 3, and then moves to the right of "3"

Our tree now looks like the following:

            9
          /   \
         3     10
          \
           5

Let's add a couple more numbers to demonstrate this:

- Next number is 2
- 2 is less than our root 9 and moves to the next number: 3
- 2 is less than node 3, and then moves to the left of "3"
- Next number is 4
- 4 is less than our root 9 and moves to the next number: 3
- 4 is greater than our node of 3, and moves down to the next number: 5
- 4 is less than 5, and is then moved to the left of 5

Our tree now looks like this:

            9
          /   \
         3     10
       /   \
      2     5
           /
          4
<br>

## Problem
You are going to be given the following Data Set: (32, 17, 3, 56, 33, 6, 10, 25, 67, 82, 77)

Place the correct numbers into the correct slots. The branches ahve already been built for you. (Read the data set from left to right. "32" is the first number.)

                                    []
                                /        \
                              []          []
                             /  \        /  \
                            []   []     []   []
                           / \                 \
                          []  []                []
                             / \               /
                            []  []            []
<br>

## Answer Key
- [Tree Solution](tree_answer.md)

