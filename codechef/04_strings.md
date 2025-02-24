## Creating a String

```python
name = 'Chef'
```

## Concatenation

```python
x = 'Good'
y = 'Work'
print(x + y)  # Output: GoodWork

x = "Good"
y = "Work"
print(x + " " + y)  # Output: Good Work
```

## Repetition

```python
string = "hello "
result = string * 3
print(result)  # Output: hello hello hello
```

## Length

```python
greeting = "hello"
len_string = len(greeting) 
print(len_string)  # Output: 5 (len_string now stores the value of the length of greeting)
```

## Lower and Upper Case

```python
name = 'CodeChef'
lowercase_name = name.lower()
uppercase_name = name.upper()
print(lowercase_name)  # Output: codechef
print(uppercase_name)  # Output: CODECHEF
```

## Indexing

We can access the characters in a string by referring to its index number inside square brackets `[ ]`.
This concept is known as **indexing**.

### Positive Indexing
Starts from the beginning of the string. The first character is at index `0`, the second is at index `1`, and so on.

```python
s = "Codechef"
print(s[0])  # Output: C
print(s[1])  # Output: o
```

### Negative Indexing
Starts from the end of the string. The last character is at index `-1`, the second to last is at index `-2`, and so on.

```python
s = "Codechef"
print(s[-1])  # Output: f
print(s[-2])  # Output: e
```

## Changing Characters in a String

In Python, strings are **immutable**, which means you cannot directly update or change a character in a string.

However, you can create a new string with the desired changes.
Here's an example of how you can replace a character:

```python
myString = "Chaf"
myString_new = myString.replace('a', 'e')  
print(myString_new)  # Output: Chef
```

> **Note:** The `replace()` method replaces all occurrences of the provided character.

## Slicing

Slicing is a way to extract a part (substring) from a string.

### Syntax:
```python
substring = string[start:end]
```

To get the first 4 characters of a string:

```python
str = 'Interesting'
substring = str[0:4]
print(substring)  # Output: Inte 
```

Another syntax:
```python
substring = string[start:end:step]
```

Step is how many characters you move forward each time you read.
- If `step` is `1`, you read one character at a time.
- If `step` is `2`, you skip one character and then read the next one.

Example:
```python
s = 'abcde'
print(s[0:4:2])  # Output: ac
```

Here, the step is set to `2`, so it takes 2 jumps after reading each character.
- The character at start index `0` is `a`.
- Then, it jumps by 2 characters and gets `c`.
- The slicing stops at index `3` because the end index is set to `4`.

## Reverse Slicing

By default, slicing moves from **left to right**.
However, you can traverse from **right to left** by using a **negative step**.

```python
s = 'abcde'
print(s[4:0:-1])  # Output: edcb
```

When using a negative step:
- The slicing starts at index `4` (character `e`).
- It moves backward one character at a time.
- It stops at index `1` (character `b`) because the end index is `0`.

To **reverse the entire string**, use:

```python
print(s[::-1])  # Output: edcba
```