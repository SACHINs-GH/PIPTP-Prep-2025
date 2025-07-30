# Week1 - Day 3

## Problem 1

### Pseudocode

```
function printUp(n):
if n == 0:
return
printUp(n-1)
print(n)

printUp(3)
```

### Approach

Recursion unwinding:
1. Calls stack: `(3)` → `(2)` → `(1)` → `(0)`
2. Base case returns, then unwind prints each level
3. Output: `1`, `2`, `3`

### Result

The final output is **123**.

-----

## Problem 2

### Pseudocode

```
function mystery(n):
if n == 0:
return
mystery(n - 1)
mystery(n - 1)
print(n)

mystery(2)
```

### Approach

Double recursive calls:
1. `mystery(2)` calls `mystery(1)` twice
2. Each `mystery(1)` prints `1` after its calls
3. Finally `mystery(2)` prints `2`

### Result

The final output is **112**.

-----

## Problem 3

### Pseudocode

```
function loopRec(n):
if n == 0:
return
for i 1 to 2:
loopRec(n-1)
print(n)

loopRec(2)
```

### Approach

Loop + recursion:
1. `loopRec(2)` calls `loopRec(1)` twice in loop
2. Each `loopRec(1)` calls `loopRec(0)` twice, then prints `1`
3. Finally `loopRec(2)` prints `2`

### Result

The final output is **112**.

-----

## Problem 4

### Pseudocode

```
function sumDown(n, total):
if n == 0:
print(total)
return
sumDown(n-1, total + n)
print(n)

sumDown(3, 0)
```

### Approach

Accumulator recursion:
1. Accumulates: `(3,0)` → `(2,3)` → `(1,5)` → `(0,6)`
2. Base case prints total: `6`
3. Unwind prints each `n`: `1`, `2`, `3`

### Result

The final output is **6123**.

-----

## Problem 5

### Pseudocode

```
array = [10, 20, 30, 40]

function reversePrint(i):
if i == length(array):
return
reversePrint(i + 1)
print(array[i])

reversePrint(0)
```

### Approach

Reverse array printing:
1. Traverse forward: `(0)` → `(1)` → `(2)` → `(3)` → `(4)`
2. Base case at index 4, then unwind
3. Print elements in reverse order

### Result

The final output is **40 30 20 10**.

## Problem 6

### Pseudocode

```
def f(n):
    if(n==0) :
        return 0
    return f(n>>1) + (n&1)
print(f(7))
```

### Approach

Bit counting recursion:
1. `f(7)`: `7>>1 = 3`, `7&1 = 1` → `f(3) + 1`
2. `f(3)`: `3>>1 = 1`, `3&1 = 1` → `f(1) + 1`  
3. `f(1)`: `1>>1 = 0`, `1&1 = 1` → `f(0) + 1`
4. `f(0)` returns `0`, so: `0 + 1 + 1 + 1 = 3`

### Result

The final output is **3**.
