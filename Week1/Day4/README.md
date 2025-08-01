# Week1 - Day 4

## Problem 1

### Program
```c
#include<stdio.h>
int f(int n, int k) {
    if(n==0) return 0;
    else if(n%2) return f(n/2, 2*k)+k;
    else return f(n/2, 2*k)-k;
}
int main() {
    printf("%d",f(20,1));
    return 0;
}
```

### Approach

Recursive with parameter doubling:
1. If `n` is even: subtract `k` after recursive call
2. If `n` is odd: add `k` after recursive call
3. For `f(20,1)`: unwind gives final result

### Result

The final output is **9**.

-----


## Problem 2

### Program
```c
int f(int n) {
    static int r=0;
    if(n<=0) return 1;
    if(n>3) {
        r=n;
        return f(n-2)+2;
    }
    return f(n-1)+r;
}
```

### Approach

Static variable recursion:
1. If `n>3`, set `r=n` and recurse by 2, add 2
2. Else, add `r` to result of `f(n-1)`
3. For `f(5)`, `r` is set to 5, then used in all additions

### Result

The final output is **18**.

-----
## Problem 3

### Program
```c
void f(int n) {
    if(n<=1) {
        printf("%d",n);
    } else {
        f(n/2);
        printf("%d",n%2);
    }
}
```

### Approach

Decimal to binary (recursive):
1. Recursively call with `n/2` until `n<=1`
2. Print `n%2` as stack unwinds
3. For `f(173)`, prints binary: **10101101**

### Result

The final output is **10101101**.

-----


## Problem 4

### Program
```c
unsigned int foo(unsigned int n, unsigned int r) {
    if(n>0) return ((n%r) + foo(n/r,r));
    else return 0;
}
```

### Approach

Sum of digits in base `r`:
1. Each call: return `(n % r) + foo(n / r, r)`
2. For `foo(345, 10)`: 5 + 4 + 3 = **12**

### Result

The final output is **12**.

-----

## Problem 5

### Program
```c
unsigned int foo(unsigned int n, unsigned int r) {
    if(n>0) return ((n%r) + foo(n/r,r));
    else return 0;
}
```

### Approach

Sum of binary digits:
1. Each call: return `(n % r) + foo(n / r, r)`
2. For `foo(513, 2)`: only `513` and `1` contribute `1`, rest are `0`
3. Output: `1 + 1 = 2`

### Result

The final output is **2**.

-----

## Problem 6

### Program
```python
def show(n):
    if n == 0:
        return
    show(n - 1)
    print(n)

show(3)
```

### Approach

Recursion with print after call:
1. Calls stack: show(3) → show(2) → show(1) → show(0)
2. Base case returns, then unwind prints: 1, 2, 3

### Result

The final output is **1 2 3**.

-----


## Problem 7

### Program
```python
def recur(n):
    if n == 0:
        return
    recur(n-1)
    recur(n-1)
    print(n)

recur(2)
```

### Approach

Double recursion with print after calls:
1. Each recur(1) prints 1 after two recur(0) calls
2. recur(2) prints 2 after both recur(1) calls
3. Output: 1, 1, 2

### Result

The final output is **1 1 2**.

-----


## Problem 8

### Program
```python
arr = [4, 5, 6]
def reversePrint(i):
    if i == len(arr):
        return
    reversePrint(i+1)
    print(arr[i])

reversePrint(0)
```

### Approach

Reverse print with recursion:
1. Traverse to end, then print as stack unwinds
2. For arr = [4,5,6], output: 6, 5, 4

### Result

The final output is **6 5 4**.

-----


## Problem 9

### Program
```python
def fact(n):
    if n == 1:
        return 1
    result = n * fact(n-1)
    print(result)
    return result


```

### Approach

Recursive factorial with print:
1. Compute factorial recursively
2. Print result after each call as stack unwinds
3. For fact(4): prints 2, 6, 24

### Result

The final output is **2 6 24**.

-----

## Problem 10
sum (3, 0)

### Program
```python
def sum(n, total):
    if n == 0:
        print(total)
        return
    sum(n-1, total + n)
    print(n)
```
### Approach

Accumulator recursion with print:
1. Accumulate sum in `total` until base case
2. Print total at base, then print n as stack unwinds
3. For sum(3,0): prints 6, 1, 2, 3

### Result

The final output is **6 1 2 3**.

-----