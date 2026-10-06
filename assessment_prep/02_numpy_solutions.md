# Section 2 - NumPy (fitness / Fitbit data) - Solutions

## Part A - Multiple choice

**Q31. Answer: A**

- A) `data.shape` -> `(96, 7)`
- B) `(97, 7)` -> `(97, 7)`
- C) `(96,)` -> `(96,)`
- D) `(7, 96)` -> `(7, 96)`

*Explanation:* 96 days (rows) and 7 columns. The header line starting with `#` is ignored by `loadtxt`.

**Q32. Answer: C**

- A) `1` -> `1`
- B) `3` -> `3`
- C) `data.ndim` -> `2`
- D) `7` -> `7`

*Explanation:* `data` is a 2-D array (rows x columns).

**Q33. Answer: D**

- A) `'int64'` -> `'int64'`
- B) `'float64'` -> `'float64'`
- C) `'object'` -> `'object'`
- D) `str(data.dtype)` -> `'<U10'`

*Explanation:* We loaded the file with `dtype='str'` because the first column contains dates. So every value is a string and the numeric columns must be converted with `astype('int')`.

**Q34. Answer: C**

- A) `steps.max()` -> `7422`
- B) `steps.sum() // 7` -> `40264`
- C) `steps.sum()` -> `281850`
- D) `steps.mean()` -> `2935.9375`

*Explanation:* `sum` adds all the elements.

**Q35. Answer: B**

- A) `steps.argmax()` -> `69`
- B) `steps.max()` -> `7422`
- C) `steps.min()` -> `25`
- D) `steps.sum()` -> `281850`

**Q36. Answer: D**

- A) `steps.argmax() + 1` -> `70`
- B) `steps.max()` -> `7422`
- C) `steps.argmin()` -> `2`
- D) `steps.argmax()` -> `69`

*Explanation:* `argmax` returns the POSITION of the maximum, not the maximum itself.

**Q37. Answer: B**

- A) `date[-1]` -> `'09-01-2018'`
- B) `date[steps.argmax()]` -> `'14-12-2017'`
- C) `date[0]` -> `'06-10-2017'`
- D) `date[steps.argmin()]` -> `'08-10-2017'`

*Explanation:* Use the position given by `argmax` to index the date array.

**Q38. Answer: A**

- A) `np.round(steps.mean(), 2)` -> `2935.94`
- B) `np.round(np.median(steps), 2)` -> `2987.5`
- C) `np.round(steps.sum() / 97, 2)` -> `2905.67`
- D) `np.round(steps.std(), 2)` -> `2132.19`

**Q39. Answer: A**

- A) `np.median(steps)` -> `2987.5`
- B) `steps.max() / 2` -> `3711.0`
- C) `steps.mean()` -> `2935.9375`
- D) `np.median(steps) + 1` -> `2988.5`

**Q40. Answer: D**

- A) `(steps < 4000).sum()` -> `58`
- B) `(steps > 3000).sum()` -> `48`
- C) `steps[steps > 4000].sum()` -> `196514`
- D) `(steps > 4000).sum()` -> `38`

*Explanation:* `steps > 4000` is a boolean array; `sum` counts the True values.

**Q41. Answer: A**

- A) `calories.sum()` -> `8971`
- B) `calories.max()` -> `243`
- C) `calories.mean()` -> `93.44791666666667`
- D) `steps.sum()` -> `281850`

**Q42. Answer: A**

- A) `np.unique(mood)` -> `[100, 200, 300]`
- B) `mood[:3]` -> `[200, 100, 100]`
- C) `np.unique(sleep)` -> `[2, 3, 4, 5, 6, 7, 8, 9]`
- D) `np.sort(mood)[:3]` -> `[100, 100, 100]`

*Explanation:* Mood is stored as 100 (sad), 200 (neutral) and 300 (happy).

**Q43. Answer: A**

- A) `len(np.unique(sleep))` -> `8`
- B) `len(sleep)` -> `96`
- C) `sleep.min()` -> `2`
- D) `sleep.max()` -> `9`

**Q44. Answer: C**

- A) `weight.mean()` -> `64.28125`
- B) `weight.max()` -> `66`
- C) `weight.min()` -> `64`
- D) `weight.argmin()` -> `18`

**Q45. Answer: C**

- A) `steps[:4].sum()` -> `16991`
- B) `steps[1:5].sum()` -> `18442`
- C) `steps[:5].sum()` -> `23906`
- D) `steps[-5:].sum()` -> `5116`

**Q46. Answer: B**

- A) `steps[3:].tolist()[:3]` -> `[5461, 6915, 4545]`
- B) `steps[-3:].tolist()` -> `[500, 2127, 2203]`
- C) `steps[:3].tolist()` -> `[5464, 6041, 25]`
- D) `steps[-4:-1].tolist()` -> `[153, 500, 2127]`

*Explanation:* A negative start counts from the end of the array.

**Q47. Answer: B**

- A) `steps[30:].tolist()[:4]` -> `[539, 5464, 6041, 4068]`
- B) `steps[::30].tolist()` -> `[5464, 539, 5934, 702]`
- C) `steps[::-30].tolist()` -> `[2203, 1648, 4033, 4545]`
- D) `steps[:30].tolist()[:4]` -> `[5464, 6041, 25, 5461]`

*Explanation:* A step of 30 picks every 30th element: indices 0, 30, 60, 90.

**Q48. Answer: B**

- A) `active.sum()` -> `21000`
- B) `(active == 500).sum()` -> `42`
- C) `(active > 500).sum()` -> `0`
- D) `(active == 0).sum()` -> `54`

**Q49. Answer: A**

- A) `np.sort(steps)[-3:].tolist()` -> `[6930, 7102, 7422]`
- B) `steps[-3:].tolist()` -> `[500, 2127, 2203]`
- C) `np.sort(steps)[:3].tolist()` -> `[25, 36, 61]`
- D) `np.sort(steps)[::-1][:3].tolist()` -> `[7422, 7102, 6930]`

**Q50. Answer: B**

- A) `np.argsort(steps)[-3:].tolist()` -> `[48, 67, 69]`
- B) `np.argsort(steps)[:3].tolist()` -> `[2, 86, 8]`
- C) `np.argsort(steps)[::-1][:3].tolist()` -> `[69, 67, 48]`
- D) `np.sort(steps)[:3].tolist()` -> `[25, 36, 61]`

*Explanation:* `argsort` returns indices that would sort the array, not the sorted values.

**Q51. Answer: D**

- A) `np.round(steps[mood != 300].mean(), 2)` -> `2609.66`
- B) `np.round(steps.mean(), 2)` -> `2935.94`
- C) `np.round(steps[mood == 100].mean(), 2)` -> `2103.07`
- D) `np.round(steps[mood == 300].mean(), 2)` -> `3392.72`

*Explanation:* A boolean mask keeps only the days where the condition is True.

**Q52. Answer: D**

- A) `((sleep >= 8) | (steps > 3000)).sum()` -> `53`
- B) `(sleep >= 8).sum()` -> `11`
- C) `((sleep > 8) & (steps > 3000)).sum()` -> `1`
- D) `((sleep >= 8) & (steps > 3000)).sum()` -> `6`

*Explanation:* Use `&` (and) / `|` (or) with parentheses on boolean arrays - not `and` / `or`.

**Q53. Answer: B**

- A) `np.all(calories > 0)` -> `False`
- B) `np.any(calories == 0)` -> `True`
- C) `np.all(calories == 0)` -> `False`
- D) `np.any(calories < 0)` -> `False`

*Explanation:* `any` is True if at least one element is True; `all` needs every element to be True.

**Q54. Answer: C**

- A) `np.all(weight < 66)` -> `False`
- B) `np.all(weight >= 66)` -> `False`
- C) `np.all(weight <= 66)` -> `True`
- D) `np.any(weight > 66)` -> `False`

*Explanation:* The weight never goes above 66, but it does equal 66 on the first day, so only `<= 66` holds for every day.

**Q55. Answer: B**

- A) `(calories < 0).sum()` -> `0`
- B) `(calories == 0).sum()` -> `5`
- C) `(calories < 10).sum()` -> `14`
- D) `(calories > 0).sum()` -> `91`

**Q56. Answer: C**

- A) `np.round(np.var(steps), 2)` -> `4546242.25`
- B) `np.round(steps.mean(), 2)` -> `2935.94`
- C) `np.round(np.std(steps), 2)` -> `2132.19`
- D) `np.round(np.std(calories), 2)` -> `71.23`

**Q57. Answer: C**

- A) `(4, 3)` -> `(4, 3)`
- B) `(12,)` -> `(12,)`
- C) `a.shape` -> `(3, 4)`
- D) `(3, 3)` -> `(3, 3)`

**Q58. Answer: A**

- A) `a[1, 2]` -> `6`
- B) `a[0, 2]` -> `2`
- C) `a[2, 1]` -> `9`
- D) `a[1][3]` -> `7`

*Explanation:* `a[row, column]` - row 1, column 2.

**Q59. Answer: C**

- A) `a.max(axis=0).tolist()` -> `[8, 9, 10, 11]`
- B) `a.sum(axis=1).tolist()` -> `[6, 22, 38]`
- C) `a.sum(axis=0).tolist()` -> `[12, 15, 18, 21]`
- D) `a.sum().tolist()` -> `66`

*Explanation:* `axis=0` collapses the rows, giving one value per column.

**Q60. Answer: C**

- A) `a.sum(axis=0).tolist()` -> `[12, 15, 18, 21]`
- B) `a.min(axis=1).tolist()` -> `[0, 4, 8]`
- C) `a.sum(axis=1).tolist()` -> `[6, 22, 38]`
- D) `a.mean(axis=1).tolist()` -> `[1.5, 5.5, 9.5]`

*Explanation:* `axis=1` collapses the columns, giving one value per row.

**Q61. Answer: A**

- A) `np.arange(2, 11, 3).tolist()` -> `[2, 5, 8]`
- B) `np.arange(2, 11).tolist()[:3]` -> `[2, 3, 4]`
- C) `np.arange(3, 11, 3).tolist()` -> `[3, 6, 9]`
- D) `np.arange(2, 12, 3).tolist() + [14]` -> `[2, 5, 8, 11, 14]`

*Explanation:* Like `range`, the stop value (11) is excluded.

**Q62. Answer: B**

- A) `np.linspace(0, 5, 5).tolist()` -> `[0.0, 1.25, 2.5, 3.75, 5.0]`
- B) `np.linspace(0, 1, 5).tolist()` -> `[0.0, 0.25, 0.5, 0.75, 1.0]`
- C) `np.linspace(0, 1, 4).tolist()` -> `[0.0, 0.3333333333333333, 0.6666666666666666, 1.0]`
- D) `np.arange(0, 1, 0.2).tolist()` -> `[0.0, 0.2, 0.4, 0.6000000000000001, 0.8]`

*Explanation:* `linspace` includes both end points and returns exactly the requested number of points.

**Q63. Answer: B**

- A) `(3, 4)` -> `(3, 4)`
- B) `np.zeros((2, 3, 4)).shape` -> `(2, 3, 4)`
- C) `(4, 3, 2)` -> `(4, 3, 2)`
- D) `(24,)` -> `(24,)`

**Q64. Answer: D**

- A) `[2, 3, 4]` -> `[2, 3, 4]`
- B) `[1, 2, 3, 1, 2, 3]` -> `[1, 2, 3, 1, 2, 3]`
- C) `[1, 4, 9]` -> `[1, 4, 9]`
- D) `(np.array([1, 2, 3]) * 2).tolist()` -> `[2, 4, 6]`

*Explanation:* NumPy operations are element-wise (unlike lists, where `*` repeats the list).

**Q65. Answer: A**

- A) `[1, 2, 3] * 2` -> `[1, 2, 3, 1, 2, 3]`
- B) `[1, 2, 3, 2]` -> `[1, 2, 3, 2]`
- C) `[2, 4, 6]` -> `[2, 4, 6]`
- D) `[2, 2, 2]` -> `[2, 2, 2]`

**Q66. Answer: C**

- A) `[10, 40, 90]` -> `[10, 40, 90]`
- B) `[11, 22]` -> `[11, 22]`
- C) `(np.array([1, 2, 3]) + np.array([10, 20, 30])).tolist()` -> `[11, 22, 33]`
- D) `[1, 2, 3, 10, 20, 30]` -> `[1, 2, 3, 10, 20, 30]`

**Q67. Answer: C**

- A) `(2,)` -> `(2,)`
- B) `(2, 3)` -> `(2, 3)`
- C) `(np.array([[1], [2], [3]]) + np.array([10, 20])).shape` -> `(3, 2)`
- D) `(3, 1)` -> `(3, 1)`

*Explanation:* Broadcasting: shapes (3,1) and (2,) stretch to (3,2).

**Q68. Answer: C**

- A) `(6, 2)` -> `(6, 2)`
- B) `(2, 2)` -> `(2, 2)`
- C) `np.array([1, 2, 3, 4, 5, 6]).reshape(2, -1).shape` -> `(2, 3)`
- D) `(3, 3)` -> `(3, 3)`

*Explanation:* `-1` lets NumPy work out that dimension: 6 / 2 = 3.

**Q69. Answer: B**

- A) `np.array([1, 2, 3]).dtype.name` -> `'int64'`
- B) `np.array([1, 2, 3.5]).dtype.name` -> `'float64'`
- C) `np.array([1, 2, '3']).dtype.name[:3]` -> `'str'`
- D) `np.array([True, 2]).dtype.name[:4]` -> `'int6'`

*Explanation:* NumPy upcasts to one common type: ints and a float become `float64`.

**Q70. Answer: A**

- A) `np.vstack([np.array([1, 2]), np.array([3, 4])]).tolist()` -> `[[1, 2], [3, 4]]`
- B) `[[3, 4], [1, 2]]` -> `[[3, 4], [1, 2]]`
- C) `np.hstack([np.array([1, 2]), np.array([3, 4])]).tolist()` -> `[1, 2, 3, 4]`
- D) `[[1, 3], [2, 4]]` -> `[[1, 3], [2, 4]]`

*Explanation:* `vstack` stacks vertically (as rows); `hstack` joins side by side.

**Q71. Answer: B**

- A) `[0, 1, 0, 1][::-1]` -> `[1, 0, 1, 0]`
- B) `np.where(np.array([5, 12, 7, 20]) > 10, 1, 0).tolist()` -> `[0, 1, 0, 1]`
- C) `[12, 20]` -> `[12, 20]`
- D) `np.where(np.array([5, 12, 7, 20]) > 10)[0].tolist()` -> `[1, 3]`

*Explanation:* With 3 arguments `np.where(cond, x, y)` picks x where True and y otherwise.

**Q72. Answer: D**

- A) `[12, 20]` -> `[12, 20]`
- B) `[True, False, True, False]` -> `[True, False, True, False]`
- C) `[0, 2]` -> `[0, 2]`
- D) `np.where(np.array([5, 12, 7, 20]) > 10)[0].tolist()` -> `[1, 3]`

*Explanation:* With only a condition, `np.where` returns the INDICES where it is True.

**Q73. Answer: B**

- A) `[3, 1, 2]` -> `[3, 1, 2]`
- B) `np.array([3, 1, 2])[np.array([True, False, True])].tolist()` -> `[3, 2]`
- C) `[1]` -> `[1]`
- D) `[True, False, True]` -> `[True, False, True]`

**Q74. Answer: C**

- A) `np.shares_memory(a, a[:2].copy())` -> `False`
- B) `np.shares_memory(a, a[[0, 1]])` -> `False`
- C) `np.shares_memory(a, a[:2])` -> `True`
- D) `np.shares_memory(a, np.arange(5))` -> `False`

*Explanation:* A basic slice is a VIEW (shares memory). `.copy()` or fancy indexing creates a new array.

**Q75. Answer: D**

- A) `[1, 2, 3]` -> `[1, 2, 3]`
- B) `[3, 2, 2]` -> `[3, 2, 2]`
- C) `[2, 2, 1]` -> `[2, 2, 1]`
- D) `np.unique(np.array([3, 1, 3, 2, 1]), return_counts=True)[1].tolist()` -> `[2, 1, 2]`

*Explanation:* Unique values are 1, 2, 3 (sorted); their counts are 2, 1, 2.

**Q76. Answer: B**

- A) `np.ones((3, 3)).sum()` -> `9.0`
- B) `np.identity(3).sum()` -> `3.0`
- C) `np.identity(3).shape[0] ** 2` -> `9`
- D) `np.zeros((3, 3)).sum()` -> `0.0`

**Q77. Answer: A**

- A) `np.dot(np.array([1, 2, 3]), np.array([4, 5, 6]))` -> `32`
- B) `np.dot(np.array([1, 2, 3]), np.array([1, 2, 3]))` -> `14`
- C) `np.sum(np.array([1, 2, 3]) + np.array([4, 5, 6]))` -> `21`
- D) `np.array([4, 5, 6]).sum()` -> `15`

*Explanation:* 1*4 + 2*5 + 3*6 = 32.

**Q78. Answer: B**

- A) `np.arange(10)[2::3].tolist()` -> `[2, 5, 8]`
- B) `np.arange(10)[2:8:2].tolist()` -> `[2, 4, 6]`
- C) `np.arange(10)[2:9:2].tolist() + [8]` -> `[2, 4, 6, 8, 8]`
- D) `np.arange(10)[2:8].tolist()` -> `[2, 3, 4, 5, 6, 7]`

*Explanation:* start 2, stop 8 (excluded), step 2: 2, 4, 6.

**Q79. Answer: B**

- A) `np.argsort(np.array([3, 1, 2])).tolist()` -> `[1, 2, 0]`
- B) `np.sort(np.array([3, 1, 2]))[::-1].tolist()` -> `[3, 2, 1]`
- C) `np.sort(np.array([3, 1, 2])).tolist()` -> `[1, 2, 3]`
- D) `np.array([3, 1, 2]).tolist()` -> `[3, 1, 2]`

*Explanation:* `sort` returns ascending values; `[::-1]` reverses them. `argsort` returns indices instead.

---

## Part B - Coding

**Q80.**

```python
data = np.loadtxt('fitness.txt', dtype='str')
print(data.shape)
```

Output:

```text
(96, 7)
```

**Q81.**

```python
print(steps[:5])
```

Output:

```text
[5464 6041   25 5461 6915]
```

**Q82.**

```python
print(steps.sum())
print(calories.sum())
print(len(date))
```

Output:

```text
281850
8971
96
```

**Q83.**

```python
i = steps.argmin()
print(date[i], steps[i])
```

Output:

```text
08-10-2017 25
```

**Q84.**

```python
print(np.round(steps.mean(), 2))
```

Output:

```text
2935.94
```

**Q85.**

```python
print(date[:7])
print(steps[:7])
```

Output:

```text
['06-10-2017' '07-10-2017' '08-10-2017' '09-10-2017' '10-10-2017'
 '11-10-2017' '12-10-2017']
[5464 6041   25 5461 6915 4545 4340]
```

**Q86.**

```python
mask = steps > 5000
print(mask.sum())
print(date[mask])
```

Output:

```text
17
['06-10-2017' '07-10-2017' '09-10-2017' '10-10-2017' '06-11-2017'
 '07-11-2017' '11-11-2017' '21-11-2017' '23-11-2017' '24-11-2017'
 '29-11-2017' '05-12-2017' '12-12-2017' '14-12-2017' '20-12-2017'
 '26-12-2017' '28-12-2017']
```

**Q87.**

```python
print(np.round(calories[active == 500].mean(), 2))
print(np.round(calories[active == 0].mean(), 2))
```

Output:

```text
102.4
86.48
```

**Q88.**

```python
for m in np.unique(mood):
    print(m, np.round(steps[mood == m].mean(), 2))
```

Output:

```text
100 2103.07
200 3153.78
300 3392.72
```

**Q89.**

```python
values, counts = np.unique(mood, return_counts=True)
print(values)
print(counts)
```

Output:

```text
[100 200 300]
[29 27 40]
```

**Q90.**

```python
idx = np.argsort(steps)[::-1][:5]
print(date[idx])
print(steps[idx])
```

Output:

```text
['14-12-2017' '12-12-2017' '23-11-2017' '10-10-2017' '29-11-2017']
[7422 7102 6930 6915 6676]
```

**Q91.**

```python
values, counts = np.unique(sleep, return_counts=True)
print(values)
print(counts)
```

Output:

```text
[2 3 4 5 6 7 8 9]
[ 3  9 14 37 16  6 10  1]
```

**Q92.**

```python
n = (sleep < 5).sum()
print(n)
print(np.round(n / len(sleep) * 100, 2))
```

Output:

```text
26
27.08
```

**Q93.**

```python
print(np.round(steps[sleep >= 8].mean(), 2))
print(np.round(steps[sleep < 5].mean(), 2))
```

Output:

```text
2874.45
2466.5
```

**Q94.**

```python
activity = np.where(steps > 4000, 'Active', 'Lazy')
values, counts = np.unique(activity, return_counts=True)
print(values)
print(counts)
```

Output:

```text
['Active' 'Lazy']
[38 58]
```

**Q95.**

```python
print(((steps > 3000) & (mood == 300)).sum())
```

Output:

```text
24
```

**Q96.**

```python
print(weight[-1] - weight[0])
```

Output:

```text
-2
```

**Q97.**

```python
mask = steps > 0
cal_per_step = calories[mask] / steps[mask]
print(np.round(cal_per_step.mean(), 4))
```

Output:

```text
0.0302
```

**Q98.**

```python
z = (steps - steps.mean()) / steps.std()
print(np.round(z[:5], 2))
```

Output:

```text
[ 1.19  1.46 -1.37  1.18  1.87]
```

**Q99.**

```python
weeks = steps[:84].reshape(12, 7)
print(weeks.sum(axis=1))
```

Output:

```text
[32791 18635 20042 16797 24881 27131 23169 18676 20506 26195 18581 21004]
```

**Q100.**

```python
weeks = steps[:84].reshape(12, 7)
print(weeks.sum(axis=1).argmax())
```

Output:

```text
0
```

**Q101.**

```python
weeks = steps[:84].reshape(12, 7)
print(np.round(weeks.mean(axis=0), 2))
```

Output:

```text
[2323.83 2092.75  989.17 3068.5  4711.42 4504.5  4677.17]
```

**Q102.**

```python
stacked = np.vstack([steps, calories, sleep])
print(stacked.shape)
print(stacked[1, :5])
```

Output:

```text
(3, 96)
[181 197   0 174 223]
```

**Q103.**

```python
both = np.hstack([steps.reshape(-1, 1), calories.reshape(-1, 1)])
print(both.shape)
```

Output:

```text
(96, 2)
```

**Q104.**

```python
print(np.concatenate([steps[:3], steps[-3:]]))
```

Output:

```text
[5464 6041   25  500 2127 2203]
```

**Q105.**

```python
print(date[::10])
```

Output:

```text
['06-10-2017' '16-10-2017' '26-10-2017' '05-11-2017' '15-11-2017'
 '25-11-2017' '05-12-2017' '15-12-2017' '25-12-2017' '04-01-2018']
```

**Q106.**

```python
print(steps[::-1][:5])
```

Output:

```text
[2203 2127  500  153  133]
```

**Q107.**

```python
print(np.any(calories == 0))
print((calories == 0).sum())
```

Output:

```text
True
5
```

**Q108.**

```python
cal = calories.copy()
cal[cal == 0] = int(round(cal[cal > 0].mean()))
print((cal == 0).sum())
print((calories == 0).sum())
```

Output:

```text
0
5
```

**Q109.**

```python
s = steps.copy()
s[s > 6000] = 6000
print(s.max())
```

Output:

```text
6000
```

**Q110.**

```python
label = np.vectorize(lambda c: 'High' if c > 150 else 'Low')(calories)
print((label == 'High').sum())
```

Output:

```text
22
```

**Q111.**

```python
I = np.identity(3)
A = np.arange(1, 10).reshape(3, 3)
print(np.matmul(A, I))
```

Output:

```text
[[1. 2. 3.]
 [4. 5. 6.]
 [7. 8. 9.]]
```

**Q112.**

```python
print(np.linspace(10, 50, 5))
```

Output:

```text
[10. 20. 30. 40. 50.]
```

**Q113.**

```python
a = np.ones((4, 4))
np.fill_diagonal(a, 5)
print(a)
```

Output:

```text
[[5. 1. 1. 1.]
 [1. 5. 1. 1.]
 [1. 1. 5. 1.]
 [1. 1. 1. 5.]]
```

**Q114.**

```python
a = np.arange(1, 13).reshape(3, 4)
print(a.T)
print(a.T.shape)
```

Output:

```text
[[ 1  5  9]
 [ 2  6 10]
 [ 3  7 11]
 [ 4  8 12]]
(4, 3)
```

**Q115.**

```python
print(np.split(np.arange(12), 3))
```

Output:

```text
[array([0, 1, 2, 3]), array([4, 5, 6, 7]), array([ 8,  9, 10, 11])]
```

**Q116.**

```python
print(np.tile([1, 2, 3], 4))
```

Output:

```text
[1 2 3 1 2 3 1 2 3 1 2 3]
```

**Q117.**

```python
print(data[:3, -2:])
```

Output:

```text
[['0' '66']
 ['0' '66']
 ['0' '66']]
```

**Q118.**

```python
print(np.round(data[:, 1:].astype('int').mean(axis=0), 2))
```

Output:

```text
[2935.94  211.46   93.45    5.22  218.75   64.28]
```

**Q119.**

```python
num = data[:, 1:].astype('int')
centered = num - num.mean(axis=0)
print(np.round(centered[0], 2))
```

Output:

```text
[ 2.52806e+03 -1.14600e+01  8.75500e+01 -2.20000e-01 -2.18750e+02
  1.72000e+00]
```

**Q120.**

```python
a = np.arange(10)
print(np.shares_memory(a, a[:5]))
print(np.shares_memory(a, a[:5].copy()))
```

Output:

```text
True
False
```

**Q121.**

```python
a = np.array([1, 2, 3])[:, np.newaxis]
b = np.array([10, 20, 30])
print(a + b)
print((a + b).shape)
```

Output:

```text
[[11 21 31]
 [12 22 32]
 [13 23 33]]
(3, 3)
```

**Q122.**

```python
print(((steps > steps.mean()) & (calories > calories.mean())).sum())
```

Output:

```text
48
```

**Q123.**

```python
i = calories.argmax()
print(date[i], steps[i], calories[i])
```

Output:

```text
14-12-2017 7422 243
```

**Q124.**

```python
idx = np.argsort(sleep)
print(sleep[idx][:5])
print(date[idx][:5])
```

Output:

```text
[2 2 2 3 3]
['08-11-2017' '03-01-2018' '05-01-2018' '07-11-2017' '10-12-2017']
```

**Q125.**

```python
print(np.round(np.corrcoef(steps, calories)[0, 1], 3))
```

Output:

```text
0.989
```

**Q126.**

```python
print(np.percentile(steps, [25, 50, 75]))
```

Output:

```text
[ 741.   2987.5  4546.25]
```

**Q127.**

```python
print((steps < 2000).sum())
print(((steps >= 2000) & (steps < 5000)).sum())
print((steps >= 5000).sum())
```

Output:

```text
39
40
17
```

**Q128.**

```python
print(np.round(calories.mean(), 2))
print(np.round(calories.std(), 2))
```

Output:

```text
93.45
71.23
```

**Q129.**

```python
print(date[sleep == sleep.min()])
```

Output:

```text
['08-11-2017' '03-01-2018' '05-01-2018']
```

**Q130.**

```python
a = np.array([[1, 2, 3], [4, 5, 6]])
print(a.sum())
print(a.mean(axis=0))
print(a.max(axis=1))
```

Output:

```text
21
[2.5 3.5 4.5]
[3 6]
```

