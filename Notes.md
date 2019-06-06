# Data Types Conversion
you can get the type of the variable with
```python
print (type(variable))
```

converts whatever that is inside () to a integer
```python
int()
```

converts whatever that is inside () to a float
```python
float()
```

converts whatever that is inside () to a string
```python(
str()
```

# Asking User for Input
to ask for numbers (float or integer) use:
```python
number = input("Enter number: ")
```

to ask for string use:
```python
name = raw_input("Enter name: ")
```

**if you are not sure what type of data you are dealing with, use the data type conversion to convert all values to the right type before continuing with the code. Example:**
```python
number = int(input("Enter number: "))
```

# Arithmetic (Maths) Operators
## Addition
```python
i = 2
j = 4
total = i + j
print(total)
```

## Subtraction
```python
i = 2
j = 4
total = j - 1
print (total)
```

## Multiplication
```python
i = 2
j = 4
total = i * j
print (total)
```

## Division
```python
i = 2
j = 4
total = j / i
print (total)
```
take note about the type of variable that you are dividing.
```python
i = 1
j = 2
print (i/j) # 0
print (float(i)/float(j)) # 0.5
```
**just to be on the safe side, if your answer needs to have decimal place, convert all numbers involved to float with float()**

## Power
```python
i = 2
j = 4
total = j**i
print (total)
```

## Modulus (Find remainder)
```python
i = 2
j = 5
remainder = 5%2
print (remainder)
```
Modulus is useful when you need to find out if a number is even number or odd. If any number divide by 2 does not produce a remainder, it is an even number.
```python
i = input("Enter number: ")
if (i%2 == 0):
    print ("This is an even number")
else:
    print("This is an odd number")
```

Order by which the arithmetic operators are processed
1. Anything in a bracket
2. Power
3. Multiplication, Division, Modulus
4. Addition, Subtraction

# Adding numbers to string (Concatenating)
adding numbers to another string
```python
string = "python"
print ("the string has " + str(len(string)) + " letters")
```
**__Take note, if you do not know the type of the variable, just add the str() around the variable just to be safe__**

# Range
a range is a quick way of generating a list of numbers
```python
range(5) = [0,1,2,3,4]
range(1,5) = [1,2,3,4]
range(0,5,2) = [0,2,4]
```

# Loop
Two scenarios that you need to do a loop
1. when you dont know how many times you need to do a certain action
2. when you need to do the same action for a lot of times

**Always remember, a loop always ask for when it should end**

Take note of variables that is declared (created) inside the loop, only when you are inside the loop, you get to see the variable, when you are outside the loop, you can no longer see the variable.

## Examples
i increase from 0 to 9, not including 10
```python
for i in range(10):
	print (str(i)) 
```
```python
i = 0
while (i < 10):
    print(str(i))
    i = i + 1
```

i increases from 1 to 9, not including 10
```python
for i in range(1,10):
	print(str(i))
```
```python
i = 1
while (i < 10):
    print(str(i))
    i = i + 1
```

i increases from 0 to 9, with a increment of 3 everytime
```python
for i in range (0,10,3):
    print(str(i))
```
```python
i = 0
while (i < 10):
    print(str(i))
    i = i + 3
```

## Getting every letter in a word
```python
word = "apple"
for i in range(len(word)):
    print (word[i])
```
```python
word = "apple"
i = 0
while i < len(word):
    print (word[i])
```

**the following works because a string is just a list of letters**
```python
word = "apple"
for letter in word:
    print (letter)
```

# Conditional Operators
Check if something is equal
```python
i = 2
j = 2
result = (i == 2)
print (result )
```
Check if something is not equal
```python
i = 2
j = 3
result = (i != j)
print (result)
```
check if something is more than
```python
i = 2
j = 3
result = (j > i)
print (result)
```
check if something is equal to or more than
```python
i = 3
j = 3
result = (j >= i)
print (result)
```
check if something is lesser than
```python
i = 2
j = 3
result = (i < j)
print (result)
```
check if something is equal to or lesser than
```python
i = 3
j = 3
result = (i <= j)
print (result)
```

# Decision Making
simply put, telling the computer what to do under what , where the conditions are either true or false
```python
if condition1:
    # do something
elif condition2:
    # do something
else:
    # do something
```
you are **allowed** to use `if` without `elif` and `else`

you are **allowed** to use `if` followed by a lot of `elif` and **optionally* ending with `else`

# Function
like how function stores value, a function can be thought of in a way that it stores a series of actions or calculations and output the results at the end of it. For example `len("words")` the function name is `len()` and the output is the length of the string in the `()`. Creating you own function will always follow this template:
```python
def function_name(parameter, parameter1, parameter2, ...):
    # do something
    return something
```
every function will have a function name and will return a value most of the time.
The parameters for your function is optional.
This is how `len` function will look like:
```python
def len(string):
    count = 0
    for letter in string:
        count = count + 1
    return count
``` 
# String Operations
## len() Method
this is a function used to check how many item there are in a list. And always remember that a string is also a list of letters, therefore `len(string)` will return (give you) the amount of letters in a string.
```python
names = ["Peter", "Jane", "Tom"]
print ("Number of names: " + str(len(names)))
```
## split() Method
this is used to seperate string by a delimiter (will be explained in the example later) and return to you a list of strings.
```python
string = "hello, world"
print (str(string.split())) # ["hello,", "world"]
print (str(string.split(","))) # ["hello", "world"]
```
in the second `print()`, `string.split(",")` has a comma in the `()` and that comma is the delimiter. Delimiter is just the string that the computer will "cut" at and give you the parts of the string in the form of a list. If `split()` without providing any delimiter as it's parameter, the delimiter is empty space by default.

## isalpha() Method
this function checks if the string is all alphabet and return `True` or `False`.
```python
name = "John"
number = "john123"
print (name.isalpha()) # True
print (name.isalpha()) # False
```

## startswith() endswith() Method
this function will check if the string starts with or the string ends with the parameter provided.
`name.startswith("H")` will check if the `name` string starts with the letter `"H"`. The parameter is **case sensitive**.
```python
name1 = "John"
print (name.startswith("J")) # True
print (name.startswith("j")) # False
print (name.endswith("n")) # True
print (name.endswith("N")) # False
```

## isdigit() Method
this function checks if the string contains only digits.
```python
number = "123"
string = "john123"
print (number.isdigit()) # True
print (string.isdigit()) # False
```

## lower() upper() Method
converts all alphabet in the string to upper or lower case.
```python
name = "John"
print (name.upper()) # JOHN
print (name.lower()) # john
print (name) # John
```
take note that the reason why the last `print()` still print out `"John"` instead of the lower case or upper case. This is because the variable `name` was never replaced with the upper or lower case version. If you want to permanently replace name to upper case, then you have to do this:
```python
name = name.upper()
```

## replace() Method
this function takes 2 parameters. the first one is the old text and the second one is the new text. it will replace all the old text in the string with the new text.
```python
name = "Johnathan"
name = name.replace('a', 'e')
print (name) # Johnethen
```

# count() Method
this function take one parameter. the function will then count the number of times the parameter appear in the string.
```python
name = "Johnathan"
print (name.count('h')) # 2
```


# List Operations
## len() Function
this is a function used to check how many item there are in a list. And always remember that a string is also a list of letters, therefore `len(string)` will return (give you) the amount of letters in a string.
```python
names = ["Peter", "Jane", "Tom"]
print ("Number of names: " + str(len(names)))
```

## append() Method
this is a function used to add item to the **back** of a list.
```python
names = ["Peter", "Jane", "Tom"]
names.append("John")
print(names) #["Peter", "Jane", "Tom", "John"]
```

## insert() Method
insert function takes 2 parameters, where the first parameter is position (technically called index) and the second parameter is value.
```python
names.insert(2, "John")
```
in this case, `"John"` is added to the list called `names` at position (or index) `2`. When a value is inserted into a certain position in the list, pushing the value at the current position back by 1.
```python
names = ["Peter", "Jane", "Tom"]
print (names[2]) # Tom
names.insert(2, "John")
print(names[2]) # John
```
in the above example `"Tom"` is pushed back from position 2 to position 3 as now `"John"` is at position 2.

## pop() Method
pop function removes the last value if no parameter is provided and return the last value. `pop(2)` will remove the value at position `2` and return the value at position `2`.
```python
random_list = [123, 'xyz', 'zara', 'abc'];
print ("List A : " + str(random_list.pop())) # abc
print ("random_list : " + str(random_list)) # [123, 'xyz', 'zara']
print ("List B : " + str(random_list.pop(0))) # zara
print ("random_list : " + str(random_list)) # ['xyz', 'zara']
```

## remove() Method
remove function removes the first item that has the same value as the parameter provided.
`names.remove("John")` will remove the first `"John"` that is in the list called `names`
```python
names = ["John", "Peter", "Jane", "Tom", "John"]
names.remove("John")
print (str(names)) # ["Peter", "Jane", "Tom", "John"]
```
