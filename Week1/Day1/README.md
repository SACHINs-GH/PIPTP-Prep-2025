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

1. Call `fun(40, 4)` with `w=40, x=4, y=0`
2. Check: `(4 mod 40 == 0) || (40 mod 4 == 0)` -> `False || True` = **True**
3. Execute `y = y + 1`, so `y = 1`

### Result

The final output is **1**.

-----

## Problem 2

### Pseudocode

Count the number of times the `while` loop executes.

```
1. Integer a
2. Set a = 1
3. while (a < 5)
4.   a = a + 2
5. end while
6. Print a
```

### Approach

1. Start with `a = 1`
2. **Iteration 1**: `1 < 5` -> True, `a = 3`
3. **Iteration 2**: `3 < 5` -> True, `a = 5`
4. **Check 3**: `5 < 5` -> False, loop ends

### Result

The `while` loop will be executed **2** times.

-----

## Problem 3

### Pseudocode

Find the output for `funn(8, 8)`:

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

Recursive trace:
- `funn(8,8)`: True -> `8 + funn(6,6) + 8`
- `funn(6,6)`: True -> `6 + funn(4,4) + 6`  
- `funn(4,4)`: True -> `4 + funn(2,2) + 4`
- `funn(2,2)`: True -> `2 + funn(0,0) + 2`
- `funn(0,0)`: False -> `0 ^ 0 = 0`

Back-substitution: `2+0+2=4`, `4+4+4=12`, `6+12+6=24`, `8+24+8=40`

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

1. Start: `a=3, b=3`
2. `a = b` (so `a=3`)
3. Check: `1 ^ 1 = 0` -> False
4. Execute else: `b = 2`

### Result

The final output is `3 + 2 =` **5**.

-----

## Problem 5

### Pseudocode

Find the output for `funn(7, 5)`:

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

1. Start: `a=7, b=5`, loop `c` from 2 to 4
2. **c=2**: `1 < 2` -> True, so `a = 1`. Inner: `2 > 5` -> False
3. **c=3**: `1 < 2` -> True, so `a = 1`. Inner: `2 > 5` -> False  
4. **c=4**: `1 < 2` -> True, so `a = 1`. Inner: `2 > 5` -> False

### Result

The final output is `1 + 5 =` **6**.

-----

## Problem 6

### Pseudocode

Find the output for `funn(4, 3)`:

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

Recursive breakdown:
- `funn(4,3)` -> `funn(2,7) + funn(1,7) + funn(0,7)`
- `funn(0,7)` -> else -> `7+7 = 14`
- `funn(1,7)` -> `funn(-1,8) + funn(-2,8) + funn(-3,8)` -> `16+16+16 = 48`
- `funn(2,7)` -> `funn(0,9) + funn(-1,9) + funn(-2,9)` -> `18+18+18 = 54`

Result: `54 + 48 + 14 = 116`

### Result



The final output is **116**.

-----

## Problem 7

### Pseudocode

Find the output for `a = 6`, `b = 1`:

```
1. Integer funn(Integer a, Integer b)
2.  a = a + a
3.  b = b + b
4.  return a + b
5. End function funn()
```

### Approach

1. Start: `a=6, b=1`
2. `a = 12`, `b = 2`

### Result

The final output is `12 + 2 =` **14**.

-----

## Problem 8

### Pseudocode

Find the output with `a=2`, `b=4`, `c=2`:

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

1. Start: `a=2, b=4, c=2`
2. `if(2)` -> True: `b = 2^4 = 6`, `a = 2`
3. `if(6)` -> True: `a = 2^6 = 4`, `b = 5`
4. `if(2)` -> True: `a = 5`

### Result

The final output is `5 + 5 + 2 =` **12**.

-----

## Problem 9

### Pseudocode

Find the output with `a=2`, `b=3`:

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

1. Start: `a=2, b=3`, loop `c` from 4 to 6
2. **c=4**: `a=5`, since `5>4` -> `a=0`, `if(2)` -> `b=10`, then `b=1`
3. **c=5**: `a=1`, since `1≤4`, `if(3)` -> `b=11`, then `b=2`  
4. **c=6**: `a=3`, since `3≤4`, `if(5)` -> `b=13`, then `b=4`

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

1. Start: `m=9, n=6`
2. `m=10, n=5`
3. `m=15`
4. `15 > 5` -> print `m`

### Result

The final output is **15**.

-----

## Problem 11

### Pseudocode

Find the output with `p=1, q=4, r=2`:

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

1. Start: `p=1, q=4, r=2`
2. Check: `1^4 > 1&4` -> `5 > 0` -> True, so `r = 0`
3. Check: `4>0 && 0>1` -> False
4. Result: `1 - 4 + 0 - 2`

### Result

The final output is `1 - 4 + 0 - 2 =` **-5**.

-----

## Problem 12

### Pseudocode

Find the output with `pp=7, qq=7, rr=2`:

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

1. Start: `pp=7, qq=7, rr=2`
2. Calculate: `pp = ((14) ^ (14&7)) ^ 14 = (14^6)^14 = 8^14 = 6`
3. `if(6 && 7)` -> True: `pp = 0`, `qq = 14`

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
