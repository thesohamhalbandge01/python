# Need of If-Else

Many times our program needs to take different actions based on some conditions.

For example, Let's suppose we have to write a program that takes the user's age and tells us if the user is old enough to vote or not. 
In this case our program will behave differently if the age entered by the user is below 18 and if the age is above 18.

If it is above 18, our program will print `"Old enough to vote!"`. Otherwise, it will print `"Not old enough to vote!"`.

We use conditions in code for decision making and controlling the flow of a program.

IF and ELSE can be used together to create conditions. The syntax for this is:

```python
if condition:
    # code to run if the condition is true
else:
    # code to run if the above condition is false
```

Condition can be any expression which you are trying to evaluate. A simple condition can be:

```python
a = 4
b = 5
if a == b:
    print("a and b are equal")
else:
    print("a and b are not equal")
```

### Output:
```
a and b are not equal
```

`a == b` is used to check whether the values of variables `a` and `b` are equal. `==` is called a equal to operator.

---

## Operators

| Operator | Description | Example |
|----------|------------|---------|
| `==` | Equal to | `a == b` |
| `!=` | Not equal to | `a != b` |
| `>`  | Greater than | `a > b` |
| `<`  | Less than | `a < b` |
| `>=` | Greater than or equal to | `a >= b` |
| `<=` | Less than or equal to | `a <= b` |

---

## Indentation

Let us take a look at the code from last problem.

```python
age = int(input())

if age >= 18:
    print("Old enough to vote")
else:
    print("Not old enough to vote")
```

Two things to note here:

1. There is some space before the `print` statements.
2. There is a colon (`:`) after `if` and `else` statements.

The space before `print` is called **indentation**. Indentation is used to define scope in Python. Because of the space before `print`, Python knows that it has to execute the `print` statement if the condition becomes True.

The colon (`:`) after `IF` and `ELSE` is also part of the syntax, you will get an error if you forget it.

---

## If Statement

The `else` statement is **optional**.

Here is an example:

```python
grade = 95
if grade >= 90:
    print("You got an A")
```

### Output:
```
You got an A
```

In this example, the `if` condition checks whether the grade is greater than or equal to 90. If the condition is `True`, the `print` statement inside the `if` block is executed, and it prints `"You got an A"`.

If the condition is `False`, the program skips the `if` block and moves on to the next part of the code (if any). Since there is no `else` block in this example, nothing happens if the condition is `False`.

The `else` block is useful when you want to specify an action if the `if` condition is not met, but it's not necessary if you only need to perform an action when the condition is `True`.

---

## Elif Statement

In the previous problems, you saw how your code can have two different flows using one `if` and one `else` condition.
Now what if you want to evaluate more than two conditions? In such case, one `if` and one `else` condition is not sufficient. That is where `elif` statements come in handy. 

In short, in cases where you have to check for multiple conditions and run some code based on each, you have to use `elif`.

The `elif` keyword means **"if the previous conditions were not true, then try this condition".**

The following example illustrates usage of `elif`.

```python
grade = 85

if grade >= 90:
    print("You got an A")
elif grade >= 80:
    print("You got a B")
```

### Output:
```
You got a B
```

The code above works as follows:

- If `grade >= 90`, then it will output: `"You got an A"`
- If `grade` is between `80` and `90` - it will output: `"You got a B"`
- If `grade` is less than `80` - there will be **no output**.

---

## Else Statement

The `else` keyword handles the case that don't meet the conditions specified in the `if` and `elif` statements. It's like a **"none of the above"** option in programming.
