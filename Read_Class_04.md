## Classes and Objects

Python is an object oriented programming language.

Almost everything in Python is an object, with its properties and methods.

A Class is like an object constructor, or a "blueprint" for creating objects.

#### Create Class
To create a class, use the keyword `` class: ``
```
class MyClass:
  x = 5
```

#### Create Objects
use the class named MyClass to create objects:
```
p1 = MyClass()
print(p1.x)

Output ==>  5
```

#### The __init__() Function

All classes have a function called __init__(), which is always executed when the class is being initiated.

Use the __init__() function to assign values to object properties, or other operations that are necessary to do when the object is being created

```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)

Output ==>  John
            36
```

#### The self Parameter

The self parameter is a reference to the current instance of the class, and is used to access variables that belongs to the class.

It does not have to be named self , you can call it whatever you like, but it has to be the first parameter of any function in the class

```
class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()

Output ==> Hello my name is John
```



## Thinking Recursively

A recursive function is a function defined in terms of itself via self-referential expressions.

This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

#### Advantages of using recursion

- A complicated function can be split down into smaller sub-problems utilizing recursion.
- Sequence creation is simpler through recursion than utilizing any nested iteration.
- Recursive functions render the code look simple and effective.

#### Disadvantages of using recursion

- A lot of memory and time is taken through recursive calls which makes it expensive for use.
- Recursive functions are challenging to debug.
- The reasoning behind recursion can sometimes be tough to think through.


## Pytest Fixtures and Coverage

we can use the fixtures in the pytest to avoied repeating ourselfs like if we have connection with data base and we want to test some queries we don't want in every 

test rewrite the connect line it will not be clear code and the connect every test will consumes resources the fixtures allowed us to connect one time and all test 

will run then you can clean up and close the connect.









