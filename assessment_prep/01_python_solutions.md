# Section 1 - Python Fundamentals - Solutions

## Part A - Multiple choice

**Q1. Answer: B**

- A) `-10 % 3` -> `2`
- B) `-10//3` -> `-4`
- C) `-10/3` -> `-3.3333333333333335`
- D) `int(-10/3)` -> `-3`

*Explanation:* `//` is floor division: it rounds towards negative infinity, so -3.33 becomes -4.

**Q2. Answer: C**

- A) `-5` -> `-5`
- B) `5**2` -> `25`
- C) `5**-1` -> `0.2`
- D) `5**0` -> `1`

*Explanation:* A negative power means a reciprocal: 5**-1 = 1/5 = 0.2.

**Q3. Answer: C**

- A) `bool('false')` -> `True`
- B) `bool(' ')` -> `True`
- C) `bool('')` -> `False`
- D) `bool(-123)` -> `True`

*Explanation:* An empty string is falsy. A non-empty string (even `'false'` or a single space) and any non-zero number are truthy.

**Q4. Answer: A**

- A) `type(10/5).__name__` -> `'float'`
- B) `type(10//5).__name__` -> `'int'`
- C) `type('10').__name__` -> `'str'`
- D) `type(True).__name__` -> `'bool'`

*Explanation:* `/` always returns a float in Python 3, even when the division is exact.

**Q5. Answer: A**

- A) `2 + 3 * 4 ** 2` -> `50`
- B) `(2 + 3 * 4) ** 2` -> `196`
- C) `(2 + 3) * 4 ** 2` -> `80`
- D) `2 + 3 * 4 * 2` -> `26`

*Explanation:* Precedence: `**` first, then `*`, then `+`. So 2 + 3*16 = 50.

**Q6. Answer: D**

- A) `7 % 3 * 7 // 3` -> `2`
- B) `7 % 3 - 7 // 3` -> `-1`
- C) `7 % 3 + 7 // 3 + 1` -> `4`
- D) `7 % 3 + 7 // 3` -> `3`

*Explanation:* 7 % 3 = 1 and 7 // 3 = 2, so the sum is 3.

**Q7. Answer: C**

- A) `len('Data')` -> `4`
- B) `len('Data Science') + 1` -> `13`
- C) `len('Data Science')` -> `12`
- D) `len('DataScience')` -> `11`

*Explanation:* The space is also a character, so the length is 12.

**Q8. Answer: A**

- A) `'Python'[1:4]` -> `'yth'`
- B) `'Python'[1:5]` -> `'ytho'`
- C) `'Python'[0:3]` -> `'Pyt'`
- D) `'Python'[2:4]` -> `'th'`

*Explanation:* Slicing includes the start index and excludes the end index: characters at positions 1, 2 and 3.

**Q9. Answer: D**

- A) `'Python'[1:5]` -> `'ytho'`
- B) `'Python'[-1:-6:-1]` -> `'nohty'`
- C) `'Python'[::1]` -> `'Python'`
- D) `'Python'[::-1]` -> `'nohtyP'`

*Explanation:* A step of -1 walks the string backwards.

**Q10. Answer: A**

- A) `a[-2:]` -> `[4, 5]`
- B) `a[-2]` -> `4`
- C) `a[2:]` -> `[3, 4, 5]`
- D) `a[:2]` -> `[1, 2]`

*Explanation:* `a[-2:]` starts at the second-last element and goes to the end.

**Q11. Answer: A**

- A) `(lambda a: (a.append([4, 5]), len(a))[1])([1, 2, 3])` -> `4`
- B) `len([1, 2, 3])` -> `3`
- C) `(lambda a: (a.extend([4, 5]), len(a))[1])([1, 2, 3])` -> `5`
- D) `len([1, 2, 3] + [4, 5, 6])` -> `6`

*Explanation:* `append` adds the whole list as ONE element (length 4). `extend` would add its elements one by one (length 5).

**Q12. Answer: D**

- A) `d['a']` -> `1`
- B) `d.get('c')` -> `None`
- C) `len(d)` -> `2`
- D) `d.get('c', 0)` -> `0`

*Explanation:* `get` returns the default (0) when the key is missing, instead of raising a KeyError.

**Q13. Answer: C**

- A) `len(set([1, 2, 2]))` -> `2`
- B) `len([1, 2, 2, 3, 3, 3])` -> `6`
- C) `len(set([1, 2, 2, 3, 3, 3]))` -> `3`
- D) `len(set([3, 3, 3]))` -> `1`

*Explanation:* A set keeps only unique elements: {1, 2, 3}.

**Q14. Answer: B**

- A) `n = 1; s = 0; while n <= 5:;     s = s + n * n;     n = n + 1; s` -> `55`
- B) `n = 1; s = 0; while n <= 5:;     s = s + n;     n = n + 1; s` -> `15`
- C) `n = 1; s = 1; while n <= 5:;     s = s + n;     n = n + 1; s` -> `16`
- D) `n = 1; s = 0; while n < 5:;     s = s + n;     n = n + 1; s` -> `10`

*Explanation:* The loop adds 1+2+3+4+5 = 15.

**Q15. Answer: B**

- A) `list(range(2, 10))` -> `[2, 3, 4, 5, 6, 7, 8, 9]`
- B) `list(range(2, 10, 3))` -> `[2, 5, 8]`
- C) `list(range(3))` -> `[0, 1, 2]`
- D) `[2, 5, 8, 11]` -> `[2, 5, 8, 11]`

*Explanation:* `range(start, stop, step)` stops before `stop`: 2, 5, 8.

---

## Part B - Coding

**Q16.**

```python
age = 17
if age >= 18:
    print('Yes! the person is eligible to vote')
else:
    print('No, the person is not eligible to vote')
```

Output:

```text
No, the person is not eligible to vote
```

**Q17.**

```python
marks = 76
if marks >= 90:
    print('A')
elif marks >= 75:
    print('B')
elif marks >= 50:
    print('C')
else:
    print('Fail')
```

Output:

```text
B
```

**Q18.**

```python
units = 180
if units <= 50:
    cost = 0
elif units <= 150:
    cost = (units - 50) * 0.75
elif units <= 250:
    cost = 100 * 0.75 + (units - 150) * 1.20
else:
    cost = 100 * 0.75 + 100 * 1.20 + (units - 250) * 1.5
print('Total bill:', 10 + cost)
```

Output:

```text
Total bill: 121.0
```

**Q19.**

```python
n = 1
total = 0
while n <= 100:
    total = total + n
    n = n + 1
print(total)
```

Output:

```text
5050
```

**Q20.**

```python
n = 1
while n <= 20:
    if n % 2 == 0:
        print(n)
    n = n + 1
```

Output:

```text
2
4
6
8
10
12
14
16
18
20
```

**Q21.**

```python
for i in range(1, 6):
    print('7 x', i, '=', 7 * i)
```

Output:

```text
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
7 x 4 = 28
7 x 5 = 35
```

**Q22.**

```python
result = 1
for i in range(1, 7):
    result = result * i
print(result)
```

Output:

```text
720
```

**Q23.**

```python
s = 'madam'
print(s == s[::-1])
```

Output:

```text
True
```

**Q24.**

```python
s = 'Data Science with Python'
count = 0
for ch in s.lower():
    if ch in 'aeiou':
        count = count + 1
print(count)
```

Output:

```text
7
```

**Q25.**

```python
nums = [12, 45, 7, 89, 23]
biggest = nums[0]
for x in nums:
    if x > biggest:
        biggest = x
print(biggest)
```

Output:

```text
89
```

**Q26.**

```python
freq = {}
for ch in 'banana':
    freq[ch] = freq.get(ch, 0) + 1
print(freq)
```

Output:

```text
{'b': 1, 'a': 3, 'n': 2}
```

**Q27.**

```python
year = 2024
if (year % 4 == 0 and year % 100 != 0) or year % 400 == 0:
    print('Leap year')
else:
    print('Not a leap year')
```

Output:

```text
Leap year
```

**Q28.**

```python
n = 29
is_prime = n > 1
for i in range(2, n):
    if n % i == 0:
        is_prime = False
        break
print(is_prime)
```

Output:

```text
True
```

**Q29.**

```python
squares = []
for i in range(1, 11):
    if i % 2 == 1:
        squares.append(i ** 2)
print(squares)
```

Output:

```text
[1, 9, 25, 49, 81]
```

**Q30.**

```python
for i in range(1, 16):
    if i % 15 == 0:
        print('FizzBuzz')
    elif i % 3 == 0:
        print('Fizz')
    elif i % 5 == 0:
        print('Buzz')
    else:
        print(i)
```

Output:

```text
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
```

