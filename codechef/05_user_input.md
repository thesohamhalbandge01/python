## Taking User Input

```python
name = input()
age = input()
```

`input()` assumes that the input is a **string**.

You can convert it to an **integer** or numerical value using `int()`:

```python
age = int(input())
```

## Multiple String Inputs

Sometimes you need to accept multiple inputs in a single line. To do this, you can use the `split()` function.

For example, if the user inputs the following:

```
Good Great Awesome
```

You can read these inputs like this:

```python
a, b, c = input().split()
```

## Multiple Integer Inputs

The syntax you saw in the previous example takes **string inputs**. But if you need to take **multiple integer inputs**, you'll have to convert them separately.

You **cannot** call the `int` function directly on the `split()` input because `int` can only be called on **one value at a time**, whereas `split()` input has **multiple values**.

To handle this, you can use the `map()` function to convert the split inputs to integers in one step:

```python
a, b, c = map(int, input().split())  # assigns integer input values to variables a, b, and c
```