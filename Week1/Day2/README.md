# Week1 - Day 2

## Problem 1

### Pseudocode

```
1. Integer a, b, c
2. Set a=2, b=6, c=8
3. a = (10+9) + c
4. if((c+b) > (a-c))
5.   a = b+c
6.   b = b+b
7. End if
8. Print a+b+c
```

### Approach

1. Start: `a=2, b=6, c=8`
2. `a = (10+9) + 8 = 27`
3. Check: `(14) > (19)` -> **False**
4. Skip if block

### Result

The final output is `27 + 6 + 8 =` **41**.

-----

## Problem 2

### Pseudocode

```
1. Integer funn(Integer a, Integer b, Integer c)
2.   b = 7+a
3.   a = (a+c)+a
4.   b = (b+b)+c
5.   c = 1+b
6.   return a+b+c
7. End function funn()

// Initial values: a=0, b=2, c=10
```

### Approach

1. Start: `a=0, b=2, c=10`
2. `b = 7`, `a = 10`, `b = 24`, `c = 25`

### Result

The final returned value is `10 + 24 + 25 =` **59**.

-----

## Problem 3

### Pseudocode

```
1. Integer pp, qq, rr
2. Set pp=0, qq=6, rr=7
3. pp = rr+pp
4. pp = (rr&4)^rr
5. if((qq&pp&rr) < (rr&qq))
6.   if((qq^pp) < (rr+qq))
7.     rr = (3+1)^pp
8.   End if
9. End if
10. Print pp+qq+rr
```

### Approach

1. Start: `pp=0, qq=6, rr=7`
2. `pp = 7`, then `pp = (7&4)^7 = 3`
3. Check: `(6&3&7) < (7&6)` -> `2 < 6` -> **True**
4. Inner check: `(6^3) < (7+6)` -> `5 < 13` -> **True**
5. `rr = 4^3 = 7`

### Result

The final output is `3 + 6 + 7 =` **16**.

-----

## Problem 4

### Pseudocode

```
1. Integer p, q, r
2. Set p=9, q=6, r=10
3. if(((q^p^r) > (r^q)))
4.   r = (11&12)+q
5. End if
6. if(((q^6^8) > (p^4)))
7.   p = (r+3)&r
8. End if
9. Print p+q+r
```

### Approach

1. Start: `p=9, q=6, r=10`
2. First: `(q^p^r) > (r^q)` -> `5 > 12` -> **False**
3. Second: `(q^6^8) > (p^4)` -> `8 > 13` -> **False**
4. Both skipped

### Result

The final output is `9 + 6 + 10 =` **25**.

-----

## Problem 5

### Pseudocode

```
1. Integer pp, qq, rr
2. Set pp=1, qq=2, rr=8
3. if((5+rr) < (7+qq))
4.   // Inner block 1
5. else
6.   if((pp+qq-rr) < (rr+pp))
7.     pp = pp+rr
8.     rr = (pp&rr)+pp
9.   End if
10. End if
11. Print pp+qq+rr
```

### Approach

1. Start: `pp=1, qq=2, rr=8`
2. First: `(5+8) < (7+2)` -> `13 < 9` -> **False**
3. Else: `(1+2-8) < (8+1)` -> `-5 < 9` -> **True**
4. `pp = 9`, `rr = (9&8)+9 = 17`

### Result

The final output is `9 + 2 + 17 =` **28**.

-----

## Problem 6

### Pseudocode

```
1. Integer p, q, r
2. Set p=8, q=4, r=5
3. if(((r+q) < (q-r)) || p>q)
4.   q = (q&8) & r
5. End if
6. Print p+q+r
```

### Approach

1. Start: `p=8, q=4, r=5`
2. Check: `((9) < (-1)) || (8>4)` -> `False || True` -> **True**
3. Execute: `q = (4&8)&5 = 0`

### Result

The final output is `8 + 0 + 5 =` **13**.

-----

## Problem 7

### Pseudocode

```
1. Integer funn(Integer a, Integer b, Integer c)
2.   for(each c from 5 to 9)
3.     if((b+5) > (a-b))
4.       a = (b+5)^a
5.     End if
6.     b = 5^c
7.   End for
8.   return a+b
// Initial values: a=1, b=2
```

### Approach

1. Start: `a=1, b=2`, loop `c` from 5 to 9
2. **c=5**: `7 > -1` -> True: `a=6`, `b=0`
3. **c=6**: `5 > 6` -> False: `b=3`
4. **c=7**: `8 > 3` -> True: `a=14`, `b=2`
5. **c=8**: `7 > 12` -> False: `b=13`
6. **c=9**: `18 > 1` -> True: `a=28`, `b=12`

### Result

The final returned value is `28 + 12 =` **40**.

-----

## Problem 8

### Pseudocode

```
1. Integer funn (Integer a, Integer b, Integer c)
2.   if((a&7&b) > (6&a))
3.     b = (12+7)+a
4.     c = (12+4)+b
5.   End if
6.   if((2+3) < (5+b))
7.     b = (b+3)+c
8.     a = (9&10)+c
9.   End if
10.  return a+b+c
// Initial values: a=2, b=6, c=5
```

### Approach

1. Start: `a=2, b=6, c=5`
2. First: `(2&7&6) > (6&2)` -> `2 > 2` -> **False**
3. Second: `(5) < (11)` -> **True**: `b=14`, `a=13`

### Result

The final returned value is `13 + 14 + 5 =` **32**.

-----

## Problem 9

### Pseudocode

```
1. Integer p, q, r
2. Set p=0, q=8, r=10
3. if(p<r && (p&q)<r)
4.   q = 4&q
5.   p = (q+3)^r
6. End if
7. r = (q&1)+p
8. q = (q^9)+p
9. Print p+q+r
```

### Approach

1. Start: `p=0, q=8, r=10`
2. Check: `0<10 && 0<10` -> **True**: `q=0`, `p=9`
3. `r = 9`, `q = 18`

### Result

The final output is `9 + 18 + 9 =` **36**.

-----

## Problem 10

### Pseudocode

```
1. Integer p, q, r
2. Set p=1, q=4, r=7
3. p = (1+8)+q
4. r = (p&r)+r
5. r = q+q
6. if((q+r) < (r-q) && 7>p)
7.   p = r+q
8.   p = (p+11)+q
9. End if
10. Print p+q+r
```

### Approach

1. Start: `p=1, q=4, r=7`
2. `p = 13`, `r = 12`, `r = 8`
3. Check: `12<4 && 7>13` -> **False**

### Result

The final output is `13 + 4 + 8 =` **25**.

-----

## Problem 11

### Pseudocode

```
1. Integer p, q, r
2. Set p=6, q=3, r=9
3. if((p&r) < (q-p))
4.   p = (2^7)+r
5.   p = (p+3)^r
6.   q = 4^q
7. End if
8. r = (r+p)&q
9. Print p+q+r
```

### Approach

1. Start: `p=6, q=3, r=9`
2. Check: `(6&9) < (3-6)` -> `0 < -3` -> **False**
3. `r = (9+6)&3 = 3`

### Result

The final output is `6 + 3 + 3 =` **12**.

-----

## Problem 12

### Pseudocode

```
1. Integer pp, qq, rr
2. Set pp=8, qq=4, rr=5
3. for(each rr from 4 to 5)
4.   if((rr-pp+qq) < (qq+rr))
5.     pp = (5+5)+qq
6.   End if
7.   pp = (rr+qq)+pp
8. End for
9. Print pp+qq
```

### Approach

1. Start: `pp=8, qq=4`, loop `rr` from 4 to 5
2. **rr=4**: `0 < 8` -> True: `pp=14`, then `pp=22`
3. **rr=5**: `-13 < 9` -> True: `pp=14`, then `pp=23`

### Result

The final output is `23 + 4 =` **27**.

-----

## Problem 13

### Pseudocode

```
1. Integer p, q, r
2. Set p=4, q=2, r=4
3. for(each r from 5 to 6)
4.   q = (r+r)+q
5.   if((p+r-q) < (6-p))
6.     p = p+q
7.     q = 12+r
8.   End if
9. End for
10. Print p+q
```

### Approach

1. Start: `p=4, q=2`, loop `r` from 5 to 6
2. **r=5**: `q=12`, check `-3 < 2` -> True: `p=16, q=17`
3. **r=6**: `q=29`, check `-7 < -10` -> False

### Result

The final output is `16 + 29 =` **45**.

-----

## Problem 14

### Pseudocode

```
1. Integer a, b, c
2. Set a=1, b=2, c=9
3. if((b+c) > (c-b))
4.   c=a+a
5. End if
6. if((7+3) < (6+a))
7.   b=12+a
8. End if
9. Print a+b+c
```

### Approach

1. Start: `a=1, b=2, c=9`
2. First: `(11) > (7)` -> **True**: `c=2`
3. Second: `(10) < (7)` -> **False**

### Result

The final output is `1 + 2 + 2 =` **5**.

-----

## Problem 15

### Pseudocode

```
1. Integer funn (Integer a, Integer b, Integer c)
2.   if((c+a+b) < (b+c))
3.     // ... nested if blocks ...
4.   End if
5.   a = a&c
6.   c = a^a
7.   return a+b+c
// Initial values: a=6, b=8, c=4
```

### Approach

1. Start: `a=6, b=8, c=4`
2. Check: `(18) < (12)` -> **False**
3. Skip nested blocks: `a=4`, `c=0`

### Result

The final returned value is `4 + 8 + 0 =` **12**.

-----

## Problem 16

### Pseudocode

```
1. Integer funn (Integer a, Integer b, Integer c)
2.   b = c^c
3.   c = (12+8)+c
4.   if((b&a) < a && (8*2)>a)
5.     // ... if block ...
6.   Else
7.     a = 3^c
8.   End if
9.   return a+b+c
// Initial values: a=3, b=4, c=4
```

### Approach

1. Start: `a=3, b=4, c=4`
2. `b=0`, `c=24`
3. Check condition -> else executes: `a=27`

### Result

The final output is `27 + 0 + 24 =` **51**.

-----

## Problem 17

### Pseudocode

```
1. Integer funn (Integer a, Integer b, Integer c)
2.   for (each c from 4 to 5)
3.     b = c+b
4.     if((4-c-a) < (a+b))
5.       b = (b+8)+b
6.       b = (a^b)+b
7.     Else
8.       // ... jump out ...
9.     End if
10.  End for
11.  return a+b
// Initial values: a=1, b=6
```

### Approach

1. Start: `a=1, b=6`, loop `c` from 4 to 5
2. **c=4**: `b=10`, check `-1 < 11` -> True: `b=28`, then `b=57`
3. **c=5**: `b=62`, check `-2 < 63` -> True: `b=132`, then `b=265`

### Result

The final returned value is `1 + 265 =` **266**.

