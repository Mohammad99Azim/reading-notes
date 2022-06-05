# Exceptions
An exception is an event, which occurs during the execution of a program that disrupts the normal flow of the program's instructions.

In general, when a Python script encounters a situation that it cannot cope with, it raises an exception. An exception is a Python object that represents an error.

### Handling an exception

Raising an Exception: This is some ways to Rais an Exception

1- Using raise 
```
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
```
2- AssertionError 
```
x = 1
y = 0
assert y != 0, "Invalid Operation" # denominator can't be 0
print(x / y)
```

3- try and except
```
try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")
```

4- try, except and else
```
try:
    statements # statements that can raise exceptions
except:
    statements # statements that will be executed to handle exceptions
else:
    statements # statements that will be executed if there is no exception
```

# Read & Write Files in Python
File handling is an important part of any web application.
Python has several functions for creating, reading, updating, and deleting files.

1- Open
To open file we need to use open function


The open() function takes two parameters; filename, and mode.

There are four different methods (modes) for opening a file:
```
"r" - Read - Default value. Opens a file for reading, error if the file does not exist

"a" - Append - Opens a file for appending, creates the file if it does not exist

"w" - Write - Opens a file for writing, creates the file if it does not exist

"x" - Create - Creates the specified file, returns an error if the file exists
```


In addition you can specify if the file should be handled as binary or text mode
```
"t" - Text - Default value. Text mode

"b" - Binary - Binary mode (images)
```

** Always make sure you close the file after finish work with it **


2- Read or Write

To read from file use read() function or readline()

```
# 
f = open("D:\\myfiles\welcome.txt", "r")
print(f.read())


# Return the 5 first characters of the file:
f = open("demofile.txt", "r")
print(f.read(5))


# Read one line of the file:
f = open("demofile.txt", "r")
print(f.readline())


To write or append to file use the write() function 

"a" - Append - will append to the end of the file

"w" - Write - will overwrite any existing content

```
Write in file
```
# will add to the end of the text in the file
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()

# will delete the content and write the text in the write function
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()

```

### Create a New File
To create a new file in Python, use the open() method, with one of the following parameters:

"x" - Create - will create a file, returns an error if the file exist

"a" - Append - will create a file if the specified file does not exist

"w" - Write - will create a file if the specified file does not exist

### Close

to close the file use the close() function


## Things I want to know more about 
1) Read file with images 
2) when we should use file in project and when we shouldn't





