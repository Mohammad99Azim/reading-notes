# Scope


## the LEGB Rule
 this Rule summarizing the Scope topic in general so what is LEGB statn for.
 
 The letters in LEGB stand for Local, Enclosing you can call it also (nonlocal) , Global, and Built-in.
 
 so let's start Explaining each on of them 
 
 ### 1-Local
 ```
 b = 10
 def func():
    a  = 0
    return a + 10
 ```
 
 In the above code, we define a variable ‘a’ in a function ‘func’. So, ‘a’ is local to ‘func’. Hence, we can read/write it in func, but not outside it.
 
 also we define a variable ‘b’ outside the function ‘func’ so we we can't read/write it in func.
 
 
 
 ### 2-nonlocal
 
 ```
 def red():
                a=1
                def blue():
                                b=2
                                print(a)
                                print(b)
                blue()
                print(a)
                
 ```


In this code, ‘b’ has local scope in Python function ‘blue’, and ‘a’ has nonlocal scope in ‘blue’ and as you see you can access ‘a’ in the ‘blue’ function

Of course, a python variable scope that isn’t global or local is nonlocal. This is also called the enclosing scope.



### 3-Global

 ```
 c = 0
 
 def red():
                a=1
                def blue():
                                b=2
                                print(a)
                                print(b)
                blue()
                print(a)
                
 ```

We declare a variable ‘c’ outside any other python Variable scope, this makes it global scope.

Consequently, we can read it anywhere in the program.


### 4-Built-in 

The built-in scope has all the names that are loaded into python variable scope when we start the interpreter.

For example, we never need to import any module to access functions like print() and id().



# BIG O notation

To calculate complexty to your program or functions you will need the big(O). so how we can do it

 NOTE !!!
 
 Big O notation doesn't show the time an algorithm will run. Instead, it shows the number of operations it will perform. 
 
 It tells you how fast an algorithm grows and  lets you compare it with others.

### O(1)

```
list = []
def printFirstElementOfList(list):
{
    print(f"First element of list = list[0]");
}

```
in the code above whatever was the long of the list the function will run in one step so it Big(1)



### O(log n)

```
def pick_just_half(listee):

    while len(listee) > 0:
       print (listee[(len(listee) // 2)] )
       listee = listee[0:len(listee) // 2]

pick_just_half(listee)

```
in the code above every step the list will be half so if it was have 1000 indexes the loop will end in  log(1000) to base 2 witch is 9 steps


### O(n)

```
def pring_all_list(my_list):
  for x in my_list:
    print(x)
    
```
in the code above every index will be printed so if we have a list of 1000 index we need a 1000 step to finish.

then if the  list have ‘n’ of the indexes we need a ‘n’ of steps then it will be O(n) 



### O(n^2)

```
def pring_all_list(my_list):
  for x in my_list:
    for y in my_list:
      print(x)
    
```
in the code above  if we have ‘n’ of indexes in the list every index will printed ( ‘n’ * ‘n’ ) withch make it O(n^2)






