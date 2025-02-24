## Dictionary

A dictionary is an unordered collection of data in a key-value pair format.  
Each value in a dictionary is accessed using a unique key.

### Creating a dictionary
```python
my_dict = {"key1": "value1", "key2": "value2", "key3": "value3"}
```
- Dictionaries are created using curly braces `{}`.
- Key-value pairs are separated by colons `:` and elements are separated by commas.

### Accessing values
Values in a dictionary are accessed using keys.

```python
my_dict = {"name": "Alice", "age": 30}
print(my_dict["name"])  # Access the value for the key "name"
```

### Dictionary characteristics
- **Order**: Unlike sequences (e.g., lists, tuples), dictionaries are not ordered till Python versions older than 3.7. After v3.7, they are ordered.
- **Mutable**: Dictionaries can be modified (items can be added, removed, or modified).
- **Unique**: Keys in a dictionary must be unique.

### Modifying a dictionary
#### Adding items to a dictionary
To add a new key-value pair to a dictionary, you simply assign a value to a new key.

```python
my_dict = {"name": "Alice", "age": 30}
my_dict["location"] = "New York"
```

#### Modifying items in a dictionary
To modify an existing value associated with a key in a dictionary, you can simply reassign a new value to that key.

```python
my_dict = {"name": "Alice", "age": 30}
my_dict["age"] = 31  # Update the value for the key "age"
```

### Removing items from a dictionary
Removing items from a dictionary involves deleting key-value pairs. Dictionaries provide different methods to remove elements based on keys.

#### `del`: Remove a specific key-value pair
```python
my_dict = {"name": "Alice", "age": 30}
del my_dict["age"]  # Remove the key "age" and its corresponding value
```

#### `pop()`: Remove a specified key and return its value
```python
my_dict = {"name": "Alice", "age": 30}
removed_age = my_dict.pop("age")  # Remove the key "age" and retrieve its value
```

#### `clear()`: Remove all key-value pairs
```python
my_dict = {"name": "Alice", "age": 30}
my_dict.clear()  # Clear all key-value pairs
```

### Iterate over a dictionary
Iterating over a dictionary in Python allows you to access and process its elements, which are key-value pairs.

#### Iterating Over Keys
By default, iterating over a dictionary iterates over its keys.
```python
my_dict = {"name": "Alice", "age": 30, "location": "New York"}
for key in my_dict:
    print("Key:", key)
```

#### Iterating Over Values
```python
my_dict = {"name": "Alice", "age": 30, "location": "New York"}
for value in my_dict.values():
    print("Value:", value)
```

#### Iterating Over Key-Value Pairs
To iterate over key-value pairs, you can use the `items()` method.
```python
my_dict = {"name": "Alice", "age": 30, "location": "New York"}
for key, value in my_dict.items():
    print("Key:", key, ", Value:", value)
```

### Key existence in a dictionary
It's important to determine whether a particular key exists before attempting to access its associated value to avoid potential errors.

#### Using `in` to check if a key exists
```python
my_dict = {"name": "Alice", "age": 30}
print("name" in my_dict)  # Output: True
print("location" in my_dict)  # Output: False
```

#### Using `get()` to retrieve values safely
```python
my_dict = {"name": "Alice", "age": 30}
print(my_dict.get("name"))  # Output: Alice
print(my_dict.get("location"))  # Output: None
```

### Nested dictionary
A nested dictionary is a dictionary that contains another dictionary (or dictionaries) as a value for one or more of its keys. This means that the values of a dictionary can themselves be dictionaries.

```python
nested_dict = {
    "person1": {"name": "Alice", "age": 30},
    "person2": {"name": "Bob", "age": 25}
}
```

#### Accessing values in a nested dictionary
```python
print(nested_dict["person1"]["name"])  # Output: Alice
print(nested_dict["person2"]["age"])   # Output: 25
```

#### Modifying values in a nested dictionary
```python
nested_dict["person1"]["age"] = 35
nested_dict["person2"]["location"] = "New York"
```