# Week1 - Day 1

## Problem 1

### Pseudocode

```
1. void fun(Integer w, Integer x)
2.   Set y = 0
3.   if ((x mod w == 0) || (w mod x == 0))
4.     y = y + 1
5.   else
6.     y = y + 10
7.   End if
8.   Print y
9. End function fun()

// Function call: fun(40, 4)
```

### Approach

1.  The function `fun` is called with `w = 40` and `x = 4`.
2.  A variable `y` is initialized to `0`.
3.  The `if` statement checks the condition `(x mod w == 0) || (w mod x == 0)`.
4.  The first part of the OR condition is `(4 mod 40 == 0)`, which is **FALSE**.
5.  The second part of the OR condition is `(40 mod 4 == 0)`, which is **TRUE**.
6.  Since one of the operands in the logical OR is TRUE, the entire condition is TRUE.
7.  The code inside the `if` block is executed: `y = y + 1`, so `y` becomes `1`.
8.  The function then prints the final value of `y`.

### Result

The final output is **1**.

-----

## Problem 2

### Pseudocode

This Problem asks for the number of times the `while` loop will be executed.

```
1. Integer a
2. Set a = 1
3. while (a < 5)
4.   a = a + 2
5. end while
6. Print a
```

### Approach

1.  The variable `a` is initialized to `1`.
2.  **First Iteration**: The condition `a < 5` (`1 < 5`) is TRUE. The loop executes. `a` is updated to `1 + 2 = 3`.
3.  **Second Iteration**: The condition `a < 5` (`3 < 5`) is TRUE. The loop executes. `a` is updated to `3 + 2 = 5`.
4.  **Third Check**: The condition `a < 5` (`5 < 5`) is FALSE. The loop terminates.

### Result

The `while` loop will be executed **2** times.

-----

## Problem 3

### Pseudocode

What is the output for the initial call `funn(8, 8)`?

```
1. Integer funn (Integer a, Integer b)
2.   if (a && b && a+b > 0)
3.     return a + funn(a-2, b-2) + b
4.   End If
5.   return a ^ b
6. End function funn()
```

*Note: `&&` is logical AND, `^` is bitwise XOR.*

### Approach

This is a recursive function. The trace of the calls is as follows:

  * `fun(8, 8)`: The condition is TRUE. Returns `8 + fun(6, 6) + 8`.
  * `fun(6, 6)`: The condition is TRUE. Returns `6 + fun(4, 4) + 6`.
  * `fun(4, 4)`: The condition is TRUE. Returns `4 + fun(2, 2) + 4`.
  * `fun(2, 2)`: The condition is TRUE. Returns `2 + fun(0, 0) + 2`.
  * `fun(0, 0)`: The condition is FALSE. It returns `0 ^ 0 = 0`.

The values are then substituted back up the call stack:

  * `fun(2, 2)` returns `2 + 0 + 2 = 4`.
  * `fun(4, 4)` returns `4 + 4 + 4 = 12`.
  * `fun(6, 6)` returns `6 + 12 + 6 = 24`.
  * `fun(8, 8)` returns `8 + 24 + 8 = 40`.

### Result

The final output is **40**.

-----

## Problem 4

### Pseudocode

```
1. Integer a, b
2. Set a = 3, b = 3
3. a = b
4. if (1 ^ 1)
5.   a = 1
6. else
7.   b = 2
8. End if
9. Print a + b
```

*Note: `^` is bitwise XOR. `if(x)` executes if `x` is not zero.*

### Approach

1.  Variables `a` and `b` are initialized to `3`.
2.  The `if` condition checks the value of `1 ^ 1`.
3.  The bitwise XOR operation `1 ^ 1` results in `0`.
4.  Since the value inside `if()` is `0`, the condition is FALSE.
5.  The `else` block is executed, setting `b` to `2`.
6.  At this point, `a` is `3` and `b` is `2`.
7.  The final line prints the sum `a + b`.

### Result

The final output is `3 + 2 =` **5**.

-----

## Problem 5

### Pseudocode

What is the output for the call `funn(7, 5)`?

```
1. Integer funn(Integer a, Integer b)
2.  for (each c from 2 to 4)
3.   if( (a mod c) < (b mod 3) )
4.    a = a mod 3
5.    if( (5 mod 3) > b )
6.     a=b
7.     b=1
8.    End if
9.   End if
10.  End for
11.  return a + b
```

### Approach

1.  Initially, `a = 7` and `b = 5`. The `for` loop iterates for `c = 2, 3, 4`.
2.  **c = 2**: `if ((7 mod 2) < (5 mod 3))` -\> `if (1 < 2)` is TRUE. `a` becomes `7 mod 3`, so `a = 1`. The inner `if` is FALSE.
3.  **c = 3**: `if ((1 mod 3) < (5 mod 3))` -\> `if (1 < 2)` is TRUE. `a` becomes `1 mod 3`, so `a = 1`. The inner `if` is FALSE.
4.  **c = 4**: `if ((1 mod 4) < (5 mod 3))` -\> `if (1 < 2)` is TRUE. `a` becomes `1 mod 3`, so `a = 1`. The inner `if` is FALSE.
5.  The loop finishes. The final values are `a = 1` and `b = 5`.
6.  The function returns `a + b`.

### Result

The final output is `1 + 5 =` **6**.

-----

## Problem 6

### Pseudocode

What is the output for the call `funn(4, 3)`?

```
1. Integer funn(Integer a, Integer b)
2.  if (a > 0)
3.   return funn(a-2, a+b) + funn(a-3, a+b) + funn(a-4, a+b)
4.  Else
5.   a = b
6.   b = a
7.   return a + b
8.  End if
9. End function funn()
```

### Approach

This is a deeply recursive function.

  * `fun(4, 3)` returns `fun(2, 7) + fun(1, 7) + fun(0, 7)`.
  * Solving the sub-problems:
      * `fun(0, 7)` runs the `else` block, returning `7 + 7 = 14`.
      * `fun(1, 7)` returns `fun(-1, 8) + fun(-2, 8) + fun(-3, 8)`. Each of these calls returns `16`, for a total of `48`.
      * `fun(2, 7)` returns `fun(0, 9) + fun(-1, 9) + fun(-2, 9)`. Each of these calls returns `18`, for a total of `54`.
  * The final calculation is `54 + 48 + 14`.

### Result

The final output is **116**.

-----

## Problem 7

### Pseudocode

What is the output for `a = 6`, `b = 1`?

```
1. Integer funn(Integer a, Integer b)
2.  a = a + a
3.  b = b + b
4.  return a + b
5. End function funn()
```

### Approach

1.  The function is called with `a = 6` and `b = 1`.
2.  `a` is updated to `6 + 6 = 12`.
3.  `b` is updated to `1 + 1 = 2`.
4.  The function returns the sum of the new `a` and `b`.

### Result

The final output is `12 + 2 =` **14**.

-----

## Problem 8

### Pseudocode

What is the output given initial values `a=2`, `b=4`, `c=2`?

```
// Initial values a=2, b=4, c=2
1. if(b-a)
2.  b = a ^ b
3.  a = c
4.  if(b)
5.   a = a ^ b
6.   b = b - 1
7.  End if
8. End if
9. if(c)
10.  a = b
11. End if
12. Print a + b + c
```

### Approach

1.  Initial values: `a = 2`, `b = 4`, `c = 2`.
2.  `if(b-a)` -\> `if(2)` is TRUE.
3.  `b = 2 ^ 4`, so `b` becomes `6`.
4.  `a = c`, so `a` becomes `2`.
5.  Inner `if(b)` -\> `if(6)` is TRUE.
6.  `a = 2 ^ 6`, so `a` becomes `4`.
7.  `b = 6 - 1`, so `b` becomes `5`.
8.  Final `if(c)` -\> `if(2)` is TRUE.
9.  `a = b`, so `a` becomes `5`.
10. The values to be printed are `a=5`, `b=5`, `c=2`.

### Result

The final output is `5 + 5 + 2 =` **12**.

-----

## Problem 9

### Pseudocode

What is the output given `a=2`, `b=3`?

```
// Initial values a=2, b=3
1. for (each c from 4 to 6)
2.  a = a + b
3.  if(a > 4)
4.   a = 0
5.  End if
6.  if(a + 2)
7.   b = a + 10
8.  Else
9.   Jump out of the loop
10. End if
11.  b = a + 1
12. End for
13. Print a + b
```

### Approach

1.  Initial values: `a = 2`, `b = 3`. The `for` loop runs for `c = 4, 5, 6`.
2.  **c = 4**: `a` becomes `5`. The `if(a > 4)` is TRUE, so `a` becomes `0`. The `if(a + 2)` is TRUE, so `b` becomes `10`. Then `b` becomes `1`.
3.  **c = 5**: `a` becomes `1`. The `if(a > 4)` is FALSE. The `if(a + 2)` is TRUE, so `b` becomes `11`. Then `b` becomes `2`.
4.  **c = 6**: `a` becomes `3`. The `if(a > 4)` is FALSE. The `if(a + 2)` is TRUE, so `b` becomes `13`. Then `b` becomes `4`.
5.  The loop finishes. Final values are `a = 3`, `b = 4`.

### Result

The final output is `3 + 4 =` **7**.

-----

## Problem 10

### Pseudocode

```
1. Integer m, n
2. Set m = 9, n = 6
3. m = m + 1
4. n = n - 1
5. m = m + n
6. if(m > n)
7.  print m
8. else
9.  print n
10. end if
```

### Approach

1.  `m` is set to `9` and `n` is set to `6`.
2.  `m` is incremented to `10`.
3.  `n` is decremented to `5`.
4.  `m` is updated to `m + n`, which is `10 + 5 = 15`.
5.  The condition `if(15 > 5)` is TRUE.
6.  The program prints the value of `m`.

### Result

The final output is **15**.

-----

## Problem 11

### Pseudocode

What is the output given `p=1, q=4, r=2`?

```
// Initial values p=1, q=4, r=2
1. if (p^q > p&q)
2.  r = p&q
3. Else
4.  r = p^q
5. End if
6. if (q>r && r>p)
7.  p = q
8. End if
9. Print p - q + r - 2
```

### Approach

1.  Initial values: `p = 1`, `q = 4`, `r = 2`.
2.  `p ^ q` is `1 ^ 4`, which results in `5`.
3.  `p & q` is `1 & 4`, which results in `0`.
4.  The condition `(5 > 0)` is TRUE. `r` is set to `p & q`, so `r` becomes `0`.
5.  The next condition `if (4>0 && 0>1)` is FALSE.
6.  The program prints `p - q + r - 2`.

### Result

The final output is `1 - 4 + 0 - 2 =` **-5**.

-----

## Problem 12

### Pseudocode

What is the output given `pp=7, qq=7, rr=2`?

```
// Initial values pp=7, qq=7, rr=2
1. pp = ((pp+pp) ^ ((pp+pp) & pp)) ^ (pp+pp)
2. if (pp && qq)
3.  pp = pp ^ pp
4.  qq = qq + qq
5. End if
6. Print pp + qq + rr
```

### Approach

1.  Initial values: `pp = 7`, `qq = 7`, `rr = 2`.
2.  **Line 1**: The complex expression evaluates step-by-step: `(14 ^ (14 & 7)) ^ 14` -\> `(14 ^ 6) ^ 14` -\> `8 ^ 14`. `pp` becomes `6`.
3.  **Line 2**: `if (6 && 7)` is TRUE.
4.  `pp = 6 ^ 6`, so `pp` becomes `0`.
5.  `qq = 7 + 7`, so `qq` becomes `14`.
6.  The program prints `pp + qq + rr`.

### Result

The final output is `0 + 14 + 2 =` **16**.

-----

## Coding Round Problem

### Problem Statement

Implement the function `InitialsName(name)` that accepts a string containing a first, an optional middle, and a last name. The function should return a string with the first and middle names converted to initials, followed by the last name.

  * **Format**: `F. M. Lastname`
  * **Example Input**: `Abc Xyz Pqrst`
  * **Example Output**: `A. X. Pqrst`

### Python Code Implementation

```python
name = input() # e.g., "Mnas Cdefgh"

def InitialsName (name):
  name = name.split(" ")
  newName = ""
  for i in range(len(name)):
    if(i == (len(name)-1)): # Check if it's the last name
      newName = newName + name[i]
    else: # It's a first or middle name
      newName = newName + name[i][0] + ". "
  return newName

p = InitialsName (name)
print(p)
```

### Sample Result

  * **Input**: `Mnas Cdefgh`
  * **Output**: `M. Cdefgh`
