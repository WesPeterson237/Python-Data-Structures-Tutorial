
# Stack Problem Solution
There are different ways you can solve problems in programming. However, tih sis one of them by implementing push and pop with append() and pop():

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
            for x in range(amount):
                self.pancakes.append("Pancake")
            # FINISH IMPLEMENTING ##############
            print ("The chef has cooked " + str(amount) + " pancake(s).")
        
        def EatPancakes(self, amount):
            # START IMPLEMENTING ###############
            for x in range(amount):
                self.pancakes.pop()
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

