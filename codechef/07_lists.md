# Creating Lists

Arrays in Python are commonly referred to as lists.  
Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

In Python, a list is denoted by square brackets `[]`.  

It can hold elements of different data types, such as numbers, strings, or even other lists.  
Lists are **mutable**, which means you can modify them by adding, removing, or changing elements.

## Example Lists

```python
# Consider the list 'fruits' and 'numbers' below
fruits = ["apple", "banana", "orange", "grape"]
numbers = [20, 10, 0, -5]
```

---

## Index & Printing Specific Elements of a List

You access an array element by referring to the **index number** inside square brackets `[]`.  
Similar to what we saw in strings, list items are indexed and you can access them by referring to their index number:

```
        0       1       2      - index numbers
     ["red", "Green", "Blue"]  - the list
```
**Note**: Indexing always starts from `0` when going **left to right**.

To access a particular element of an array, we use the same syntax we used to access a character of a string:

```python
arr = ["red", "Green", "Blue"]
# to access the third element of the array:
print(arr[2]) # Output: Blue
```

---

## Changing the Elements of a List

You can also modify elements in a list by assigning a new value to a specific index.

```python
fruits = ["apple", "banana", "orange", "grape"]
fruits[1] = "kiwi"
print(fruits)  # Output: ["apple", "kiwi", "orange", "grape"]
```

---

## Displaying the Count of Elements

To get the length of a list or the number of elements present in a list, you can use the `len()` function:

```python
myNumbers = [10, 20, 30, 40, 50]
print(len(myNumbers))  # Output: 5
```

---

## Negative Indexing

List items can also be negatively indexed:

```
        -3      -2      -1      - index numbers
     ["red", "Green", "Blue"]  - the list
```

**Note**: Indexing always starts from `-1` when going **right to left**.

---

## Slicing a List

Similar to what we saw in **slicing of strings**, you can slice lists as well.  
You can specify a range of consecutive indexes by specifying where to start and where to end the range in this manner:

```python
print(list[1:4])
```

This will print elements from **index number 1 to 3**.

### **Note**:
- Indexing starts from `0`.
- Item on index `4` will **not** be printed as the end index is excluded.

Example:

```python
a = ["Juke", "King", "Hearts", "68", "Kite"]
print(a[1:4])
```

### Output:
```
["King", "Hearts", "68"]
```

---

# List Operations

## List Append

To add an item to the end of a list, we use the `append()` function.

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits)  # Output: ["apple", "banana", "cherry", "orange"]
```

---

## List Insert

Another function that helps us add elements to a list is the `insert()` function.

While the `append()` function adds elements to the end of the list, the `insert()` function allows us to **specify the index** where we want to insert the new element.

```python
fruits = ["apple", "banana", "cherry"]
fruits.insert(1, "orange")
print(fruits)  # Output: ["apple", "orange", "banana", "cherry"]
```

- When we insert a new item into the list, it is placed at the **specified position**, and the rest of the items are shifted to the right.
- In the example above, `"orange"` is added at index `1`, so `"banana"` and `"cherry"` are shifted to the right.

---

## List Remove

To remove an item, we use the `remove()` function.  
This function **removes the first occurrence** of the specified item from the list.

```python
fruits = ["apple", "banana", "cherry", "banana"]
fruits.remove("banana")
print(fruits)  # Output: ["apple", "cherry", "banana"]
```

---

## List Pop

The `pop()` function lets you remove items from a list.

If you don't specify an index, `pop()` **removes the last item**.

```python
fruits = ["apple", "banana", "cherry"]
fruits.pop()
print(fruits)  # Output: ["apple", "banana"]
```

You can also specify an index to remove an item from a specific position:

```python
fruits = ["apple", "banana", "cherry"]
removed_fruit = fruits.pop(1)
print(removed_fruit)  # Output: banana
print(fruits)  # Output: ["apple", "cherry"]
```

### **Note**:
- If you use `pop()` **without** any arguments, it **removes and returns** the last item in the list.
- If you use `pop()` **with an index**, it **removes and returns** the item at that index.
- If the index you provide is **out of range**, you will get an error.

---

## List Concatenation

When you use the addition (`+`) operator on two lists, it combines them into one longer list.

```python
fruits1 = ["apple", "banana"]
fruits2 = ["cherry", "date"]
all_fruits = fruits1 + fruits2
print(all_fruits)  # Output: ["apple", "banana", "cherry", "date"]
```

---

## List String User Input

Instead of hardcoding the list items, you can ask the user to provide them.

```python
fruits = input().split()
print(fruits)
```

### **Example User Input**:
```
apple banana cherry date
```

### **Output**:
```python
["apple", "banana", "cherry", "date"]
```

### **How It Works**:
1. The `input()` function reads a line of text input from the user.
2. The `split()` function splits the input string at each space and returns a list of words.

### **Note**:
- When using `input().split()`, the input is read as a **string** by default.
- If you need to read integer inputs, you'll need to convert these string inputs into integers.

---

## List Integer User Input

If you want to take a list of numbers as input, you need to convert each input from a string to an integer.

```python
numbers = list(map(int, input().split()))
```

### **Example User Input**:
```
1 2 3 4 5
```

### **Output**:
```python
[1, 2, 3, 4, 5]
```

### **How It Works**:
1. **Read User Input**: The `input()` function reads a line of text input.
2. **Convert to Integers**: The `map()` function applies the `int()` function to each item.
3. **Create a List**: The `list()` function collects these elements into a list.