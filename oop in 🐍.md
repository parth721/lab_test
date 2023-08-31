## We have the basic idea of class & object. Let's start

1. create a class:
  `class Hat:`

2. create an object(hat) :
  `hat = Hat()`

3. let's call the sort method(func.)
  `hat.sort("harry")`

5. Now lets define the attributes & methods inside class :
   ```
   def __init__(self):
       self.house = ["red", "blue", "green"]
   def sort(self, name):
      house = random.choice(self.house)
      print(name, "is in " house)
    ```
   
6. so the final code looks like 
 ```
 import random

 class Hat: 
    def __init__(self):
       self.house = ["red", "blue", "green"]
    def sort(self, name):
       house = random.choice(self.house)
       print(name, "is in " house)

 hat = Hat()

 hat.sort("harry")
```

@classmethod : a func.  that operate on a class itself rather than on instance.

@instancemethod : a function within a class that operate on an instance of that class. It takes the instance itself ('self') as an argument. Allowing it to access & modify instance specific attribute's behavior.

@staticmethod : a function that is defined within class but it doesn't have access to the instance or class . They can be called as `result = Math.add_num(5,7)`

properties : They allow you to define methods that are used to get, set, delete values of specific attributes.

decorator : Python tool used to modify the behavior of the function.

constructor : A special fuction that modify the behavior of the function.

why its used 
if__name__(self) == "__main__" 
    main() 
