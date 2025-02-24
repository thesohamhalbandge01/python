# Loops

A loop in programming is like doing something over and over again until you're satisfied.  
You get to pick what you want to do and how many times you want to do it.  
It's like telling the computer, "Keep doing this until I say stop!"

Using loops makes things easier because instead of writing the same instructions multiple times, you can just tell the computer to repeat those instructions for you.

Imagine you want to print numbers from 1 to 10, each on a new line.

Without using a loop, you'd have to write 10 separate print statements like this:

```python
print(1)
print(2)
print(3)
# And so on, until print(10)
```

---

## While Loop

LOOPS can execute a block of code as long as a specified condition is reached.  
They are handy because they save time, reduce errors, and make code more readable.

The **WHILE LOOP** loops through a block of code as long as a specified condition is true:

```python
while (condition):
    # code to be executed
```

### Example

```python
counter = 0
while counter < 5:
    print("The counter is:", counter)
    counter = counter + 1
```

In the example above, the **WHILE loop** is executed as long as the condition `'counter < 5'` is true.  
- The initial value of `counter` is `0`.
- The code block inside the loop prints the value of `counter` and increments it by `1`.
- The loop will continue executing until `counter` becomes equal to or greater than `5`.

---

## For Loop

When you know **exactly how many times** you want to loop through a block of code, use the **FOR loop** instead of a **WHILE loop**.

The **FOR loop** in Python is designed to iterate over a sequence of elements, such as a list, string, or range of numbers.

### Example 1: Iterating over a list

```python
fruits = ["apple", "banana", "orange"]
for item in fruits:
    print(item)
```

#### Output:
```
apple
banana
orange
```

The **For loop** iterates over each element in the `fruits` list.  
On each iteration, the `item` variable takes the value of the current element and prints it.

---

### For loop iterating over a string

```python
name = "Alice"
for char in name:
    print(char)
```

#### Output:
```
A
l
i
c
e
```

Here, the **For loop** iterates over each character in the `name` string.  
The `char` variable takes on the value of each character, and it is printed.

---

## Range of numbers

In Python, you can use a **for loop** to iterate over a sequence of numbers.

The **`range()` function** helps generate this sequence, allowing you to define where to start, where to stop, and how much to increment by.

```python
for i in range(start, stop, step):
    # do something
```

### Example

```python
for i in range(0, 10, 2):
    print(i)
```

#### Output:
```
0
2
4
6
8
```

- `start`: The first number in the sequence (inclusive). In `range(0, 10, 2)`, the sequence starts at `0`.
- `stop`: The number where the sequence ends (exclusive). It stops before `10`.
- `step`: The increment between numbers. In `range(0, 10, 2)`, it increments by `2`.

---

## Two range arguments

Another way to use the `range` function is by providing **two arguments**: `start` and `stop`.

```python
for i in range(2, 6):
    print(i)
```

#### Output:
```
2
3
4
5
```

Here, the **sequence starts at 2** and **stops before 6**.

---

## Single range argument

You can also pass just **one argument** to the `range()` function.

```python
for i in range(5):
    print(i)
```

#### Output:
```
0
1
2
3
4
```

- The sequence starts at `0` and ends at `n-1`. In this example, it generates numbers from `0` to `4`.
- This is useful when you need to repeat something a specific number of times.

---

## Break Statement

The **break statement** allows you to **exit a loop prematurely**.

- When the `break` statement is encountered inside a loop, the loop is immediately terminated.
- The program execution continues with the next statement after the loop.

### Example

```python
fruits = ["apple", "banana", "orange", "grape"]

for item in fruits:
    if item == "orange":
        break
    print(item)
```

#### Output:
```
apple
banana
```

Here, when the loop encounters `"orange"`, it breaks and exits the loop.

---

## Continue Statement

The **continue statement** allows you to **skip an iteration** in a loop.

- Unlike `break`, `continue` **does not exit the loop**; it **skips the current iteration** and moves to the next one.

### Example: Print odd numbers using `continue`

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers:
    if number % 2 == 0:
        continue
    print(number)
```

#### Output:
```
1
3
5
7
9
```

Here, when `number % 2 == 0` (i.e., when the number is even), the `continue` statement **skips** that iteration and moves to the next number.