## Arithmetic

```python
a = 6
b = 3

print(a + b)  # addition: 9
print(a - b)  # subtraction: 3
print(a * b)  # multiplication: 18
print(a / b)  # division: 2.0
print(10 // 3)  # integer division: 3 (returns the whole number of the quotient discarding remainder)
print(a % b)  # modulus: 0 (returns the remainder) 
print(a ** b)  # exponentiation: 216 (a^b => 6^3 => 6 * 6 * 6 => 216)
```

## Assignment

```python
length = 15  # basic assignment

length += 15  # length = length + 15
length -= 15  # length = length - 15
length *= 15  # length = length * 15
length /= 15  # length = length / 15
length %= 15  # length = length % 15
```

## Relational (Will Return Either True/False)

- `a > b`   (Checks if `a` is greater than `b`)
- `a == b`  (Checks if `a` is equal to `b`)
- `a != b`  (Checks if `a` is not equal to `b`)
- `a >= b`  (Checks if `a` is greater than or equal to `b`)
- `a <= b`  (Checks if `a` is less than or equal to `b`)

## Logical

### 1. `and`
The `AND` operator returns `True` only if both conditions are `True`.

```python
a = 7
condition = a > 5 and a < 10  # Only True if a is greater than 5 AND less than 10
print(condition)  # Output: True
```

### 2. `or`
The `OR` operator returns `True` if at least one of the conditions is `True`.

```python
a = 7
condition = a > 10 or a < 5  # True if a is greater than 10 OR less than 5
print(condition)  # Output: False
```

### 3. `not`
The `NOT` operator reverses the result of the condition. If the condition is `True`, `not` makes it `False`. If the condition is `False`, `not` makes it `True`.

```python
a = 7
condition = not(a > 5)  # Reverses the result of a > 5
print(condition)  # Output: False
```