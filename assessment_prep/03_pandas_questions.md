# Section 3 - Pandas (McKinsey and IMDB data)

Run this set-up first (keep the data files in the same folder as your notebook):

```python
import pandas as pd
import numpy as np
df        = pd.read_csv('mckinsey.csv')     # country, year, population, continent, life_exp, gdp_cap
movies    = pd.read_csv('movies.csv')       # id, budget, popularity, revenue, title, vote_average, vote_count, director_id, year, month, day
directors = pd.read_csv('directors.csv')    # director_name, id, gender
```

## Part A - Multiple choice (62)

**Q131.** What is `df.shape`?

- **A)** `(1704, 5)`
- **B)** `(1703, 6)`
- **C)** `(1704, 6)`
- **D)** `(6, 1704)`

**Q132.** How many different continents are in the data (`df['continent'].nunique()`)?

- **A)** `142`
- **B)** `1704`
- **C)** `5`
- **D)** `12`

**Q133.** How many different countries are in the data?

- **A)** `142`
- **B)** `1704`
- **C)** `5`
- **D)** `12`

**Q134.** Which continent has the most rows? (`df['continent'].value_counts().index[0]`)

- **A)** `624`
- **B)** `'Africa'`
- **C)** `'Oceania'`
- **D)** `'Asia'`

**Q135.** How many rows belong to the continent `Oceania`?

- **A)** `1680`
- **B)** `624`
- **C)** `24`
- **D)** `5`

**Q136.** How many years are recorded for every country (`df['country'].value_counts().iloc[0]`)?

- **A)** `12`
- **B)** `55`
- **C)** `13`
- **D)** `1704`

**Q137.** What are the first and last years in the data?

- **A)** `[1952, 2002]`
- **B)** `[1957, 2007]`
- **C)** `[1952, 2007]`
- **D)** `[2007, 1952]`

**Q138.** What is the highest life expectancy in the data?

- **A)** `59.474439366197174`
- **B)** `82.603`
- **C)** `23.599`
- **D)** `60.7125`

**Q139.** What is the average life expectancy (rounded to 2 decimals)?

- **A)** `7215.33`
- **B)** `60.71`
- **C)** `12.92`
- **D)** `59.47`

**Q140.** Which country has the highest GDP per capita value? (`df.loc[df['gdp_cap'].idxmax(), 'country']`)

- **A)** `'China'`
- **B)** `'Japan'`
- **C)** `'Kuwait'`
- **D)** `'Congo, Dem. Rep.'`

**Q141.** Which country has the largest population in the data?

- **A)** `'Japan'`
- **B)** `'Sao Tome and Principe'`
- **C)** `'China'`
- **D)** `'Kuwait'`

**Q142.** How many rows are there for the year 2007?

- **A)** `142`
- **B)** `0`
- **C)** `12`
- **D)** `143`

**Q143.** What is the average life expectancy of the year 2007, rounded to 2 decimals?

- **A)** `67.01`
- **B)** `59.47`
- **C)** `71.94`
- **D)** `49.06`

**Q144.** In 2007, how many countries had a life expectancy above 75?

- **A)** `173`
- **B)** `271`
- **C)** `13`
- **D)** `44`

**Q145.** Which continent has the highest average life expectancy? (`groupby` + `mean`)

- **A)** `'Asia'`
- **B)** `'Europe'`
- **C)** `'Africa'`
- **D)** `'Oceania'`

**Q146.** Which continent has the lowest average life expectancy?

- **A)** `'Africa'`
- **B)** `'Asia'`
- **C)** `'Oceania'`
- **D)** `'Americas'`

**Q147.** What is the total population of `Asia` in 2007?

- **A)** `3811953827`
- **B)** `1395357351`
- **C)** `30507333901`
- **D)** `6251013179`

**Q148.** What does `df.iloc[0]['country']` return?

- **A)** `'Asia'`
- **B)** `'Albania'`
- **C)** `'Afghanistan'`
- **D)** `'Zimbabwe'`

**Q149.** What does `df.loc[1703, 'year']` return?

- **A)** `2002`
- **B)** `469.7092981`
- **C)** `2007`
- **D)** `1952`

**Q150.** After `df2 = df.rename({'country': 'Country'}, axis=1)`, what are the first two column names?

- **A)** `['year', 'population']`
- **B)** `['country', 'year']`
- **C)** `['Country', 'year']`
- **D)** `['country', 'Year']`

**Q151.** `df.drop('life_exp', axis=1)` (without `inplace`). How many columns does `df` have afterwards?

- **A)** `4`
- **B)** `1704`
- **C)** `5`
- **D)** `6`

**Q152.** How many duplicated rows are in `df`?

- **A)** `1562`
- **B)** `1`
- **C)** `0`
- **D)** `1692`

**Q153.** What is the type of `df['life_exp']`?

- **A)** `'Series'`
- **B)** `'ndarray'`
- **C)** `'tuple'`
- **D)** `'DataFrame'`

**Q154.** What is the median GDP per capita for the continent `Europe`, rounded to 2 decimals?

- **A)** `1192.14`
- **B)** `3531.85`
- **C)** `12081.75`
- **D)** `14469.48`

**Q155.** How many rows contain a country name that starts with `'Un'`?

- **A)** `24`
- **B)** `0`
- **C)** `48`
- **D)** `142`

**Q156.** Which year has the highest average life expectancy?

- **A)** `2002`
- **B)** `2007`
- **C)** `1952`
- **D)** `1957`

**Q157.** What is `movies.shape`?

- **A)** `(1465, 12)`
- **B)** `(1464, 12)`
- **C)** `(12, 1465)`
- **D)** `(1465, 11)`

**Q158.** What is `directors.shape`?

- **A)** `(2349, 4)`
- **B)** `(2349, 3)`
- **C)** `(2348, 4)`
- **D)** `(4, 2349)`

**Q159.** How many movies have been released in 2012?

- **A)** `49`
- **B)** `1239`
- **C)** `41`
- **D)** `177`

**Q160.** What is the highest revenue in the data?

- **A)** `143253923.0750853`
- **B)** `2787965087`
- **C)** `380000000`
- **D)** `0`

**Q161.** Which movie has the highest revenue?

- **A)** `'The Pink Panther'`
- **B)** `'Pirates of the Caribbean: On Stranger Tides'`
- **C)** `'Interstellar'`
- **D)** `'Avatar'`

**Q162.** What is the average `vote_average`, rounded to 2 decimals?

- **A)** `8.3`
- **B)** `6.4`
- **C)** `6.37`
- **D)** `1146.4`

**Q163.** How many movies have a `vote_average` of at least 8?

- **A)** `23`
- **B)** `13`
- **C)** `1459`
- **D)** `1452`

**Q164.** Which month has the most movie releases?

- **A)** `'Sep'`
- **B)** `'Friday'`
- **C)** `'Dec'`
- **D)** `'Jan'`

**Q165.** Which weekday has the most releases?

- **A)** `'Thursday'`
- **B)** `'Sunday'`
- **C)** `'Dec'`
- **D)** `'Friday'`

**Q166.** How many movies have a title containing the word `'Love'` (case-sensitive)?

- **A)** `15`
- **B)** `4`
- **C)** `1`
- **D)** `5`

**Q167.** How many unique director ids are used in `movies`?

- **A)** `2349`
- **B)** `199`
- **C)** `2348`
- **D)** `1465`

**Q168.** How many directors have a missing `gender`?

- **A)** `1724`
- **B)** `624`
- **C)** `2`
- **D)** `625`

**Q169.** Which gender value is most common among the directors?

- **A)** `2`
- **B)** `'Female'`
- **C)** `'Male'`
- **D)** `1574`

**Q170.** After `movies.merge(directors, left_on='director_id', right_on='id')` (inner join), how many rows are there?

- **A)** `2349`
- **B)** `1465`
- **C)** `3814`
- **D)** `1464`

**Q171.** How many columns does the merged frame of the previous question have? (Both tables have an `id` and an `Unnamed: 0` column, so pandas adds the suffixes `_x` and `_y`.)

- **A)** `4`
- **B)** `16`
- **C)** `15`
- **D)** `12`

**Q172.** What is the shape of `pd.concat([movies, movies])`?

- **A)** `(2930, 24)`
- **B)** `(1465, 12)`
- **C)** `(2930, 12)`
- **D)** `(1465, 24)`

**Q173.** What is the shape of `pd.concat([movies, movies], axis=1)`?

- **A)** `(1465, 12)`
- **B)** `(2930, 24)`
- **C)** `(2930, 12)`
- **D)** `(1465, 24)`

**Q174.** Which year has the highest average `vote_average`?

- **A)** `2009`
- **B)** `2016`
- **C)** `1976`
- **D)** `2004.0`

**Q175.** Which year has the highest total revenue?

- **A)** `1976`
- **B)** `2004.0`
- **C)** `2009`
- **D)** `2016`

**Q176.** What is the total budget of all movies released in 2010?

- **A)** `70353617179`
- **B)** `3767500000`
- **C)** `59801587.3015873`
- **D)** `10175829727`

**Q177.** How many movies made a profit (`revenue > budget`)?

- **A)** `1270`
- **B)** `1041`
- **C)** `1146`
- **D)** `319`

**Q178.** What are the titles of the top 3 movies by `popularity`?

- **A)** `['Avatar', "Pirates of the Caribbean: At World's End", 'Spectre']`
- **B)** `['Interstellar', 'Mad Max: Fury Road', 'Pirates of the Caribbean: The Curse of the Black Pearl']`
- **C)** `['Walking and Talking', 'An Everlasting Piece', 'The Magic Flute']`
- **D)** `['Avatar', 'Titanic', 'Furious 7']`

**Q179.** What does `movies.sort_values('budget', ascending=False).iloc[0]['title']` return?

- **A)** `"Pirates of the Caribbean: At World's End"`
- **B)** `'Pirates of the Caribbean: On Stranger Tides'`
- **C)** `'Slacker'`
- **D)** `'Avatar'`

**Q180.** How many movies were released on a `'Friday'`?

- **A)** `654`
- **B)** `46`
- **C)** `811`
- **D)** `7`

**Q181.** How many movies were released in `'Dec'` or `'Nov'` (use `isin`)?

- **A)** `310`
- **B)** `459`
- **C)** `193`
- **D)** `117`

**Q182.** Which director (name) directed the most movies in this data after merging? (`merge` + `value_counts`)

- **A)** `'Brian Herzlinger'`
- **B)** `'James Cameron'`
- **C)** `'Nicole Holofcener'`
- **D)** `'Steven Spielberg'`

**Q183.** How many `movies` rows have a director whose gender is `'Female'` after merging?

- **A)** `1309`
- **B)** `32`
- **C)** `150`
- **D)** `124`

**Q184.** Which of the following gives the number of movies per year, sorted by year? (choose the first 3 values)

- **A)** `[73, 71, 69]`
- **B)** `[53, 41, 26]`
- **C)** `[3, 6, 5]`
- **D)** `[112875431, 349040060, 532589023]`

**Q185.** `s = pd.Series([10, 20, 30])`. What is `s[1]`?

- **A)** `10`
- **B)** `60`
- **C)** `30`
- **D)** `20`

**Q186.** `s = pd.Series([4, 8, 6])`. What is `s.sort_values().index.tolist()`?

- **A)** `[1, 2, 0]`
- **B)** `[4, 6, 8]`
- **C)** `[0, 2, 1]`
- **D)** `[0, 1, 2]`

**Q187.** For `d = pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6]})`, what is `d.sum(axis=1).tolist()`?

- **A)** `[5, 7, 9]`
- **B)** `[6, 15]`
- **C)** `21`
- **D)** `[4, 5, 6]`

**Q188.** `d = pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]})`. What is `d.groupby('g')['v'].sum().to_dict()`?

- **A)** `{'x': 3, 'y': 4}`
- **B)** `{'x': 2, 'y': 2}`
- **C)** `{'x': 2.0, 'y': 3.0}`
- **D)** `{'x': 4, 'y': 6}`

**Q189.** `d = pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]})`. What does `d.groupby('g')['v'].transform('sum').tolist()` return?

- **A)** `[4, 6]`
- **B)** `[1, 2, 3, 4]`
- **C)** `[3, 4, 3, 4]`
- **D)** `[4, 6, 4, 6]`

**Q190.** `s = pd.Series([1, 2, 3, 4])`. What is `s.apply(lambda x: x ** 2).tolist()`?

- **A)** `[2, 4, 6, 8]`
- **B)** `[1, 2, 3, 4]`
- **C)** `[3, 4, 5, 6]`
- **D)** `[1, 4, 9, 16]`

**Q191.** `d = pd.DataFrame({'a': [3, 1, 2]})`. What is `d.sort_values('a').reset_index(drop=True)['a'].index.tolist()`?

- **A)** `[2, 1, 0]`
- **B)** `[0, 1, 2]`
- **C)** `[1, 2, 3]`
- **D)** `[1, 2, 0]`

**Q192.** `d = pd.DataFrame({'a': [1, 1, 2, 3, 3]})`. How many rows remain after `d.drop_duplicates()`?

- **A)** `2`
- **B)** `4`
- **C)** `3`
- **D)** `5`

---

## Part B - Coding (58)

**Q193.** Read `mckinsey.csv` into `df` and print the first 5 rows and the shape.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q194.** Use `df.info()` to see the data types and check if there are any null values.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q195.** Print the descriptive statistics of all numeric columns (`describe`).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q196.** Print the number of rows for every continent.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q197.** Create a copy of `df` called `df1`. Rename `country` to `New_Country` in `df1` and drop the `life_exp` column (use `inplace=True`). Print the column names of `df1` and of `df`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q198.** Select only the rows for the year 2007 and print how many rows there are and the first 3 rows.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q199.** Print all the rows for `India`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q200.** Print the country, year and life expectancy for `Japan` using `loc` with a condition.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q201.** Print the average life expectancy for every continent, rounded to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q202.** Print the total population of every continent in the year 2007.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q203.** Print the 5 countries with the highest GDP per capita in 2007 (country and gdp_cap).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q204.** Print the 5 countries with the lowest life expectancy in 2007.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q205.** Create a new column `gdp_total = gdp_cap * population` in a copy of `df` and print the top 3 rows of 2007 by this column (country, gdp_total).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q206.** Create a column `rich` in a copy of `df` that is `'Yes'` if `gdp_cap > 10000` else `'No'` (use `apply` or `np.where`). Print the counts.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q207.** Print the number of countries per continent (hint: unique countries, `groupby` + `nunique`).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q208.** Find the average life expectancy per year and print the values for the first 3 years.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q209.** For every continent print the minimum, mean and maximum life expectancy using `agg`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q210.** Print how many countries had a life expectancy above 80 in 2007 and name them.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q211.** Print the row at position 100 using `iloc` and the row with label 100 using `loc`. Are they the same?

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q212.** Print the countries whose names start with `'New'`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q213.** Print the countries whose name contains `'Republic'`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q214.** Print the rows for the countries `India`, `China` and `Japan` in 2007 using `isin`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q215.** How much did the life expectancy of `India` change between 1952 and 2007?

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q216.** Print the median GDP per capita of every continent in 2007, sorted from highest to lowest.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q217.** Add a column `pop_share` to a copy of the 2007 data that shows each country's share of the total 2007 population in percent (rounded to 2 decimals). Print the top 3 countries by share.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q218.** For every country compute the life expectancy compared to the continent average of the same year using `groupby` + `transform` and print the first 3 values of a new column `diff` (rounded to 2).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q219.** Print the correlation between `gdp_cap` and `life_exp`, rounded to 3 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q220.** Drop the columns `Unnamed: 0` from both data frames (without changing the originals) and print the new shapes.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q221.** Merge `movies` and `directors` on the director id into a new frame `data`, keeping only the matching rows, and print its shape.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q222.** After the merge, drop the redundant columns (`Unnamed: 0_x`, `Unnamed: 0_y`, `id_y`) and rename `id_x` to `movie_id`. Print the column names.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q223.** Print the 5 movies with the highest revenue (title and revenue).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q224.** Print the 5 most expensive movies (title and budget).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q225.** Create a column `profit = revenue - budget` in a copy of `movies` and print the 5 most profitable movies (title, profit).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q226.** Print how many movies were released in every year from 2010 to 2015 (sorted by year).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q227.** Print the number of movies released in each month, sorted from most to least.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q228.** Print the movies released in 2015 with a `vote_average` above 7.5 (title, vote_average).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q229.** Print the titles that contain the word `'War'` and the number of them.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q230.** Print the total revenue for every year and show the top 5 years.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q231.** Print the average budget for every year, rounded to 0 decimals, for the last 5 years in the data.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q232.** After merging with `directors`, print the 5 directors with the most movies and the number of movies.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q233.** After merging, print the average `vote_average` of the movies of the director `Christopher Nolan`, rounded to 2 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q234.** After merging, print the total revenue per director for the top 5 directors.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q235.** After merging, print the number of movies directed by Male, Female and unknown (missing) gender directors.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q236.** After merging, print the average revenue by gender (rounded to 0 decimals).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q237.** Print how many directors in the `directors` table never directed a movie of the `movies` table (hint: `isin`).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q238.** Use a LEFT join of `directors` on `movies` (`how='left'`) and print the shape. Why is it bigger than the inner join?

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q239.** Group `movies` by `year` and `month` and print the number of movies for the 5 busiest year-month combinations.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q240.** Find the movie with the highest `vote_average` among the movies with at least 5000 votes.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q241.** Add a column `decade` (e.g. 2010 for 2012) to a copy of `movies` and print the number of movies per decade.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q242.** Using `transform`, add a column `rev_vs_year_avg` = revenue minus the average revenue of that year to a copy of `movies`. Print the first 3 values (rounded to 0 decimals).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q243.** Use `pd.concat` to stack the first 3 and last 3 rows of `movies` into one DataFrame and print the titles.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q244.** Set `title` as the index of `movies` (in a copy) and print the `revenue` of `'Avatar'` using `loc`.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q245.** Create a DataFrame from the dictionary `{'name': ['A', 'B', 'C'], 'marks': [80, 65, 90]}` and print the name of the student with the highest marks.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q246.** For the DataFrame `{'dept': ['HR', 'IT', 'HR', 'IT', 'IT'], 'salary': [40, 60, 50, 80, 70]}` print the average salary per department.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q247.** Using `apply` with a lambda, create a column `short_title` in a copy of `movies` with the first 10 characters of every title. Print the first 3.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q248.** Print how many movies have `budget == 0` and what share of all movies this is (in percent, 2 decimals).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q249.** Print the average revenue of movies released on weekends (`'Saturday'`, `'Sunday'`) vs the other days. Round to 0 decimals.

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

**Q250.** Print the movies from 2009 that earned more than 500 million, sorted by revenue (title, revenue).

*Type:* coding - write the code and compare your output with the expected output in the solutions file.

