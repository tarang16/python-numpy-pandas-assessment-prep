# Section 2 - NumPy (fitness / Fitbit data)

Run this set-up first (keep the data files in the same folder as your notebook):

```python
import numpy as np
data = np.loadtxt('fitness.txt', dtype='str')
date     = data[:, 0]
steps    = data[:, 1].astype('int')
mood     = data[:, 2].astype('int')
calories = data[:, 3].astype('int')
sleep    = data[:, 4].astype('int')
active   = data[:, 5].astype('int')
weight   = data[:, 6].astype('int')
```

## Part A - Multiple choice (49)

**Q31.** What is `data.shape`?

- **A)** `(96, 7)`
- **B)** `(97, 7)`
- **C)** `(96,)`
- **D)** `(7, 96)`

**Q32.** What is `data.ndim`?

- **A)** `1`
- **B)** `3`
- **C)** `2`
- **D)** `7`

**Q33.** What is the `dtype` of `data`? (the file is loaded with `dtype='str'` because the first column holds dates)

- **A)** `'int64'`
- **B)** `'float64'`
- **C)** `'object'`
- **D)** `'<U10'`

**Q34.** What is the total number of steps walked, `steps.sum()`?

- **A)** `7422`
- **B)** `40264`
- **C)** `281850`
- **D)** `2935.9375`

**Q35.** What is the maximum number of steps in a day?

- **A)** `69`
- **B)** `7422`
- **C)** `25`
- **D)** `281850`

**Q36.** On which day (as an index) were the maximum steps walked?

- **A)** `70`
- **B)** `7422`
- **C)** `2`
- **D)** `69`

**Q37.** Which date had the maximum number of steps?

- **A)** `'09-01-2018'`
- **B)** `'14-12-2017'`
- **C)** `'06-10-2017'`
- **D)** `'08-10-2017'`

**Q38.** What is the average number of steps per day (rounded to 2 decimals)?

- **A)** `2935.94`
- **B)** `2987.5`
- **C)** `2905.67`
- **D)** `2132.19`

**Q39.** What is the median number of steps per day?

- **A)** `2987.5`
- **B)** `3711.0`
- **C)** `2935.9375`
- **D)** `2988.5`

**Q40.** On how many days were more than 4000 steps walked?

- **A)** `58`
- **B)** `48`
- **C)** `196514`
- **D)** `38`

**Q41.** What is the total number of calories burned?

- **A)** `8971`
- **B)** `243`
- **C)** `93.44791666666667`
- **D)** `281850`

**Q42.** What are the unique mood values?

- **A)** `[100, 200, 300]`
- **B)** `[200, 100, 100]`
- **C)** `[2, 3, 4, 5, 6, 7, 8, 9]`
- **D)** `[100, 100, 100]`

**Q43.** How many different values of hours of sleep occur?

- **A)** `8`
- **B)** `96`
- **C)** `2`
- **D)** `9`

**Q44.** What is the minimum weight recorded?

- **A)** `64.28125`
- **B)** `66`
- **C)** `64`
- **D)** `18`

**Q45.** What is the sum of the steps of the first 5 days?

- **A)** `16991`
- **B)** `18442`
- **C)** `23906`
- **D)** `5116`

**Q46.** What does `steps[-3:]` return?

- **A)** `[5461, 6915, 4545]`
- **B)** `[500, 2127, 2203]`
- **C)** `[5464, 6041, 25]`
- **D)** `[153, 500, 2127]`

**Q47.** What does `steps[::30]` return?

- **A)** `[539, 5464, 6041, 4068]`
- **B)** `[5464, 539, 5934, 702]`
- **C)** `[2203, 1648, 4033, 4545]`
- **D)** `[5464, 6041, 25, 5461]`

**Q48.** On how many days was the `active` flag equal to 500?

- **A)** `21000`
- **B)** `42`
- **C)** `0`
- **D)** `54`

**Q49.** What are the 3 largest values of `steps` (in ascending order)?

- **A)** `[6930, 7102, 7422]`
- **B)** `[500, 2127, 2203]`
- **C)** `[25, 36, 61]`
- **D)** `[7422, 7102, 6930]`

**Q50.** What are the indices of the 3 days with the fewest steps?

- **A)** `[48, 67, 69]`
- **B)** `[2, 86, 8]`
- **C)** `[69, 67, 48]`
- **D)** `[25, 36, 61]`

**Q51.** What is the average number of steps on the days when mood was 300 (happy), rounded to 2 decimals?

- **A)** `2609.66`
- **B)** `2935.94`
- **C)** `2103.07`
- **D)** `3392.72`

**Q52.** How many days had sleep of at least 8 hours AND more than 3000 steps?

- **A)** `53`
- **B)** `11`
- **C)** `1`
- **D)** `6`

**Q53.** Which of the following expressions is `True`?

- **A)** `np.all(calories > 0)`
- **B)** `np.any(calories == 0)`
- **C)** `np.all(calories == 0)`
- **D)** `np.any(calories < 0)`

**Q54.** Which of the following expressions is `True` for the weight data?

- **A)** `np.all(weight < 66)`
- **B)** `np.all(weight >= 66)`
- **C)** `np.all(weight <= 66)`
- **D)** `np.any(weight > 66)`

**Q55.** How many days had calories burned equal to 0?

- **A)** `0`
- **B)** `5`
- **C)** `14`
- **D)** `91`

**Q56.** What is `np.round(np.std(steps), 2)`?

- **A)** `4546242.25`
- **B)** `2935.94`
- **C)** `2132.19`
- **D)** `71.23`

**Q57.** Given `a = np.arange(12).reshape(3, 4)`, what is `a.shape`?

```python
a = np.arange(12).reshape(3, 4)
```

- **A)** `(4, 3)`
- **B)** `(12,)`
- **C)** `(3, 4)`
- **D)** `(3, 3)`

**Q58.** Given `a = np.arange(12).reshape(3, 4)`, what is `a[1, 2]`?

```python
a = np.arange(12).reshape(3, 4)
```

- **A)** `6`
- **B)** `2`
- **C)** `9`
- **D)** `7`

**Q59.** Given `a = np.arange(12).reshape(3, 4)`, what is `a.sum(axis=0)`?

```python
a = np.arange(12).reshape(3, 4)
```

- **A)** `[8, 9, 10, 11]`
- **B)** `[6, 22, 38]`
- **C)** `[12, 15, 18, 21]`
- **D)** `66`

**Q60.** Given `a = np.arange(12).reshape(3, 4)`, what is `a.sum(axis=1)`?

```python
a = np.arange(12).reshape(3, 4)
```

- **A)** `[12, 15, 18, 21]`
- **B)** `[0, 4, 8]`
- **C)** `[6, 22, 38]`
- **D)** `[1.5, 5.5, 9.5]`

**Q61.** What is `np.arange(2, 11, 3)`?

- **A)** `[2, 5, 8]`
- **B)** `[2, 3, 4]`
- **C)** `[3, 6, 9]`
- **D)** `[2, 5, 8, 11, 14]`

**Q62.** What is `np.linspace(0, 1, 5)`?

- **A)** `[0.0, 1.25, 2.5, 3.75, 5.0]`
- **B)** `[0.0, 0.25, 0.5, 0.75, 1.0]`
- **C)** `[0.0, 0.3333333333333333, 0.6666666666666666, 1.0]`
- **D)** `[0.0, 0.2, 0.4, 0.6000000000000001, 0.8]`

**Q63.** What is the shape of `np.zeros((2, 3, 4))`?

- **A)** `(3, 4)`
- **B)** `(2, 3, 4)`
- **C)** `(4, 3, 2)`
- **D)** `(24,)`

**Q64.** What is `np.array([1, 2, 3]) * 2`?

- **A)** `[2, 3, 4]`
- **B)** `[1, 2, 3, 1, 2, 3]`
- **C)** `[1, 4, 9]`
- **D)** `[2, 4, 6]`

**Q65.** What is `[1, 2, 3] * 2` (a Python list)?

- **A)** `[1, 2, 3, 1, 2, 3]`
- **B)** `[1, 2, 3, 2]`
- **C)** `[2, 4, 6]`
- **D)** `[2, 2, 2]`

**Q66.** What is `np.array([1, 2, 3]) + np.array([10, 20, 30])`?

- **A)** `[10, 40, 90]`
- **B)** `[11, 22]`
- **C)** `[11, 22, 33]`
- **D)** `[1, 2, 3, 10, 20, 30]`

**Q67.** What is the result of `(np.array([[1], [2], [3]]) + np.array([10, 20])).shape`?

- **A)** `(2,)`
- **B)** `(2, 3)`
- **C)** `(3, 2)`
- **D)** `(3, 1)`

**Q68.** What is `np.array([1, 2, 3, 4, 5, 6]).reshape(2, -1).shape`?

- **A)** `(6, 2)`
- **B)** `(2, 2)`
- **C)** `(2, 3)`
- **D)** `(3, 3)`

**Q69.** What is the dtype name of `np.array([1, 2, 3.5])`?

- **A)** `'int64'`
- **B)** `'float64'`
- **C)** `'str'`
- **D)** `'int6'`

**Q70.** What is `np.vstack([np.array([1, 2]), np.array([3, 4])]).tolist()`?

- **A)** `[[1, 2], [3, 4]]`
- **B)** `[[3, 4], [1, 2]]`
- **C)** `[1, 2, 3, 4]`
- **D)** `[[1, 3], [2, 4]]`

**Q71.** What is `np.where(np.array([5, 12, 7, 20]) > 10, 1, 0)`?

- **A)** `[1, 0, 1, 0]`
- **B)** `[0, 1, 0, 1]`
- **C)** `[12, 20]`
- **D)** `[1, 3]`

**Q72.** What does `np.where(np.array([5, 12, 7, 20]) > 10)` return (as a list of indices)?

- **A)** `[12, 20]`
- **B)** `[True, False, True, False]`
- **C)** `[0, 2]`
- **D)** `[1, 3]`

**Q73.** What is `np.array([3, 1, 2])[np.array([True, False, True])]`?

- **A)** `[3, 1, 2]`
- **B)** `[3, 2]`
- **C)** `[1]`
- **D)** `[True, False, True]`

**Q74.** `a = np.arange(5)`. Which of these is `True`, i.e. which result shares memory with `a` (changing it changes `a`)?

```python
a = np.arange(5)
```

- **A)** `np.shares_memory(a, a[:2].copy())`
- **B)** `np.shares_memory(a, a[[0, 1]])`
- **C)** `np.shares_memory(a, a[:2])`
- **D)** `np.shares_memory(a, np.arange(5))`

**Q75.** What is `np.unique(np.array([3, 1, 3, 2, 1]), return_counts=True)[1].tolist()`?

- **A)** `[1, 2, 3]`
- **B)** `[3, 2, 2]`
- **C)** `[2, 2, 1]`
- **D)** `[2, 1, 2]`

**Q76.** What is `np.identity(3).sum()`?

- **A)** `9.0`
- **B)** `3.0`
- **C)** `9`
- **D)** `0.0`

**Q77.** What is `np.dot(np.array([1, 2, 3]), np.array([4, 5, 6]))`?

- **A)** `32`
- **B)** `14`
- **C)** `21`
- **D)** `15`

**Q78.** What is `np.arange(10)[2:8:2]`?

- **A)** `[2, 5, 8]`
- **B)** `[2, 4, 6]`
- **C)** `[2, 4, 6, 8, 8]`
- **D)** `[2, 3, 4, 5, 6, 7]`

**Q79.** What is `np.sort(np.array([3, 1, 2]))[::-1]`?

- **A)** `[1, 2, 0]`
- **B)** `[3, 2, 1]`
- **C)** `[1, 2, 3]`
- **D)** `[3, 1, 2]`

---

## Part B - Coding (51)

**Q80.** Load `fitness.txt` as strings and print the shape of the loaded array.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q81.** Split the loaded data into separate arrays and print the first 5 values of `steps` (convert to integers).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q82.** Print the total number of steps, the total calories burned and the number of days in the data.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q83.** Print the date on which the minimum steps were walked and the number of steps on that day.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q84.** Print the average steps per day, rounded to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q85.** Print the first 7 dates and the steps walked on them, i.e. the first week of data.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q86.** Create a boolean mask for the days with `steps > 5000` and print how many days there are and their dates.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q87.** Print the average calories burned on the days where `active` is 500 and on the days where it is 0 (rounded to 2 decimals).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q88.** Find the average steps for each of the three mood values (100, 200, 300), rounded to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q89.** Count how many days there were for each mood value using `np.unique` with `return_counts`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q90.** Print the dates of the 5 days with the highest step count (most steps first).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q91.** Print the sorted unique values of `sleep` and how many days had each.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q92.** Count the days with fewer than 5 hours of sleep and print their share of all days as a percentage (rounded to 2 decimals).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q93.** Print the average steps on days with at least 8 hours of sleep, and on days with fewer than 5 hours of sleep. Round to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q94.** Create a new array `activity` that is `'Active'` where `steps > 4000`, else `'Lazy'`, using `np.where`. Print how many of each there are.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q95.** Print the number of days on which both `steps > 3000` and `mood == 300`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q96.** Print the total change in weight between the first and last day.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q97.** Create an array `cal_per_step = calories / steps` for the days with `steps > 0` and print its mean rounded to 4 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q98.** Standardise the steps: `(steps - mean) / std`. Print the first 5 values rounded to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q99.** Reshape the first 84 values of `steps` into 12 rows x 7 columns (12 weeks) and print the total steps of every week.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q100.** Using the weekly matrix from the previous question, print the index of the week with the highest total steps.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q101.** Using the weekly matrix, print the average steps for each weekday column (rounded to 2 decimals).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q102.** Stack `steps`, `calories` and `sleep` into one 3 x 96 array using `np.vstack` and print its shape and its second row's first 5 values.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q103.** Join `steps` and `calories` side by side as columns using `np.hstack` / `reshape`, and print the shape.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q104.** Use `np.concatenate` to join the first 3 and the last 3 values of `steps` into one array.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q105.** Print every 10th date from the dataset.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q106.** Print the steps of the days in reverse order for the last 5 days.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q107.** Print the number of days with 0 steps recorded as `np.any` result and count for `calories == 0`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q108.** Replace all `calories` values that are 0 by the mean of the non-zero calories (rounded to integer) in a COPY and print how many zeros are left in the copy and in the original.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q109.** Clip the steps: replace every value above 6000 by 6000 (in a copy). Print the new maximum.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q110.** Use `np.vectorize` (or a loop) to create a label array: `'High'` if calories > 150 else `'Low'`. Print the number of `'High'` days.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q111.** Create the 3 x 3 identity matrix and a matrix of the numbers 1..9. Multiply them with `np.matmul` and print the result.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q112.** Create an array of 5 equally spaced numbers between 10 and 50 using `np.linspace` and print it.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q113.** Create a 4 x 4 array filled with ones, set its diagonal to 5 using `np.diag` / slicing logic, and print it.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q114.** Create `np.arange(1, 13).reshape(3, 4)` and print its transpose and the transposed shape.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q115.** Split `np.arange(12)` into 3 equal parts using `np.split` and print the parts.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q116.** Use `np.tile` to repeat the array `[1, 2, 3]` four times and print the result.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q117.** Print the first 3 rows and the last 2 columns of `data` (the string array).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q118.** Compute the mean of every numeric column of `data` (columns 1 to 6) in one line using `astype` and `axis`. Round to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q119.** Using broadcasting, subtract the mean of every column (columns 1 to 6) from the numeric part of `data` and print the first row, rounded to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q120.** Show with `np.shares_memory` that a slice is a view and that `.copy()` is not.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q121.** Create a column vector with `np.newaxis` from `np.array([1, 2, 3])` and add it to `np.array([10, 20, 30])`. Print the result and its shape.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q122.** Find the days where steps were above the average AND calories burned were above the average. Print their count.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q123.** Print the date and steps of the day with the highest calories burned.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q124.** Sort the days by sleep hours (ascending) and print the first 5 sorted `sleep` values together with their dates.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q125.** Print the correlation of steps and calories using `np.corrcoef`, rounded to 3 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q126.** Print the 25th, 50th and 75th percentiles of `steps` using `np.percentile`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q127.** How many days fall in each step range: below 2000, 2000-4999, 5000 and above? Print the three counts.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q128.** Print the mean and the standard deviation of `calories`, rounded to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q129.** Print the dates on which the minimum number of sleep hours was recorded.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q130.** Create `a = np.array([[1, 2, 3], [4, 5, 6]])` and print `a.sum()`, `a.mean(axis=0)` and `a.max(axis=1)`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

