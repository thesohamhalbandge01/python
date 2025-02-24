## Creating a Variable

### Numeric Variables - Hold integers and decimal values
```python
age = 25 # integer
temperature = 98.6 # float 
```

### String Variables - Stores a sequence of characters enclosed in single or double quotes
```python
name = "John Doe"
message = 'Hello, world!'
```

### Boolean Variables - Only hold the values True and False
```python
is_true = True
is_false = False
```

### List Variables - Stores a collection of items, which can be of different types.
```python
numbers = [1, 2, 3, 4, 5]
fruits = ['apple', 'banana', 'orange']
```

### Tuple Variables
```python
coordinates = (10, 20)
```

### Dictionary Variables
```python
person = {'name': 'Alice', 'age': 30}
```

### Set Variables
```python
unique_numbers = {1, 2, 3}
```

### None Variable
```python
empty_value = None
```

## Properties of Variables

```python
age = 25
print(age) # 25

age = 26
print(age) # 26
```

## Rules for Variable Names

- A variable name can only contain alphabets, numbers, and underscores (i.e., A-Z, a-z, 0-9, and `_`).
- A variable name cannot start with a number.
- A variable name cannot have spaces in between.
- Variable names are case-sensitive (`age`, `Age`, and `AGE` are three different variables).

## Type Conversion

### Implicit Conversion
```python
x = 7
x = x / 2
print(x) # Output: 3.5
```

### Explicit Conversion
```python
num = '12'
num = int(num)
num = num + num  # if num='12' then num + num = 1212
print(num) # 24
```

## Check Type of Variable

```python
a = 5
print(type(a)) # Output: <class 'int'>
```