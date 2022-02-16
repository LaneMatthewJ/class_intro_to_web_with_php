# Python

Like javascript and php, python is an interpreted language. Python's syntax is also relatively different from everything we've seen so far. Unlike languages like javascript and php, python was designed for readability, and uses no curly braces like other languages. Python as a language can be used for writing command line scripts, servers, or even web pages (similar to how we write web pages with php and html). This introduction to python is to get you up to speed with the language before we jump into writing a web crawler. 



### Installation

Many, if not most computers come with python preinstalled. To ensure that python is installed on your machine, type: 

**Windows:**

```powershell
C:\Users\<YOUR USERNAME>python --version
```

**Mac:**

```bash
python --version
```

You should receive a message either says `command not found` OR something that looks akin to: 

```shell
Python 2.7.3 :: Continuum Analytics, Inc.
```

OR

```shell
Python 3.7.3
```



If you received a `command not found` error, go to [Python's webpage](https://www.python.org/) and download either Python 2.7, or the newest version of Python 3 (as of now, Python3's most up to date version is Python 3.7.4). For the sake of most, Python 2.7 is the standard version that already exists on computers, so we'll stick with that. If you've downloaded a more recent version, the code should not be that much different, however you may have to make minor changes on the code that can be found in the documentation. 



### Syntax

Python syntax is not entirely similar to other languages. We'll see more when we get to control flow and functions, but python is a language that, instead of enforcing scope through curly braces like javascript, php, etc., it uses indentation. Additionally, python's logical operators are different from those of other languages we've used up to now as well. 



#### Commenting

In order to comment things out in python, instead of using a `//` like in PHP and javascript, you can comment out code by placing a `#` in front of it. 



### Variables

To assign a value to a variable in python, it is as simple as declaring a variable by just naming it: 

```python
myVariable = "some value"
```

Two things to note here: 

	1. Notice that we did not declare a "var" or a data type before declaring the variable. Python lets users declare variables without using a reserved word. This is equally really nice, but also a potential problem (suppose you misspelled the variable, you've just created a brand new variable and not reassigned your old variable, leaving it as its old value). 
 	2. Python does not require semicolons! 



Also, python variables can also be reassigned at will to completely separate datatypes without a problem: 

```python
myVariable = 15
print(myVariable)

myVariable = "Hello World"
print(myVariable)
```



Python does not have "constants" per se. However, so long as conventions with capital letters are maintained, many are able to create variables and treat them as constants. Additionally, it is possible to create a function that returns a hard-coded so that the constant can act as a function. 

### Data Types

Python "has" datatypes, but, as we've seen above, those types are not confined to a specific variable name. As far as numerical types, there are three. We will, however, only cover two of the three (as the third is rarely used). 

#### Numerical Types: 

The numerical types for python are `int`, `float`, and `complex`. Just like most other languages, `int` stands for integers (such as 0, 1, 2, 3, 4, 5, etc), and `float` stands for a number with a decimal point (e.g. 0.1, 0.2, 0.0000003, etc). `complex` is used for imaginary numbers (which we won't be covering beyond noting that they exist).

Python lets you declare your variables with just a basic assignment like what was seen above. Types are implicitly allocated. To check the type of a variable, you can use the function `type()`, and pass the variable name in as a parameter: 

```python
num1 = 1
num2 = 2.4

print(num1)
print(num2)

print(type(num1))
print(type(num2))
```



#### Strings: 

Python strings are similar to strings in javascript: 

```python
stringOne = "I am a string with double quotes"
stringTwo = 'I am also a string, but with single quotes'

print(stringOne)
print(stringTwo)
```

It's also possible to create strings that span more than one line in your code: 

```python
whatIWant = '''Yo, I'll tell you what I want, what I really, really want
So tell me what you want, what you really, really want
I'll tell you what I want, what I really, really want
So tell me what you want, what you really, really want
I wanna, (ha) I wanna, (ha) I wanna, (ha) I wanna, (ha)
I wanna really, really, really wanna zigazig ah'''

print(whatIWant)
```

When you print out the above `whatIWant`, the string prints in the same format as how it was typed (i.e. the new lines in the string print as new lines).

Similar to other languages, strings are just character arrays. We'll cover arrays more later, however, it is worth noting that any character can be accessed by an index: 

```python
someString = "I am some string"
print(someString[3])
```

There are also supplied string functions, such as: 

- **upper**: You can change all of the letters in a string to upper case by using a dot function of `stringName.upper()`: 

- ```python
  someString = "I am some string"
  print(someString.upper())
  ```

- **lower**:  You can also change all letters in a string to lower case by using the dot function of `stringName.lower()`: 

- ```python
  someString = "I am some string"
  print(someString.lower())
  ```

- **replace**: In the case you need to replace a certain character or substring with another string, use `stringName.replace("original", "newString")`

- ```python
  someString = "I am some string"
  print(someString.replace("some", "a really cool"))
  ```

- **split**: It's very likely that you'll need to split a string to access elements of it as an array, you can do that by using split by choosing a delimiter (similar to PHP's explode method), like `stringName.split(' ')`:  

- ```python
  someString = "I am some string"
  print(someString.split(' ') # so we split on a space
  ```

- **strip**: Sometimes a string will have spaces around it, and to remove those spaces (without having to access the elements by array notation), you can clip the whitespaces off of the edge by using `stringName.strip()`:

- ```python
  someString = "          I am some string            "
  print(someString.strip())
  ```

- **length**:  To find the length of a string, use `len()` with the string as a parameter.

- ```python
  someString = "I am some string"
  print(len(someString))
  ```



String concatenation is much the same as in javascript: 

```python
stringOne = "I am a string with double quotes"
stringTwo = 'I am also a string, but with single quotes'

stringThree = stringOne + stringTwo
print(stringThree)
```



Printing variables mid-string can be very tricky. In order to interpolate a string with a variable, you need to place a `{}` in place of where the variable ought to show up in the string. In order to have a variable interpolated in the string, you need to use the `stringName.format()` function, where inside the format, the variable gets passed as a parameter: 

```python
name = "Matt"

stringName = "hello, my name is {}"
print(stringName.format(name))
```

It's also possible to use more than one variable, and to pass them in a comma separated values: 

```python
name = "Matt"
socialSecurityNumber = 1234561936


stringName = "hello, my name is {}, and my social security number is: {} "
print(stringName.format(name, socialSecurityNumber))
```



#### Casting

It might not always be the case that the type you have is the type you want. Sometimes you'll need to either convert a number from one type to another OR possibly you'll want to ensure that a specific number is a certain type when created: 

```python
someFloatingPoint = 6.3
integerNumber = int(someFloatingPoint)

floatingPointNumber = float(3)
otherInteger = int("3")

someString = str(someFloatingPoint)
otherString = str(5)

print(someFloatingPoint)
print(integerNumber)
print(floatingPointNumber)
print(otherInteger)
print(someString)
print(otherString)

print(type(someFloatingPoint))
print(type(integerNumber))
print(type(floatingPointNumber))
print(type(otherInteger)
print(type(someString))
print(type(otherString))
```



### Operators

Almost all operators of python are similar to all other languages, but there are a few differences that we haven't seen (primarily the logical operators):

#### Maths

Arithmetic operators in python are just like those of every other language. Addition `+`, subtraction `-`, multiplication `*`, division `/`, modulus `%`,  are the same as in every other language. Exponentiation `**` is the same as PHP, such that some variable as x^2 is represented as `x**2`. 

One addition to the maths we haven't seen yet is floor division.  It is possible you may see it in documentation. Regardless, floor division leaves out the decimal places to give an integer value. Suppose we divided 9 by 2, instead of receiving 4.5, we'd receive 4: 

```python
numeral = 9
divisor = 2

someVariable = 9 // 2
print(someVariable)
```

#### Logical

Unlike the languages we've looked at previously, logical operators are significantly different in python. Because python is a language written to be more human readable, instead of using operators like `&&` and `||`, we instead need to use the words themselves: 

Instead of doing: 

```javascript
trueAndTrue = True and True
trueAndFalse = True and False
falseAndFalse = False and False

trueOrTrue = True or True
trueOrFalse = True or False
falseOrFalse = False or False

notTrue = not True
notFalse = not False

print("true and true: ", trueAndTrue)
print("true and false: ", trueAndFalse)
print("false and false: ", falseAndFalse)

print("true or true: ", trueOrTrue)
print("true or false: ", trueOrFalse)
print("false or false: ", falseOrFalse)
print("not true: ", notTrue)
print("not false: ", notFalse)
```

While it is easy to see these working here, it is sometimes very easy to forget that `&&` and `||` do not work in python. If you find a syntax error in your code pointing to logical operators, it's likely because you've used one that works with a c-style language, and did not use the more human readable words used in python. 



### Functions

The more we get into functions, control flow and more advanced data structures, the differences of python become more apparent. Functions are defined in python with the keyword: `func`.  Let's take a look at a basic function that will add one to a number and then print it: 

```python
def addOneAndPrintSomething(something): 
 	newValue = something + 1
  print("The new value is ", newValue)
```

When calling this function, we call it just as if we'd call any other function: 

```python
someNumber = 5
addOneAndPrintSomething(someNumber)
```



In order to return data from a function, the return keyword is required: 

```python
def addOneAndPrintSomething(something): 
 	newValue = something + 1
  print("The new value is ", newValue)
  return newValue
```

And storying that data looks just like any other function: 

```python
someNumber = 5
newNumber = addOneAndPrintSomething(someNumber)

print("New number is: ", newNumber)
```



As a note concerning scoping, when using a function, just like other languages, if you declare a variable inside of a function, you will not be able to access it outside of the function. The following code will error out: 

```python
def addOneAndPrintSomething(something): 
 	newValue = something + 1
  print("The new value is ", newValue)
  return newValue


someNumber = 5
newNumber = addOneAndPrintSomething(someNumber)

print("Printing the value newValue from line 2: ", newValue)
```



### Control Flow

#### If/Else: 

If statements in python work just like any other languages, but the syntax is just slightly different (beyond using indentation as scoping), that is, you don't need to wrap the truth statement in parentheses like in other languages: 

```python
number = 10
if number > 7: 
  printString = "The number {} is greater than 7".format(number)
  print(printString)
```



If/Else statements work just the same: 

```python
number = 6
if number > 7: 
  printString = "The number {} is greater than 7".format(number)
  print(printString)
else: 
	printString = "The number {} is not greater than 7".format(number)
  print(printString)
```

Take note that the else has the same indentation as the if! 



Nested if/else statements are use the `elif` notation, as opposed to the `else if` notation: 

```python
number = 7
if number > 7: 
  printString = "The number {} is greater than 7".format(number)
  print(printString)
elif number == 7: 
	printString = "The number {} is 7!".format(number)
  print(printString)
else: 
	printString = "The number {} is less than 7".format(number)
  print(printString)
```



A note about scoping and python. It is possible to define a variable inside of an if/else block and access it outside of the block: 

```python
number = 10
if number > 7: 
  someValue = "I am a string assigned inside the if"

print(someValue)
```



#### Loops: 

Loops in python mostly work the same as in all other languages. While loops have a singular condition on which to stop. Like the if/elses before,  the conditions do not require parentheses around them: 

```python
counter = 0
while counter < 10: 
  print(counter)
  counter = counter + 1
```

For loops are a bit different, in that they act more as `for each` loops, instead.  As an example, suppose we have a string "some string". Because strings are really character arrays behind the scenes, we can iterate over each character in the string, such as: 

```python
for letter in "some string":
   print "Letter: ", letter
```

In the above code, we iterate over each specific letter in the array, and then print it out. This works the same for arrays, which we'll be getting into next (where we'll see more examples of how for loops work in python).



### Advanced Data Structures

#### Lists

In python, what are usually known as arrays are referred to as lists. These lists are quite literally just a group of variables that are stored inside of one variable name, and are accessed by a numerical index. For example, suppose I had a list of band members, such as the 'NSync. You can store all of those 'NSync into a single variable with the list syntax (which just so happens to look like every other language's array syntax) : 

```python
nSync = ['Justin Timberlake', 'Chris Kirkpatrick', 'Joey Fatone', 'Lance Bass', 'JC Chasez']
```

Now, suppose you wanted to loop over the backstreet boys to print out each of their names, you could do so by using either a while loop, like: 

```python
counter = 0
while counter < len(nSync):
  print(nSync[counter])
  counter += 1
```

The above works just fine, however, it's just as easy to loop over a list with the for, so that we can access each individual element as if it were a variable: 

```python
for syncedPerson in nSync:
  print(syncedPerson)
```



Lists in python do not have to all be of the same datatype either: 

```python
myList = ["Cool stuff", 23, "Neat!", 32.5, True ]

for item in myList: 
  print(item)
```

The ability to have more than one datatype in a list is very nice, however it can be extremely problematic when passing lists to and from functions. 



**NOTE:** While it's easy to see that we can loop over a list quite easily, it is good to know that if you are attempting to loop over an array and manipulate it, then you'll be in for a surprise if you wind up using a for each loop: 

```python
def printArr(arr):
  for elm in arr:
    print(elm)
    
myArray = ['a','b','c']

print("Now printing myArray:")
printArr(myArray)

print("Using for loop to 'change' myArray")
for element in myArray:
  element = 0
  print(element)
  
print("Now printing myArray:")
printArr(myArray)

print("Using while loop to change myArray")
counter = 0
while counter < len(myArray): 
  myArray[counter] = 0
  counter += 1
  
print("Now printing myArray:")
printArr(myArray)
```

So, what's happening in the above code is that we create an array, try to manipulate it with a `for` loop, but inside that for loop, what's happening is that we're actually reassigning a copy of the data, not the data itself. When we use the `while` loop, we are accessing the data directly, and can then overwrite it. 



Additionally, it should be noted that when passing lists to functions, the values are passed by reference: 

```python
def printArr(arr):
  for elm in arr:
    print(elm)

def doStuff(arr):
  counter = 0
  while counter < len(arr):
    arr[counter] = 0
		counter += 1
        
myArray = ['a','b','c']

printArr(myArray)
doStuff(myArray)
printArr(myArray)
```



#### Dictionaries

More advanced data structures like dictionaries also exist in python. Remember that dictionaries are just variables that house multiple data in them like arrays, but instead of being indexed with numbers, the data are accessed with key-value pairing: `containerName["key"] = "value"`.  Dictionaries are defined as: 

```python
myDictionary = {
	"key":"value", 
  "alsoAKey":"some different value", 
  "finalKey": "other value"
}
```

In `myDictionary` defined above, we have three elements, each one of those elements is accessed like: 

```python
print(myDictionary["key"])
print(myDictionary["alsoAKey"])
print(myDictionary["finalKey"])
```

Dictionaries are very powerful, but they're typically not used in the same way as are arrays. That being said, if it were required, it is possible to iterate over a dictionary, either the keys, values, or both: 

```python
for dictionaryItem in myDictionary: 
  print(dictionaryItem)
```

Notice that it prints only the dictionary key. To get the values you'd need to either use: 

```python
for dictionaryItem in myDictionary: 
  print(myDictionary[dictionaryItem])
```

OR you can loop over the values as: 

```python
for dictionaryItem in myDictionary.values(): 
	print(dictionaryItem)
```

Many libraries in python make heavy use of dictionaries, so it's very good to get used to dictionary syntax. One of those popular libraries is the [pandas](https://pandas.pydata.org/) library for data analysis and manipulation. 



#### Classes and Objects

Class definitions in python are a bit different than in other languages you may have already encountered, that is, beyond the difference in defining scope. Python constructors act a bit differently than constructors for other classes. Before we get to that though, it's worth noting that python classes don't necessarily need a construct (assuming that your class doesn't need to do any heavy lifting): 

```python
class HumanPerson: 
  name = "Matt"
  age = 31
  ssn = 123456789
```

To instantiate a class and then use it, you need only to invoke, then access the internal variables with the dot operator: 

```python
matt = HumanPerson()

mattsSocialSecurityNumber = matt.ssn
print("Matt's social security number is {}".format(mattsSocialSecurityNumber))
```

You can also modify the object's values by using simple assignments on the dot operators: 

```python
matt = HumanPerson()

print("Matt's original social security number is {}".format(matt.ssn))
matt.ssn = '000000001'
print("Matt's NEW social security number is {}".format(matt.ssn))
```



Not every class is as simple as one that just stores data. Suppose your class needs to do a bit more heavy lifting you'll need to create a constructor. Python constructors are significantly different from constructors in other languages, specifically in that they are not named the same name as the class with a function parameter, they instead are a function called `__init__`. Additionally, the very first parameter of this function must always be a reference to the instance calling the class. Typically, it's written as `self`, however, if you're familiar with c-style languages, think of `self` as python's version of `this`. Let's take a look at a more significant class: 

```python
class HumanPerson: 
  def __init__(self, name, age, ssn): 
		self.name = name
  	self.age = age
	  self.ssn = ssn
```

By writing the code as above, the values stored in `name`, `age`, and `ssn` are all passed in as parameters, such as: 

```python
matt = HumanPerson("Matt", 31, 123456789)

mattsSocialSecurityNumber = matt.ssn
print("Matt's social security number is {}".format(mattsSocialSecurityNumber))
```

Notice that we didn't pass in self? That can be a big trip up for a lot of folks. Just know that when defining your constructor function, you need to have a self, but when calling it, you only need to pass in the parameters that aren't `self`. 



As you've probably noticed, there's a def in front of our `__init__`.  That's the exact same way you'd define any other method in your class: 

```python
class HumanPerson: 
  def __init__(self, name, age, ssn): 
		self.name = name
  	self.age = age
	  self.ssn = ssn
    
  def doStuff(): 
    print("oh hello, from the object!")

 
matt = HumanPerson("Matt", 31, 123456789)
matt.doStuff()
```



Suppose you wanted to access class information, though. In order to do that, you'll need to pass in the `self` as a parameter. For example, suppose wen wanted a print method: 

```python
class HumanPerson: 
  def __init__(self, name, age, ssn): 
		self.name = name
  	self.age = age
	  self.ssn = ssn
    
  def doStuff(): 
    print("oh hello, from the object!")

  def printHuman(self): 
    print("{}'s social security number is {}".format(self.name, self.ssn))
```

By passing in self on `printHuman` we now have access to that specific instance's variables inside the class object. 