# Set Problem Solution
This is one way we can implement the functions below. By using ".add" and ".remove" We can fulfill the roles.  As for the "Contains" Function, we can simply uery to see if the item is in the list.  Of course, Sets do not allow duplicates.  So we want to notify the user if they attempt to enter in a duplicate.

    class ItemSet():

        items = set()

        def __init__(self):
            self.items = set()

        def __str__(self):
                return ("\nSET - " + str(self.items))

        def Contains(self, query):
            if query in self.items:
                print("Yes, " + str(query) + " is in this set.")
            else:
                print("No, " + str(query) + " is NOT in this set.")

        def AddItem(self, itemToAdd):
            if (itemToAdd not in self.items):
                self.items.add(itemToAdd)
                print (str(itemToAdd) + " added to set.")
            else:
                print (str(itemToAdd) + " is already in the set. No duplicates allowed.")

        def RemoveItem(self, itemToRemove):
            if itemToRemove in self.items:
                self.items.remove(itemToRemove)
                print (str(itemToRemove) + " removed from the set.")
            else:
                print(str(itemToRemove) + " is not in this set. Nothing to remove.")

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

