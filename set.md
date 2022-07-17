# Set

## Introduction
What are sets? Sets are essentially a way to store multiple items into one variable. Uniquely, sets are one of the 4 base data type collections that are unorganized and unindexed. This means that the data inside the set variable can vary from case to case as well as the order of the data.
<br>
The common way to initalize a set is simply by the following:<br>
<br>
Initialize empty set: 

> mySet = set()


Initialize with data in the set:

> mySet = {"Pancakes", "Eggs", "Bacon"}

<br>

## Accessing a Set
You can access any item in a set by using a couple different methods.
Observe the block of code below. The code will check to see if the item is in the set. If it is it will let us know. If the item is not in the list, it will also let us know.

    mySet = {"Pancakes", "Eggs", "Bacon"}
    
    if ("Pancakes" in mySet):<br>
        print ("Item is in this list")<br>
    else:
        print ("Item is NOT in this list")

Now that we have looked at how to access items in the set, you might be wondering how we can manipulate the data. Unfortunately, one cannot change items in a set. You can only add or remove items. Read through the next section to learn how to accomplish this.
<br>


## Add and Remove
Upon initlizing a set, you cannot change the items inside by statement.  Instead, you must use Add and Remove commands. Using our example above in the previous section, this is how we would add items to our set:

### Add Example
    mySet = {"Pancakes", "Eggs", "Bacon"}

    mySet.add("Sausage")

    print (mySet)
    # Expected output: {'Sausage', 'Pancakes', 'Eggs', 'Bacon'}

### Remove Example
    mySet = {"Pancakes", "Eggs", "Bacon"}

    mySet.remove("Bacon")

    mySet.remove("Eggs")

    print (mySet)
    # Expected output: {'Pancakes'}

As you can tell from the code above, the first example adds items to the list while the bottom example removes them.  After doing each operation, we print out the result. Again, we find a cheat sheet/table that reiterates what we have gone over.

<table>
    <tr>
        <th>Command</th>
        <th>Action</th>
        <th>Syntax</th>
    </tr>
    <tr>
        <td>Add</td>
        <td>Add an item/element to the set.</td>
        <td>mySet.add(-item-)</td>
    </tr>
    <tr>
        <td>Remove</td>
        <td>Remove an item/element from the set.</td>
        <td>mySet.remove(-item-)</td>
    </tr>
</table>
<br>


## Problem
For this exercise, we have a class named ItemSet that has some built in functions. Your job is to implement the functions properly so they function as intended. 3 functions will need to be worked on. 

**Contains()** - This function must check to see if the set has that item within it. Then notify the user of the result

**AddItem()** - This function must add an item to the list based on the parameter given. If there is a duplicate found, notify the user so that they are aware.

**RemoveItem()** - Delete an item from the list based on the parameter passed. If the item being requested is not in the list. Notify the user so they are aware

The tests for the program are written below the class. First section of the test will add values to the set. The second section will test the functions. Hopefully you ahve placed good statements that report information back to the user. 

    class ItemSet():

        items = set()

        def __init__(self):
            self.items = set()

        def __str__(self):
                return ("\nSET - " + str(self.items))

        def Contains(self, query):
            # START IMPLEMENTING ###############
            pass
            # FINISH IMPLEMENTING ##############

        def AddItem(self, itemToAdd):
            # START IMPLEMENTING ###############
            pass
            # FINISH IMPLEMENTING ##############

        def RemoveItem(self, itemToRemove):
            # START IMPLEMENTING ###############
            pass
            # FINISH IMPLEMENTING ##############

    userSet = ItemSet()

    print("\n-ADDING ITEMS-")
    print("********************")
    userSet.AddItem(5)
    userSet.AddItem("Wes")
    userSet.AddItem(17)
    userSet.AddItem("Peterson")
    userSet.AddItem(45.8)
    print (str(userSet) + "\n") # Expected set result: {5, 'Wes', 45.8, 17, 'Peterson'}

    print("\n-TESTING THE LIST-")
    print("********************")
    userSet.Contains(5)
    userSet.AddItem(5)
    userSet.AddItem ("@@@")
    userSet.RemoveItem("@@@")
    userSet.RemoveItem(7)
    userSet.RemoveItem(5)
    userSet.Contains(5)
    userSet.RemoveItem(45.8)
    userSet.RemoveItem(17)

    print (str(userSet) + "\n") # Expected set result: {'Wes', 'Peterson'}


<br>

## Answer Key
- [Set Solution](set_answer.md)
<br>
<br>

## Home Page
- [Back to Home](Tutorial.md)

