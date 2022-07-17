# Stack

## Introduction
A stack is essentially a data structure that operates on a Last in, First out basis.  This means that the first object we put into our stack will be the last out to come out again.  The best way to visualize this is by looking at a stack of pancakes as we cook them.  The pancake we put on the plate first will be the last pancake eaten.

<br>

## Implementation using Lists and Deque
### Lists
One of the easiest ways you can create a stack data structure is to use a list. If you are not familiar with lists. I recommend you get yourself familiar with them first.  To create a list and utilize it as a stack, we can simply create a list by using:

> userStack = [ ]   <font color="green"># This is our List that will be used as a stack</font>



### Deque
The other way we can implement a stackis to use the *"collections"* module. The *"collections"* module contains the *"deque"*. We can do so by stating the following:
> from collections import deque <br>
> userStack = deque ( )   <font color="green"># This is our deque collection that will be used as a stack</font>

As you can see from the code examples above, we are simply creating a list or a deque collection. From here we can use our commands that are stated in the next section of the tutorial.

<br>


## Push and Pop
The 3 main commands that we use when working with a stack is Push and Pop data. Refer to the table below for a description of each

<table>
    <tr>
        <th>Command</th>
        <th>Action</th>
        <th>Syntax</th>
    </tr>
    <tr>
        <td>Push</td>
        <td>Add an item/element to the "top" of the stack</td>
        <td>myStack.append("test")</td>
    </tr>
    <tr>
        <td>Pop</td>
        <td>Remove the "top" item/element of the stack</td>
        <td>myStack.pop()</td>
    </tr>
    
</table>

<br>

## Example

Now that we understand how to create a stack using two methods and how to manipulate that data with certain commands, let's put it to practice.  Refer to the following example code below.

> userStack = [ ]   <font color="green"># This is our List</font>
><br>
><br>
><font color="green"># This "pushes" values into our list</font><br>
> userStack.append("1") <br>
> userStack.append("2") <br>
> userStack.append("3") <br>
>
> print (userStack) <font color="green"># This results in printing out "['1','2','3']"</font> <br>
> userStack.pop() <font color="green"># This will remove, or "pop" the last item  added from the top of the stack</font> <br>
> print (userStack) <font color="green"># This results in printing out "['1','2']"</font>
>

As you can see, we begin our code by declaring a blank list named "*userStack*". This is an empty list which we then "push" data into out list by using the "append" command.  After adding the numbers, we then print out the stack to reveal the data inside is "['1','2','3']".  We then use the "pop" command to remove the top-most item from "*userStack*".  Rembember, because the number 3 was put in last, and we follow a last in first out basis, the number 3 will be removed.  This is why when we print out "*userStack*" afterwards, we receive the result of "['1','2']"

## Problem
Finish implementing the functions "CookPancakes" and "EatPancakes" of the a program that will allow the user to simulate cooking pancakes in a kitchen and placing them on a plate. The program will also simulate customers eating the pancakes from off the platter:


    class pancakeStack():

        pancakes = []

        def __init__(self):
            self.pancakes = ["Platter Base"]

        def __str__(self):
            print("")

            if len(self.pancakes) == 1:
                print ("-Empty Platter-")
                return (self.pancakes[0])

            for x in reversed(self.pancakes):
                print (x)
            print ("")
            return ("")

        def CookPancakes(self, amount):
            # START IMPLEMENTING ###############
            pass
            # FINISH IMPLEMENTING ##############
            print ("The chef has cooked " + str(amount) + " pancake(s).")
        
        def EatPancakes(self, amount):
            # START IMPLEMENTING ###############
            pass
            # FINISH IMPLEMENTING ##############
            print ("The customers have eaten " + str(amount) + " pancake(s).")



    platter = pancakeStack() # Creates an initial empty Pancake Platter

    platter.CookPancakes(5) # Cook 5 pancakes and add them to the platter
    print (platter) # Expected result:
                    # Pancake 5
                    # Pancake 4
                    # Pancake 3
                    # Pancake 2
                    # Pancake 1
                    # Platter 

    platter.EatPancakes(3) # Eat 3 pancakes from the top of the platter
    print (platter) # Expected result:
                    # Pancake 2
                    # Pancake 1
                    # Platter Base

    platter.CookPancakes(2) # Cook 2 pancakes and add them to the platter
    print (platter) # Expected result:
                    # Pancake 4
                    # Pancake 3
                    # Pancake 2
                    # Pancake 1
                    # Platter Base

    platter.EatPancakes(3) # Eat 3 pancakes from the top of the platter
    print (platter) # Expected result:
                    # Pancake 1
                    # Platter Base

    platter.EatPancakes(1) # Eat 1 pancake from the top of the platter
    print (platter) # Expected result:
                    # Empty Platter
                    # Platter Base

## Answer Key
- [Stack Solution](stack_answer.md)
<br>
<br>

## Home Page
- [Back to Home](Tutorial.md)
