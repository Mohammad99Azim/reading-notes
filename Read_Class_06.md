## Random Module

It use to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc...

### Random functions
- Randint
   ```
   import random
   print random.randint(0, 5)
   
   output => random integer number from 1 to 5
   
   ```
 - Choice
    ```
    import random
    my_list = ["one" , 2 , 3 , "string" , None]
    ss = random.choice(my_list)
    print(ss) 
    
     output => will print one index randomly
    ```
    
 - Shuffle
    The shuffle function, shuffles the elements in list in place, so they are in a random order.
    ```
    from random import shuffle
    x = [1,2,3,4,5]
    shuffle(x)
    print(x)
    
     output =>  will print the list in different ordere each time will sort the indexes randomly
    ```
    
    

## Risk Analysis

 A risk analysis performed during software testing helps to identify areas where software flaws could result in serious issues in production. By identifying areas of concern early, developers are able to proactively remediate and reduce the overall risk of a production defect

 Implementing risk analysis in software testing typically requires a detailed evaluation of the source code to identify how it interacts with other components of a complete application. This evaluation looks at the various code components and maps how the code interacts.

    
## Test Coverage   

Test coverage is defined as a metric in Software Testing that measures the amount of testing performed by a set of test. It will include gathering information about which parts of a program are executed when running the test suite to determine which branches of conditional statements have been taken.

In simple terms, it is a technique to ensure that your tests are testing your code or how much of your code you exercised by running the test.



## Big O Notation
Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity. 

- Big O (O()) describes the upper bound of the complexity.
- Omega (Ω()) describes the lower bound of the complexity.
- Theta (Θ()) describes the exact bound of the complexity.
- Little O (o()) describes the upper bound excluding the exact bound.

![](https://www.freecodecamp.org/news/content/images/2021/06/1_O-dcXbYXojkAPEnDuVZMvA.png)



- O(1) has the least complexity

- O(log(n)) is more complex than O(1), but less complex than polynomials

- O(n^2) Complexity of polynomials increases as the exponent increases 

- O(2^n) Exponentials have greater complexity than polynomials as long as the coefficients are positive multiples of n

- O(n!) Factorials have greater complexity than exponentials

![](https://www.freecodecamp.org/news/content/images/2021/06/1_KfZYFUT2OKfjekJlCeYvuQ.jpeg)








