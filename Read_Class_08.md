# List Comprehensions
List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.

Example:

Based on a list of fruits, you want a new list, containing only the fruits with the letter "a" in the name.

Without list comprehension you will have to write a ``for`` statement with a conditional test inside:

```
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)
```

With list comprehension you can do all that with only one line of code:

```
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)

```

so the Syntax is:

```
newlist = [expression for item in iterable if condition == True]
```


# PySnooper

### PySnooper - Never use print for debugging again

PySnooper is a debugger. You will use instade of put a print statment to debug your code 

### How to use it 

We're writing a function that converts a number to binary, by returning a list of bits. 

Let's snoop on it by adding the ``@pysnooper.snoop()`` decorator:

```
import pysnooper

@pysnooper.snoop()
def number_to_bits(number):
    if number:
        bits = []
        while number:
            number, remainder = divmod(number, 2)
            bits.insert(0, remainder)
        return bits
    else:
        return [0]

number_to_bits(6)

```
The output to stderr is:

![output image](https://warehouse-camo.ingress.cmh1.psfhosted.org/a0926851398042fbc70a0622bc368f49cb14fa86/68747470733a2f2f692e696d6775722e636f6d2f5472463356566a2e6a7067)


Or if you don't want to trace an entire function, you can wrap the relevant part in a with block:

```
import pysnooper
import random

def foo():
    lst = []
    for i in range(10):
        lst.append(random.randrange(1, 1000))

    with pysnooper.snoop():  #### Using with
        lower = min(lst)
        upper = max(lst)
        mid = (lower + upper) / 2
        print(lower, mid, upper)

foo()
```

which outputs something like:

```
New var:....... i = 9
New var:....... lst = [681, 267, 74, 832, 284, 678, ...]
09:37:35.881721 line        10         lower = min(lst)
New var:....... lower = 74
09:37:35.882137 line        11         upper = max(lst)
New var:....... upper = 832
09:37:35.882304 line        12         mid = (lower + upper) / 2
74 453.0 832
New var:....... mid = 453.0
09:37:35.882486 line        13         print(lower, mid, upper)
Elapsed time: 00:00:00.000344

```

So it will trace your code line by line and show you every things happening












