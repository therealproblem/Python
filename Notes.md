# Data Types Conversion
converts whatever that is inside () to a integer
```python
int()
```

converts whatever that is inside () to a float
```python
float()
```

converts whatever that is inside () to a string
```python
str()
```


# Asking User for Input
to ask for numbers (float or integer) use:
```python
input("Enter number: ")
```

to ask for string use:
```python
raw_input("Enter string: ")
```

# Loop
Two scenarios that you need to do a loop
1. when you dont know how many times you need to do a certain action
2. when you need to do the same action for a lot of times

***Always remember, a loop always ask for when it should end***

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

getting every letter in a word
```python
word = "apple"
for letter in word:
    print (letter)
```
```python
word = "apple"
i = 0
while i < len(word):
    print (word[i])
```
