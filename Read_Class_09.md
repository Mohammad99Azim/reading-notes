## Dunder Methods

Dunder or magic methods in Python are the methods having two prefix and suffix underscores in the method name. Dunder here means “Double Under (Underscores)”.

These are commonly used for operator overloading. Few examples for magic methods are: __init__, __add__, __len__, __repr__ etc.

## Statistics in Python

### \_\_repr\_\_ magic method

\_\_repr\_\_ magic method is used to represent the instance of a class in string. 

When we try to print the object of a class the __repr__ method is implicitly invoked that returns a string

```
class ReprExample:
    def __init__(self, a, b, c):
        self.a = a
        self.b = b
        self.c = c
    def __repr__(self):
        return f"ReprExample(a={self.a}, b={self.b}, c={self.c})"
repr_instance = ReprExample(1, 2, 3)
print(repr_instance)
# Output
# ReprExample(a=1, b=2, c=3)

```

###\_\_len\_\_ magic method
\_\_len\_\_ magic method is used to find the length of the instance attributes. 

When we use len(instance), it returns the length of the instance attribute which is usually containers.

```
class LenExample:
    def __init__(self, item):
        self.item = item
    def __len__(self):
        return len(self.item)
len_instance = LenExample([1, 2, 3])
print(len(len_instance))
# Output: 3

```

### \_\_lt\_\_, \_\_gt\_\_, \_\_le\_\_, \_\_ge\_\_, \_\_eq\_\_, and \_\_ne\_\_ magic methods

Comparative operators can be used to compare between the object’s attributes. The available methods are \_\_lt\_\_,\_\_gt\_\_, \_\_le\_\_, \_\_ge\_\_, \_\_eq\_\_ , and \_\_ne\_\_ 

that performs less than, greater than, less than or equal to, greater than or equal to, equal to, and not equal to operations respectively.

```
class Comparison:
    def __init__(self, a):
        self.a = a
    def __lt__(self, object2):
        return self.a < object2.a
    def __gt__(self, object2):
        return self.a > object2.a
    def __le__(self, object2):
        return self.a <= object2.a
    def __ge__(self, object2):
        return self.a >= object2.a
    def __eq__(self, object2):
        return self.a == object2.a
    def __ne__(self, object2):
        return self.a != object2.a
a = Comparison(1)
b = Comparison(2)
print(
    a < b,
    a > b,
    a <= b,
    a >= b,
    a == b,
    a != b
)
# Output
# True False True False False True

```

### \_\_enter\_\_ and \_\_exit\_\_ magic methods

__enter__ and __exit__ methods are used along with the ‘with’ block in python. 
The ‘with’ block in python is used to open and close the file object or any other objects that have a close method.

```
class WriteFile:
    def __init__(self, file_name):
        self.file_name = file_name
        self.file = None
    def log(self, text):
        self.file.write(text+'n')
    def __enter__(self):
        self.file = open(self.file_name, "a+")
        return self    
    def __exit__(self, exc_type, exc_val, exc_tb):
        self.file.close()
with WriteFile(r"filename.txt") as log_file:
    log_file.log("Log Test 1")
    log_file.log("Log Test 2")
    
```

When the class is invoked with the file name ‘filename.txt’ the __enter__ method implicitly creates a text file. 
After executing the commands in the text file the __exit__ method is implicitly invoked to close the file object. 
In this way, we can use the __enter__ and __exit__ magic methods. These methods can also be used to open and close a database connection.

