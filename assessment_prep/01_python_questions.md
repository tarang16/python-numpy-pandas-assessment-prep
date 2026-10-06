# Section 1 - Python Fundamentals

## Part A - Multiple choice (15)

**Q1.** What is the value of `-10 // 3`?

- **A)** `2`
- **B)** `-4`
- **C)** `-3.3333333333333335`
- **D)** `-3`

**Q2.** What is the value of `5 ** -1`?

- **A)** `-5`
- **B)** `25`
- **C)** `0.2`
- **D)** `1`

**Q3.** Which of the following expressions evaluates to `False`?

- **A)** `bool('false')`
- **B)** `bool(' ')`
- **C)** `bool('')`
- **D)** `bool(-123)`

**Q4.** What is the data type of the result of `10 / 5`?

- **A)** `'float'`
- **B)** `'int'`
- **C)** `'str'`
- **D)** `'bool'`

**Q5.** What does `2 + 3 * 4 ** 2` evaluate to?

- **A)** `50`
- **B)** `196`
- **C)** `80`
- **D)** `26`

**Q6.** What does `7 % 3 + 7 // 3` evaluate to?

- **A)** `2`
- **B)** `-1`
- **C)** `4`
- **D)** `3`

**Q7.** What is the value of `len('Data Science')`?

- **A)** `4`
- **B)** `13`
- **C)** `12`
- **D)** `11`

**Q8.** What is the value of `'Python'[1:4]`?

- **A)** `'yth'`
- **B)** `'ytho'`
- **C)** `'Pyt'`
- **D)** `'th'`

**Q9.** What is the value of `'Python'[::-1]`?

- **A)** `'ytho'`
- **B)** `'nohty'`
- **C)** `'Python'`
- **D)** `'nohtyP'`

**Q10.** Given `a = [1, 2, 3, 4, 5]`, what is `a[-2:]`?

```python
a = [1, 2, 3, 4, 5]
```

- **A)** `[4, 5]`
- **B)** `4`
- **C)** `[3, 4, 5]`
- **D)** `[1, 2]`

**Q11.** `a = [1, 2, 3]`. After `a.append([4, 5])`, what is `len(a)`?

- **A)** `4`
- **B)** `3`
- **C)** `5`
- **D)** `6`

**Q12.** Given `d = {'a': 1, 'b': 2}`, what does `d.get('c', 0)` return?

```python
d = {'a': 1, 'b': 2}
```

- **A)** `1`
- **B)** `None`
- **C)** `2`
- **D)** `0`

**Q13.** What is `len(set([1, 2, 2, 3, 3, 3]))`?

- **A)** `2`
- **B)** `6`
- **C)** `3`
- **D)** `1`

**Q14.** What is the value of `s` at the end of this code?

```python
n = 1
s = 0
while n <= 5:
    s = s + n
    n = n + 1
```

- **A)** `55`
- **B)** `15`
- **C)** `16`
- **D)** `10`

**Q15.** What is `list(range(2, 10, 3))`?

- **A)** `[2, 3, 4, 5, 6, 7, 8, 9]`
- **B)** `[2, 5, 8]`
- **C)** `[0, 1, 2]`
- **D)** `[2, 5, 8, 11]`

---

## Part B - Coding (15)

**Q16.** Write a program that checks whether a person is eligible to vote (age >= 18). Test with `age = 17`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q17.** Marks are given. Print the grade: `A` for 90 and above, `B` for 75-89, `C` for 50-74, else `Fail`. Test with `marks = 76`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q18.** Electricity bill: base fee 10. First 50 units are free, units 51-150 cost 0.75 each, units 151-250 cost 1.20 each, beyond 250 cost 1.5 each. Print the total bill for `units = 180`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q19.** Using a `while` loop, print the sum of the numbers from 1 to 100.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q20.** Using a `while` loop, print all the even numbers from 1 to 20 (one per line).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q21.** Print the multiplication table of 7 (from 7 x 1 to 7 x 5).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q22.** Print the factorial of 6 using a loop.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q23.** Check whether the string `'madam'` is a palindrome and print `True` or `False`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q24.** Count the number of vowels in the string `'Data Science with Python'` (ignore case).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q25.** Find the largest number of the list `[12, 45, 7, 89, 23]` without using `max()`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q26.** Create a dictionary with the frequency of every character in `'banana'` and print it.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q27.** Print whether `year = 2024` is a leap year (divisible by 4 and not by 100, or divisible by 400).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q28.** Check whether `29` is a prime number and print the result.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q29.** Create a list of the squares of all odd numbers from 1 to 10 using a `for` loop.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q30.** Print the numbers from 1 to 15, but print `Fizz` for multiples of 3, `Buzz` for multiples of 5 and `FizzBuzz` for multiples of both.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

