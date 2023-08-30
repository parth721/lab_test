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

if __name__ == "__main":
 
```
