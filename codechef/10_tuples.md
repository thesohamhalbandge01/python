## Tuples

A tuple is an ordered collection of elements, which can be of different types.  
Tuples are similar to lists, but they are immutable (cannot be changed).

### Tuple creation
```python
my_tuple = (1, "hello", 3.14)
```
- Tuples are created using parentheses `()`.
- Elements are separated by commas.

### Accessing elements of a tuple
```python
my_tuple = (1, "hello", 3.14)
print(my_tuple[0])  # Access the first element
```
- Indexing starts from `0`, similar to lists.
- Elements are accessed using square brackets `[]`.

### Tuple characteristics
- **Ordered**: Elements in a tuple are ordered, meaning they have a specific position and can be accessed using indexing.
- **Immutable**: Tuples cannot be modified or changed once created.
- **Allows Duplicates**: Tuples can contain duplicate elements.

### List as part of a tuple
A tuple can hold elements of various types, including lists, which makes tuples versatile for storing a mix of different data structures.

#### Example:
```python
my_list = [1, 2, 3]
my_tuple = ("Alice", 30, my_list)

print("Tuple:", my_tuple)   # Output - Tuple: ('Alice', 30, [1, 2, 3])
```

### Tuple unpacking
Tuple unpacking, also known as **tuple destructuring**, is a feature in Python that allows you to assign the elements of a tuple to individual variables in a single assignment statement.  
This makes it easy to extract and work with the individual elements of a tuple.

#### Example:
```python
my_tuple = (1, 'hello', 3.14)

# Unpack the tuple into separate variables
a, b, c = my_tuple

# Print the unpacked variables
print("a:", a)  # Output: a: 1
print("b:", b)  # Output: b: hello
print("c:", c)  # Output: c: 3.14
```

### Length and count of elements in a tuple
For tuples, `len()` returns the number of elements.

#### Example:
```python
my_tuple = (1, 2, 3, 4, 5)
print("Length of the tuple:", len(my_tuple))  # Output: Length of the tuple: 5
```

For tuples, `count()` allows you to count the occurrences of a specified value.

#### Example:
```python
my_tuple = (1, 2, 2, 3, 2, 4, 5, 2)
print("Number of occurrences of 2:", my_tuple.count(2))  # Output: Number of occurrences of 2: 4