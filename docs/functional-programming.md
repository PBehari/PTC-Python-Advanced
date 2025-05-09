# Functional Programming in Python

## What is Functional Programming?

Functional programming is a way of writing code where:
1. You build your program using functions, like math functions.
2. These functions always give the same result when you give them the same input — no surprises.
3. You don’t change things, like variables or data. Instead, you make a new version of it.
4. You describe what you want to do, not how to do it step by step.

#### 1. Build programs using functions

In functional programming, you build your logic with reusable, clear functions:
```python
def add(a, b):
    return a + b

print(add(2, 3)) # Output: 5
```

#### 2. Pure functions = No surprises

A pure function always gives the same output for the same input and doesn’t change anything outside itself.
```python
def square(x):
    return x * x

print(square(5))  # Always returns 25
```

No matter how often you run this, the result stays the same.

#### 3. Don’t change data — create new data

Instead of updating existing data, return new data.
```python
numbers = [1, 2, 3, 4]

# Create a new list of doubled numbers
doubled = list(map(lambda x: x * 2, numbers))

print(numbers) # [1, 2, 3, 4] — original unchanged
print(doubled) # [2, 4, 6, 8] — new list
```

This avoids bugs and keeps your code clean.

#### 4. Describe what you want, not how to do it

Imperative Style (Step-by-step)
```python
nums = [1, 2, 3, 4]
squares = []
for n in nums:
    squares.append(n * n)
```

Functional Style (What to do)
```python
nums = [1, 2, 3, 4]
squares = list(map(lambda x: x * x, nums))
```

Much shorter, easier to read, and less room for mistakes!

## When to Use Functional Programming

Functional programming is a style of writing code using pure functions — no changing variables, no side effects. It's useful when you want clean, reusable, and safe code.

#### 1. You Want Clean and Readable Code
Use `map()`, `filter()`, `lambda` to express ideas simply.

**Example:**
```python
squares = list(map(lambda x: x*x, nums))
```

#### 2. You Want to Avoid Bugs

- Pure functions don’t change anything outside themselves.
- Safe for large projects: no hidden changes, no surprises.

#### 3. You Want to Write Code That Runs in Parallel

- Functional code doesn’t share state, so it works well with multiprocessing.
- Great for data science, analytics, and large-scale computations.

#### 4. You Want Reusable and Testable Functions

- Pure functions depend only on inputs → easy to test.
- You can reuse the same function in many places without breaking other code.

#### 5. You’re Working with Lists or Collections

- Functional tools make working with data much easier.
- Use `map()`, `filter()`, `reduce()` for transforming data.

## When Not to Use It

- For apps with lots of changing state, like games or GUIs, object-oriented programming might work better.
- Nested functional code (especially with lambdas) can become hard to read if overused.