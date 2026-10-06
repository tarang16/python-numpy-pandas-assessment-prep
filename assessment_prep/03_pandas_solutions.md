# Section 3 - Pandas (McKinsey and IMDB data) - Solutions

## Part A - Multiple choice

**Q131. Answer: C**

- A) `(1704, 5)` -> `(1704, 5)`
- B) `(1703, 6)` -> `(1703, 6)`
- C) `df.shape` -> `(1704, 6)`
- D) `(6, 1704)` -> `(6, 1704)`

**Q132. Answer: C**

- A) `df['country'].nunique()` -> `142`
- B) `len(df)` -> `1704`
- C) `df['continent'].nunique()` -> `5`
- D) `df['year'].nunique()` -> `12`

**Q133. Answer: A**

- A) `df['country'].nunique()` -> `142`
- B) `len(df)` -> `1704`
- C) `df['continent'].nunique()` -> `5`
- D) `df['year'].nunique()` -> `12`

**Q134. Answer: B**

- A) `df['continent'].value_counts().iloc[0]` -> `624`
- B) `df['continent'].value_counts().index[0]` -> `'Africa'`
- C) `df['continent'].value_counts().index[-1]` -> `'Oceania'`
- D) `df['continent'].unique()[0]` -> `'Asia'`

**Q135. Answer: C**

- A) `(df['continent'] != 'Oceania').sum()` -> `1680`
- B) `df['continent'].value_counts().iloc[0]` -> `624`
- C) `(df['continent'] == 'Oceania').sum()` -> `24`
- D) `df['continent'].nunique()` -> `5`

**Q136. Answer: A**

- A) `df['country'].value_counts().iloc[0]` -> `12`
- B) `df['year'].max() - df['year'].min()` -> `55`
- C) `df['year'].nunique() + 1` -> `13`
- D) `len(df)` -> `1704`

**Q137. Answer: C**

- A) `[df['year'].min(), df['year'].max() - 5]` -> `[1952, 2002]`
- B) `[df['year'].min() + 5, df['year'].max()]` -> `[1957, 2007]`
- C) `[df['year'].min(), df['year'].max()]` -> `[1952, 2007]`
- D) `[df['year'].max(), df['year'].min()]` -> `[2007, 1952]`

**Q138. Answer: B**

- A) `df['life_exp'].mean()` -> `59.474439366197174`
- B) `df['life_exp'].max()` -> `82.603`
- C) `df['life_exp'].min()` -> `23.599`
- D) `df['life_exp'].median()` -> `60.7125`

**Q139. Answer: D**

- A) `round(df['gdp_cap'].mean(), 2)` -> `7215.33`
- B) `round(df['life_exp'].median(), 2)` -> `60.71`
- C) `round(df['life_exp'].std(), 2)` -> `12.92`
- D) `round(df['life_exp'].mean(), 2)` -> `59.47`

**Q140. Answer: C**

- A) `df.loc[df['population'].idxmax(), 'country']` -> `'China'`
- B) `df.loc[df['life_exp'].idxmax(), 'country']` -> `'Japan'`
- C) `df.loc[df['gdp_cap'].idxmax(), 'country']` -> `'Kuwait'`
- D) `df.loc[df['gdp_cap'].idxmin(), 'country']` -> `'Congo, Dem. Rep.'`

*Explanation:* `idxmax` gives the row label of the maximum; `loc` then reads the country from that row.

**Q141. Answer: C**

- A) `df.loc[df['life_exp'].idxmax(), 'country']` -> `'Japan'`
- B) `df.loc[df['population'].idxmin(), 'country']` -> `'Sao Tome and Principe'`
- C) `df.loc[df['population'].idxmax(), 'country']` -> `'China'`
- D) `df.loc[df['gdp_cap'].idxmax(), 'country']` -> `'Kuwait'`

**Q142. Answer: A**

- A) `(df['year'] == 2007).sum()` -> `142`
- B) `(df['year'] > 2007).sum()` -> `0`
- C) `df['year'].nunique()` -> `12`
- D) `(df['year'] == 1952).sum() + 1` -> `143`

**Q143. Answer: A**

- A) `round(df[df['year'] == 2007]['life_exp'].mean(), 2)` -> `67.01`
- B) `round(df['life_exp'].mean(), 2)` -> `59.47`
- C) `round(df[df['year'] == 2007]['life_exp'].median(), 2)` -> `71.94`
- D) `round(df[df['year'] == 1952]['life_exp'].mean(), 2)` -> `49.06`

**Q144. Answer: D**

- A) `len(df[df['life_exp'] > 75])` -> `173`
- B) `len(df[(df['year'] == 2007) | (df['life_exp'] > 75)])` -> `271`
- C) `len(df[(df['year'] == 2007) & (df['life_exp'] > 80)])` -> `13`
- D) `len(df[(df['year'] == 2007) & (df['life_exp'] > 75)])` -> `44`

*Explanation:* Combine conditions with `&` and put each condition in parentheses.

**Q145. Answer: D**

- A) `df.groupby('continent')['population'].sum().idxmax()` -> `'Asia'`
- B) `'Europe'` -> `'Europe'`
- C) `df.groupby('continent')['life_exp'].mean().idxmin()` -> `'Africa'`
- D) `df.groupby('continent')['life_exp'].mean().idxmax()` -> `'Oceania'`

**Q146. Answer: A**

- A) `df.groupby('continent')['life_exp'].mean().idxmin()` -> `'Africa'`
- B) `'Asia'` -> `'Asia'`
- C) `df.groupby('continent')['life_exp'].mean().idxmax()` -> `'Oceania'`
- D) `'Americas'` -> `'Americas'`

**Q147. Answer: A**

- A) `df[(df['continent'] == 'Asia') & (df['year'] == 2007)]['population'].sum()` -> `3811953827`
- B) `df[(df['continent'] == 'Asia') & (df['year'] == 1952)]['population'].sum()` -> `1395357351`
- C) `df[df['continent'] == 'Asia']['population'].sum()` -> `30507333901`
- D) `df[df['year'] == 2007]['population'].sum()` -> `6251013179`

**Q148. Answer: C**

- A) `df['continent'].iloc[0]` -> `'Asia'`
- B) `df.iloc[12]['country']` -> `'Albania'`
- C) `df.iloc[0]['country']` -> `'Afghanistan'`
- D) `df.iloc[-1]['country']` -> `'Zimbabwe'`

*Explanation:* `iloc` is purely position-based: position 0 is the first row.

**Q149. Answer: C**

- A) `df.loc[1702, 'year']` -> `2002`
- B) `df.loc[1703, 'gdp_cap']` -> `469.7092981`
- C) `df.loc[1703, 'year']` -> `2007`
- D) `df.loc[0, 'year']` -> `1952`

*Explanation:* `loc` is label-based: label 1703 is the last row.

**Q150. Answer: C**

- A) `df.rename({'country': 'Country'}, axis=1).columns.tolist()[1:3]` -> `['year', 'population']`
- B) `df.columns.tolist()[:2]` -> `['country', 'year']`
- C) `df.rename({'country': 'Country'}, axis=1).columns.tolist()[:2]` -> `['Country', 'year']`
- D) `df.rename({'year': 'Year'}, axis=1).columns.tolist()[:2]` -> `['country', 'Year']`

*Explanation:* `rename` needs `axis=1` (or `columns=`) to rename columns. With `axis=0` it renames index labels and leaves column names unchanged.

**Q151. Answer: D**

- A) `df.shape[1] - 2` -> `4`
- B) `df.drop('life_exp', axis=1).shape[0]` -> `1704`
- C) `df.drop('life_exp', axis=1).shape[1]` -> `5`
- D) `df.drop('life_exp', axis=1).shape[1] + 1` -> `6`

*Explanation:* Without `inplace=True` the result is a NEW DataFrame; the original `df` still has 6 columns.

**Q152. Answer: C**

- A) `df['country'].duplicated().sum()` -> `1562`
- B) `df.duplicated().sum() + 1` -> `1`
- C) `df.duplicated().sum()` -> `0`
- D) `df['year'].duplicated().sum()` -> `1692`

**Q153. Answer: A**

- A) `type(df['life_exp']).__name__` -> `'Series'`
- B) `type(df['life_exp'].values).__name__` -> `'ndarray'`
- C) `type(df.shape).__name__` -> `'tuple'`
- D) `type(df[['life_exp']]).__name__` -> `'DataFrame'`

*Explanation:* Single brackets return a Series; double brackets return a DataFrame.

**Q154. Answer: C**

- A) `round(df[df['continent'] == 'Africa']['gdp_cap'].median(), 2)` -> `1192.14`
- B) `round(df['gdp_cap'].median(), 2)` -> `3531.85`
- C) `round(df[df['continent'] == 'Europe']['gdp_cap'].median(), 2)` -> `12081.75`
- D) `round(df[df['continent'] == 'Europe']['gdp_cap'].mean(), 2)` -> `14469.48`

**Q155. Answer: A**

- A) `df['country'].str.startswith('Un').sum()` -> `24`
- B) `df['country'].str.endswith('Un').sum()` -> `0`
- C) `df['country'].str.contains('un').sum()` -> `48`
- D) `df['country'].nunique()` -> `142`

*Explanation:* `str.contains` is case-sensitive by default, so `'un'` and `'Un'` give different results.

**Q156. Answer: B**

- A) `df['year'].max() - 5` -> `2002`
- B) `df.groupby('year')['life_exp'].mean().idxmax()` -> `2007`
- C) `df.groupby('year')['life_exp'].mean().idxmin()` -> `1952`
- D) `df['year'].min() + 5` -> `1957`

**Q157. Answer: A**

- A) `movies.shape` -> `(1465, 12)`
- B) `(1464, 12)` -> `(1464, 12)`
- C) `(12, 1465)` -> `(12, 1465)`
- D) `(1465, 11)` -> `(1465, 11)`

**Q158. Answer: A**

- A) `directors.shape` -> `(2349, 4)`
- B) `(2349, 3)` -> `(2349, 3)`
- C) `(2348, 4)` -> `(2348, 4)`
- D) `(4, 2349)` -> `(4, 2349)`

**Q159. Answer: A**

- A) `(movies['year'] == 2012).sum()` -> `49`
- B) `(movies['year'] < 2012).sum()` -> `1239`
- C) `movies['year'].nunique()` -> `41`
- D) `(movies['year'] > 2012).sum()` -> `177`

**Q160. Answer: B**

- A) `movies['revenue'].mean()` -> `143253923.0750853`
- B) `movies['revenue'].max()` -> `2787965087`
- C) `movies['budget'].max()` -> `380000000`
- D) `movies['revenue'].min()` -> `0`

**Q161. Answer: D**

- A) `movies.loc[movies['revenue'].idxmin(), 'title']` -> `'The Pink Panther'`
- B) `movies.loc[movies['budget'].idxmax(), 'title']` -> `'Pirates of the Caribbean: On Stranger Tides'`
- C) `movies.loc[movies['popularity'].idxmax(), 'title']` -> `'Interstellar'`
- D) `movies.loc[movies['revenue'].idxmax(), 'title']` -> `'Avatar'`

**Q162. Answer: C**

- A) `round(movies['vote_average'].max(), 2)` -> `8.3`
- B) `round(movies['vote_average'].median(), 2)` -> `6.4`
- C) `round(movies['vote_average'].mean(), 2)` -> `6.37`
- D) `round(movies['vote_count'].mean(), 2)` -> `1146.4`

**Q163. Answer: A**

- A) `(movies['vote_average'] >= 8).sum()` -> `23`
- B) `(movies['vote_average'] > 8).sum()` -> `13`
- C) `(movies['vote_count'] >= 8).sum()` -> `1459`
- D) `(movies['vote_average'] <= 8).sum()` -> `1452`

**Q164. Answer: C**

- A) `movies['month'].value_counts().index[1]` -> `'Sep'`
- B) `movies['day'].value_counts().index[0]` -> `'Friday'`
- C) `movies['month'].value_counts().index[0]` -> `'Dec'`
- D) `movies['month'].value_counts().index[-1]` -> `'Jan'`

**Q165. Answer: D**

- A) `movies['day'].unique()[0]` -> `'Thursday'`
- B) `movies['day'].value_counts().index[-1]` -> `'Sunday'`
- C) `movies['month'].value_counts().index[0]` -> `'Dec'`
- D) `movies['day'].value_counts().index[0]` -> `'Friday'`

**Q166. Answer: A**

- A) `movies['title'].str.contains('Love').sum()` -> `15`
- B) `movies['title'].str.startswith('Love').sum()` -> `4`
- C) `movies['title'].str.contains('love').sum()` -> `1`
- D) `movies['title'].str.endswith('Love').sum()` -> `5`

**Q167. Answer: B**

- A) `len(directors)` -> `2349`
- B) `movies['director_id'].nunique()` -> `199`
- C) `directors['id'].nunique() - 1` -> `2348`
- D) `len(movies)` -> `1465`

**Q168. Answer: D**

- A) `directors['gender'].notnull().sum()` -> `1724`
- B) `directors.isnull().sum().sum() - 1` -> `624`
- C) `directors['gender'].nunique()` -> `2`
- D) `directors['gender'].isnull().sum()` -> `625`

**Q169. Answer: C**

- A) `directors['gender'].nunique()` -> `2`
- B) `directors['gender'].value_counts().index[-1]` -> `'Female'`
- C) `directors['gender'].value_counts().index[0]` -> `'Male'`
- D) `directors['gender'].value_counts().iloc[0]` -> `1574`

**Q170. Answer: B**

- A) `len(directors)` -> `2349`
- B) `len(movies.merge(directors, left_on='director_id', right_on='id'))` -> `1465`
- C) `len(movies) + len(directors)` -> `3814`
- D) `len(movies) - 1` -> `1464`

*Explanation:* Each movie matches exactly one director id, so no rows are lost or duplicated.

**Q171. Answer: B**

- A) `directors.shape[1]` -> `4`
- B) `movies.merge(directors, left_on='director_id', right_on='id').shape[1]` -> `16`
- C) `movies.shape[1] + directors.shape[1] - 1` -> `15`
- D) `movies.shape[1]` -> `12`

*Explanation:* Both frames have `id` and `Unnamed: 0` columns, so all 12 + 4 = 16 columns are kept and the duplicates get `_x` / `_y` suffixes.

**Q172. Answer: C**

- A) `(2930, 24)` -> `(2930, 24)`
- B) `movies.shape` -> `(1465, 12)`
- C) `pd.concat([movies, movies]).shape` -> `(2930, 12)`
- D) `pd.concat([movies, movies], axis=1).shape` -> `(1465, 24)`

*Explanation:* `concat` stacks vertically by default (axis=0); `axis=1` would place them side by side.

**Q173. Answer: D**

- A) `movies.shape` -> `(1465, 12)`
- B) `(2930, 24)` -> `(2930, 24)`
- C) `pd.concat([movies, movies]).shape` -> `(2930, 12)`
- D) `pd.concat([movies, movies], axis=1).shape` -> `(1465, 24)`

**Q174. Answer: C**

- A) `movies.groupby('year')['revenue'].sum().idxmax()` -> `2009`
- B) `movies.groupby('year')['vote_average'].mean().idxmin()` -> `2016`
- C) `movies.groupby('year')['vote_average'].mean().idxmax()` -> `1976`
- D) `movies['year'].median()` -> `2004.0`

**Q175. Answer: C**

- A) `movies.groupby('year')['revenue'].sum().idxmin()` -> `1976`
- B) `movies['year'].median()` -> `2004.0`
- C) `movies.groupby('year')['revenue'].sum().idxmax()` -> `2009`
- D) `movies.groupby('year')['budget'].mean().idxmax()` -> `2016`

**Q176. Answer: B**

- A) `movies['budget'].sum()` -> `70353617179`
- B) `movies[movies['year'] == 2010]['budget'].sum()` -> `3767500000`
- C) `movies[movies['year'] == 2010]['budget'].mean()` -> `59801587.3015873`
- D) `movies[movies['year'] == 2010]['revenue'].sum()` -> `10175829727`

**Q177. Answer: B**

- A) `(movies['revenue'] > 0).sum()` -> `1270`
- B) `(movies['revenue'] > movies['budget']).sum()` -> `1041`
- C) `(movies['revenue'] >= movies['budget']).sum()` -> `1146`
- D) `(movies['revenue'] < movies['budget']).sum()` -> `319`

**Q178. Answer: B**

- A) `movies['title'].head(3).tolist()` -> `['Avatar', "Pirates of the Caribbean: At World's End", 'Spectre']`
- B) `movies.sort_values('popularity', ascending=False)['title'].head(3).tolist()` -> `['Interstellar', 'Mad Max: Fury Road', 'Pirates of the Caribbean: The Curse of the Black Pearl']`
- C) `movies.sort_values('popularity')['title'].head(3).tolist()` -> `['Walking and Talking', 'An Everlasting Piece', 'The Magic Flute']`
- D) `movies.sort_values('revenue', ascending=False)['title'].head(3).tolist()` -> `['Avatar', 'Titanic', 'Furious 7']`

*Explanation:* `sort_values` sorts ascending by default; use `ascending=False` for the top values.

**Q179. Answer: B**

- A) `movies.iloc[1]['title']` -> `"Pirates of the Caribbean: At World's End"`
- B) `movies.sort_values('budget', ascending=False).iloc[0]['title']` -> `'Pirates of the Caribbean: On Stranger Tides'`
- C) `movies.sort_values('budget').iloc[0]['title']` -> `'Slacker'`
- D) `movies.sort_values('revenue', ascending=False).iloc[0]['title']` -> `'Avatar'`

**Q180. Answer: A**

- A) `(movies['day'] == 'Friday').sum()` -> `654`
- B) `(movies['day'] == 'Sunday').sum()` -> `46`
- C) `(movies['day'] != 'Friday').sum()` -> `811`
- D) `movies['day'].nunique()` -> `7`

**Q181. Answer: A**

- A) `movies['month'].isin(['Dec', 'Nov']).sum()` -> `310`
- B) `movies['month'].isin(['Dec', 'Nov', 'Oct']).sum()` -> `459`
- C) `(movies['month'] == 'Dec').sum()` -> `193`
- D) `(movies['month'] == 'Nov').sum()` -> `117`

**Q182. Answer: D**

- A) `directors['director_name'].iloc[-1]` -> `'Brian Herzlinger'`
- B) `directors['director_name'].value_counts().index[0]` -> `'James Cameron'`
- C) `movies.merge(directors, left_on='director_id', right_on='id')['director_name'].value_counts().index[-1]` -> `'Nicole Holofcener'`
- D) `movies.merge(directors, left_on='director_id', right_on='id')['director_name'].value_counts().index[0]` -> `'Steven Spielberg'`

**Q183. Answer: B**

- A) `(movies.merge(directors, left_on='director_id', right_on='id')['gender'] == 'Male').sum()` -> `1309`
- B) `(movies.merge(directors, left_on='director_id', right_on='id')['gender'] == 'Female').sum()` -> `32`
- C) `(directors['gender'] == 'Female').sum()` -> `150`
- D) `movies.merge(directors, left_on='director_id', right_on='id')['gender'].isnull().sum()` -> `124`

**Q184. Answer: C**

- A) `movies['year'].value_counts().head(3).tolist()` -> `[73, 71, 69]`
- B) `movies['year'].value_counts().sort_index().tail(3).tolist()` -> `[53, 41, 26]`
- C) `movies['year'].value_counts().sort_index().head(3).tolist()` -> `[3, 6, 5]`
- D) `movies.groupby('year')['revenue'].sum().head(3).tolist()` -> `[112875431, 349040060, 532589023]`

**Q185. Answer: D**

- A) `pd.Series([10, 20, 30])[0]` -> `10`
- B) `pd.Series([10, 20, 30]).sum()` -> `60`
- C) `pd.Series([10, 20, 30])[2]` -> `30`
- D) `pd.Series([10, 20, 30])[1]` -> `20`

**Q186. Answer: C**

- A) `pd.Series([4, 8, 6]).sort_values(ascending=False).index.tolist()` -> `[1, 2, 0]`
- B) `pd.Series([4, 8, 6]).sort_values().tolist()` -> `[4, 6, 8]`
- C) `pd.Series([4, 8, 6]).sort_values().index.tolist()` -> `[0, 2, 1]`
- D) `pd.Series([4, 8, 6]).index.tolist()` -> `[0, 1, 2]`

*Explanation:* Sorting keeps the original index labels, so they get reordered along with the values.

**Q187. Answer: A**

- A) `pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6]}).sum(axis=1).tolist()` -> `[5, 7, 9]`
- B) `pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6]}).sum(axis=0).tolist()` -> `[6, 15]`
- C) `pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6]}).sum().sum()` -> `21`
- D) `pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6]}).max(axis=1).tolist()` -> `[4, 5, 6]`

*Explanation:* `axis=1` sums across the columns of every row; `axis=0` sums down each column.

**Q188. Answer: D**

- A) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]}).groupby('g')['v'].max().to_dict()` -> `{'x': 3, 'y': 4}`
- B) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]}).groupby('g')['v'].count().to_dict()` -> `{'x': 2, 'y': 2}`
- C) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]}).groupby('g')['v'].mean().to_dict()` -> `{'x': 2.0, 'y': 3.0}`
- D) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]}).groupby('g')['v'].sum().to_dict()` -> `{'x': 4, 'y': 6}`

**Q189. Answer: D**

- A) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]}).groupby('g')['v'].sum().tolist()` -> `[4, 6]`
- B) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]})['v'].tolist()` -> `[1, 2, 3, 4]`
- C) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]}).groupby('g')['v'].transform('max').tolist()` -> `[3, 4, 3, 4]`
- D) `pd.DataFrame({'g': ['x', 'y', 'x', 'y'], 'v': [1, 2, 3, 4]}).groupby('g')['v'].transform('sum').tolist()` -> `[4, 6, 4, 6]`

*Explanation:* `transform` returns a result with the SAME length as the original (one value per row); `sum()` returns one value per group.

**Q190. Answer: D**

- A) `pd.Series([1, 2, 3, 4]).apply(lambda x: x * 2).tolist()` -> `[2, 4, 6, 8]`
- B) `[1, 2, 3, 4]` -> `[1, 2, 3, 4]`
- C) `pd.Series([1, 2, 3, 4]).apply(lambda x: x + 2).tolist()` -> `[3, 4, 5, 6]`
- D) `pd.Series([1, 2, 3, 4]).apply(lambda x: x ** 2).tolist()` -> `[1, 4, 9, 16]`

**Q191. Answer: B**

- A) `pd.DataFrame({'a': [3, 1, 2]}).index.tolist()[::-1]` -> `[2, 1, 0]`
- B) `pd.DataFrame({'a': [3, 1, 2]}).sort_values('a').reset_index(drop=True).index.tolist()` -> `[0, 1, 2]`
- C) `pd.DataFrame({'a': [3, 1, 2]}).sort_values('a')['a'].tolist()` -> `[1, 2, 3]`
- D) `pd.DataFrame({'a': [3, 1, 2]}).sort_values('a').index.tolist()` -> `[1, 2, 0]`

*Explanation:* `reset_index(drop=True)` renumbers the rows 0, 1, 2 ... and throws the old index away.

**Q192. Answer: C**

- A) `pd.DataFrame({'a': [1, 1, 2, 3, 3]}).duplicated().sum()` -> `2`
- B) `len(pd.DataFrame({'a': [1, 1, 2, 3, 3]}).drop_duplicates()) + 1` -> `4`
- C) `len(pd.DataFrame({'a': [1, 1, 2, 3, 3]}).drop_duplicates())` -> `3`
- D) `len(pd.DataFrame({'a': [1, 1, 2, 3, 3]}))` -> `5`

---

## Part B - Coding

**Q193.**

```python
print(df.head())
print(df.shape)
```

Output:

```text
       country  year  population continent  life_exp     gdp_cap
0  Afghanistan  1952     8425333      Asia    28.801  779.445314
1  Afghanistan  1957     9240934      Asia    30.332  820.853030
2  Afghanistan  1962    10267083      Asia    31.997  853.100710
3  Afghanistan  1967    11537966      Asia    34.020  836.197138
4  Afghanistan  1972    13079460      Asia    36.088  739.981106
(1704, 6)
```

**Q194.**

```python
df.info()
```

Output:

```text
<class 'pandas.DataFrame'>
RangeIndex: 1704 entries, 0 to 1703
Data columns (total 6 columns):
 #   Column      Non-Null Count  Dtype  
---  ------      --------------  -----  
 0   country     1704 non-null   str    
 1   year        1704 non-null   int64  
 2   population  1704 non-null   int64  
 3   continent   1704 non-null   str    
 4   life_exp    1704 non-null   float64
 5   gdp_cap     1704 non-null   float64
dtypes: float64(2), int64(2), str(2)
memory usage: 103.7 KB
```

**Q195.**

```python
print(df.describe())
```

Output:

```text
             year    population     life_exp        gdp_cap
count  1704.00000  1.704000e+03  1704.000000    1704.000000
mean   1979.50000  2.960121e+07    59.474439    7215.327081
std      17.26533  1.061579e+08    12.917107    9857.454543
min    1952.00000  6.001100e+04    23.599000     241.165876
25%    1965.75000  2.793664e+06    48.198000    1202.060309
50%    1979.50000  7.023596e+06    60.712500    3531.846988
75%    1993.25000  1.958522e+07    70.845500    9325.462346
max    2007.00000  1.318683e+09    82.603000  113523.132900
```

**Q196.**

```python
print(df['continent'].value_counts())
```

Output:

```text
continent
Africa      624
Asia        396
Europe      360
Americas    300
Oceania      24
Name: count, dtype: int64
```

**Q197.**

```python
df1 = df.copy()
df1.rename({'country': 'New_Country'}, axis=1, inplace=True)
df1.drop('life_exp', axis=1, inplace=True)
print(df1.columns.tolist())
print(df.columns.tolist())
```

Output:

```text
['New_Country', 'year', 'population', 'continent', 'gdp_cap']
['country', 'year', 'population', 'continent', 'life_exp', 'gdp_cap']
```

**Q198.**

```python
d07 = df[df['year'] == 2007]
print(len(d07))
print(d07.head(3))
```

Output:

```text
142
        country  year  population continent  life_exp      gdp_cap
11  Afghanistan  2007    31889923      Asia    43.828   974.580338
23      Albania  2007     3600523    Europe    76.423  5937.029526
35      Algeria  2007    33333216    Africa    72.301  6223.367465
```

**Q199.**

```python
print(df[df['country'] == 'India'])
```

Output:

```text
    country  year  population continent  life_exp      gdp_cap
696   India  1952   372000000      Asia    37.373   546.565749
697   India  1957   409000000      Asia    40.249   590.061996
698   India  1962   454000000      Asia    43.605   658.347151
699   India  1967   506000000      Asia    47.193   700.770611
700   India  1972   567000000      Asia    50.651   724.032527
701   India  1977   634000000      Asia    54.208   813.337323
702   India  1982   708000000      Asia    56.596   855.723538
703   India  1987   788000000      Asia    58.553   976.512676
704   India  1992   872000000      Asia    60.223  1164.406809
705   India  1997   959000000      Asia    61.765  1458.817442
706   India  2002  1034172547      Asia    62.879  1746.769454
707   India  2007  1110396331      Asia    64.698  2452.210407
```

**Q200.**

```python
print(df.loc[df['country'] == 'Japan', ['country', 'year', 'life_exp']])
```

Output:

```text
    country  year  life_exp
792   Japan  1952    63.030
793   Japan  1957    65.500
794   Japan  1962    68.730
795   Japan  1967    71.430
796   Japan  1972    73.420
797   Japan  1977    75.380
798   Japan  1982    77.110
799   Japan  1987    78.670
800   Japan  1992    79.360
801   Japan  1997    80.690
802   Japan  2002    82.000
803   Japan  2007    82.603
```

**Q201.**

```python
print(df.groupby('continent')['life_exp'].mean().round(2))
```

Output:

```text
continent
Africa      48.87
Americas    64.66
Asia        60.06
Europe      71.90
Oceania     74.33
Name: life_exp, dtype: float64
```

**Q202.**

```python
print(df[df['year'] == 2007].groupby('continent')['population'].sum())
```

Output:

```text
continent
Africa       929539692
Americas     898871184
Asia        3811953827
Europe       586098529
Oceania       24549947
Name: population, dtype: int64
```

**Q203.**

```python
d07 = df[df['year'] == 2007]
print(d07.sort_values('gdp_cap', ascending=False)[['country', 'gdp_cap']].head(5))
```

Output:

```text
            country      gdp_cap
1151         Norway  49357.19017
863          Kuwait  47306.98978
1367      Singapore  47143.17964
1619  United States  42951.65309
755         Ireland  40675.99635
```

**Q204.**

```python
d07 = df[df['year'] == 2007]
print(d07.sort_values('life_exp')[['country', 'life_exp']].head(5))
```

Output:

```text
           country  life_exp
1463     Swaziland    39.613
1043    Mozambique    42.082
1691        Zambia    42.384
1355  Sierra Leone    42.568
887        Lesotho    42.592
```

**Q205.**

```python
d = df.copy()
d['gdp_total'] = d['gdp_cap'] * d['population']
d07 = d[d['year'] == 2007]
print(d07.sort_values('gdp_total', ascending=False)[['country', 'gdp_total']].head(3))
```

Output:

```text
            country     gdp_total
1619  United States  1.293446e+13
299           China  6.539501e+12
803           Japan  4.035135e+12
```

**Q206.**

```python
d = df.copy()
d['rich'] = np.where(d['gdp_cap'] > 10000, 'Yes', 'No')
print(d['rich'].value_counts())
```

Output:

```text
rich
No     1312
Yes     392
Name: count, dtype: int64
```

**Q207.**

```python
print(df.groupby('continent')['country'].nunique())
```

Output:

```text
continent
Africa      52
Americas    25
Asia        33
Europe      30
Oceania      2
Name: country, dtype: int64
```

**Q208.**

```python
print(df.groupby('year')['life_exp'].mean().head(3))
```

Output:

```text
year
1952    49.057620
1957    51.507401
1962    53.609249
Name: life_exp, dtype: float64
```

**Q209.**

```python
print(df.groupby('continent')['life_exp'].agg(['min', 'mean', 'max']).round(2))
```

Output:

```text
             min   mean    max
continent                     
Africa     23.60  48.87  76.44
Americas   37.58  64.66  80.65
Asia       28.80  60.06  82.60
Europe     43.58  71.90  81.76
Oceania    69.12  74.33  81.24
```

**Q210.**

```python
d = df[(df['year'] == 2007) & (df['life_exp'] > 80)]
print(len(d))
print(d['country'].tolist())
```

Output:

```text
13
['Australia', 'Canada', 'France', 'Hong Kong, China', 'Iceland', 'Israel', 'Italy', 'Japan', 'New Zealand', 'Norway', 'Spain', 'Sweden', 'Switzerland']
```

**Q211.**

```python
print(df.iloc[100])
print(df.loc[100])
```

Output:

```text
country       Bangladesh
year                1972
population      70759295
continent           Asia
life_exp          45.252
gdp_cap       630.233627
Name: 100, dtype: object
country       Bangladesh
year                1972
population      70759295
continent           Asia
life_exp          45.252
gdp_cap       630.233627
Name: 100, dtype: object
```

**Q212.**

```python
print(df[df['country'].str.startswith('New')]['country'].unique())
```

Output:

```text
<ArrowStringArray>
['New Zealand']
Length: 1, dtype: str
```

**Q213.**

```python
print(df[df['country'].str.contains('Republic')]['country'].unique())
```

Output:

```text
<ArrowStringArray>
['Central African Republic', 'Czech Republic', 'Dominican Republic', 'Slovak Republic']
Length: 4, dtype: str
```

**Q214.**

```python
print(df[(df['country'].isin(['India', 'China', 'Japan'])) & (df['year'] == 2007)])
```

Output:

```text
    country  year  population continent  life_exp       gdp_cap
299   China  2007  1318683096      Asia    72.961   4959.114854
707   India  2007  1110396331      Asia    64.698   2452.210407
803   Japan  2007   127467972      Asia    82.603  31656.068060
```

**Q215.**

```python
i = df[df['country'] == 'India'].set_index('year')['life_exp']
print(round(i[2007] - i[1952], 3))
```

Output:

```text
27.325
```

**Q216.**

```python
print(df[df['year'] == 2007].groupby('continent')['gdp_cap'].median().sort_values(ascending=False))
```

Output:

```text
continent
Oceania     29810.188275
Europe      28054.065790
Americas     8948.102923
Asia         4471.061906
Africa       1452.267078
Name: gdp_cap, dtype: float64
```

**Q217.**

```python
d = df[df['year'] == 2007].copy()
d['pop_share'] = (d['population'] / d['population'].sum() * 100).round(2)
print(d.sort_values('pop_share', ascending=False)[['country', 'pop_share']].head(3))
```

Output:

```text
            country  pop_share
299           China      21.10
707           India      17.76
1619  United States       4.82
```

**Q218.**

```python
d = df.copy()
d['diff'] = d['life_exp'] - d.groupby(['continent', 'year'])['life_exp'].transform('mean')
print(d['diff'].round(2).head(3))
```

Output:

```text
0   -17.51
1   -18.99
2   -19.57
Name: diff, dtype: float64
```

**Q219.**

```python
print(round(df['gdp_cap'].corr(df['life_exp']), 3))
```

Output:

```text
0.584
```

**Q220.**

```python
m = movies.drop('Unnamed: 0', axis=1)
d = directors.drop('Unnamed: 0', axis=1)
print(m.shape)
print(d.shape)
```

Output:

```text
(1465, 11)
(2349, 3)
```

**Q221.**

```python
data = movies.merge(directors, how='inner', left_on='director_id', right_on='id')
print(data.shape)
```

Output:

```text
(1465, 16)
```

**Q222.**

```python
data = movies.merge(directors, how='inner', left_on='director_id', right_on='id')
data = data.drop(['Unnamed: 0_x', 'Unnamed: 0_y', 'id_y'], axis=1).rename({'id_x': 'movie_id'}, axis=1)
print(data.columns.tolist())
```

Output:

```text
['movie_id', 'budget', 'popularity', 'revenue', 'title', 'vote_average', 'vote_count', 'director_id', 'year', 'month', 'day', 'director_name', 'gender']
```

**Q223.**

```python
print(movies.sort_values('revenue', ascending=False)[['title', 'revenue']].head(5))
```

Output:

```text
                                       title     revenue
0                                     Avatar  2787965087
19                                   Titanic  1845034188
30                                 Furious 7  1506249360
36            Transformers: Dark of the Moon  1123746996
199  The Lord of the Rings: The Return of...  1118888979
```

**Q224.**

```python
print(movies.sort_values('budget', ascending=False)[['title', 'budget']].head(5))
```

Output:

```text
                                      title     budget
12  Pirates of the Caribbean: On Strange...  380000000
1   Pirates of the Caribbean: At World's...  300000000
6                          Superman Returns  270000000
4                              Spider-Man 3  258000000
9                           The Lone Ranger  255000000
```

**Q225.**

```python
m = movies.copy()
m['profit'] = m['revenue'] - m['budget']
print(m.sort_values('profit', ascending=False)[['title', 'profit']].head(5))
```

Output:

```text
                                       title      profit
0                                     Avatar  2550965087
19                                   Titanic  1645034188
30                                 Furious 7  1316249360
199  The Lord of the Rings: The Return of...  1024888979
36            Transformers: Dark of the Moon   928746996
```

**Q226.**

```python
vc = movies['year'].value_counts().sort_index()
print(vc.loc[2010:2015])
```

Output:

```text
year
2010    63
2011    67
2012    49
2013    57
2014    53
2015    41
Name: count, dtype: int64
```

**Q227.**

```python
print(movies['month'].value_counts())
```

Output:

```text
month
Dec    193
Sep    166
Oct    149
Jun    133
Jul    127
Nov    117
May    116
Aug    111
Feb    104
Mar     99
Apr     90
Jan     60
Name: count, dtype: int64
```

**Q228.**

```python
d = movies[(movies['year'] == 2015) & (movies['vote_average'] > 7.5)]
print(d[['title', 'vote_average']])
```

Output:

```text
                      title  vote_average
162             The Martian           7.6
394       The Hateful Eight           7.6
833  Straight Outta Compton           7.7
```

**Q229.**

```python
d = movies[movies['title'].str.contains('War')]
print(len(d))
print(d['title'].tolist())
```

Output:

```text
15
['World War Z', 'The Chronicles of Narnia: The Lion, the Witch and the Wardrobe', 'War of the Worlds', 'The 13th Warrior', 'The Flowers of War', "Charlie Wilson's War", 'War Horse', 'This Means War', 'Lord of War', 'Bride Wars', 'Warrior', '5 Days of War', 'Warlock', 'A Nightmare on Elm Street 3: Dream Warriors', 'Mad Max 2: The Road Warrior']
```

**Q230.**

```python
print(movies.groupby('year')['revenue'].sum().sort_values(ascending=False).head(5))
```

Output:

```text
year
2009    11447602057
2011    10558632684
2014    10548142007
2008    10394045331
2012    10197473358
Name: revenue, dtype: int64
```

**Q231.**

```python
print(movies.groupby('year')['budget'].mean().round(0).tail(5))
```

Output:

```text
year
2012    62612245.0
2013    65346491.0
2014    60837736.0
2015    64548781.0
2016    80846154.0
Name: budget, dtype: float64
```

**Q232.**

```python
data = movies.merge(directors, left_on='director_id', right_on='id')
print(data['director_name'].value_counts().head(5))
```

Output:

```text
director_name
Steven Spielberg    26
Martin Scorsese     19
Clint Eastwood      19
Woody Allen         18
Ridley Scott        16
Name: count, dtype: int64
```

**Q233.**

```python
data = movies.merge(directors, left_on='director_id', right_on='id')
print(round(data[data['director_name'] == 'Christopher Nolan']['vote_average'].mean(), 2))
```

Output:

```text
7.8
```

**Q234.**

```python
data = movies.merge(directors, left_on='director_id', right_on='id')
print(data.groupby('director_name')['revenue'].sum().sort_values(ascending=False).head(5))
```

Output:

```text
director_name
Steven Spielberg     8676739164
Peter Jackson        6498642820
James Cameron        5883569439
Michael Bay          5832524638
Christopher Nolan    4227483234
Name: revenue, dtype: int64
```

**Q235.**

```python
data = movies.merge(directors, left_on='director_id', right_on='id')
print(data['gender'].value_counts(dropna=False))
```

Output:

```text
gender
Male      1309
NaN        124
Female      32
Name: count, dtype: int64
```

**Q236.**

```python
data = movies.merge(directors, left_on='director_id', right_on='id')
print(data.groupby('gender')['revenue'].mean().round(0))
```

Output:

```text
gender
Female    138498167.0
Male      148016014.0
Name: revenue, dtype: float64
```

**Q237.**

```python
print((~directors['id'].isin(movies['director_id'])).sum())
```

Output:

```text
2150
```

**Q238.**

```python
d = directors.merge(movies, how='left', left_on='id', right_on='director_id')
print(d.shape)
```

Output:

```text
(3615, 16)
```

**Q239.**

```python
print(movies.groupby(['year', 'month']).size().sort_values(ascending=False).head(5))
```

Output:

```text
year  month
2005  Sep      17
2006  Sep      13
2011  Sep      13
2000  Dec      12
2002  Dec      12
dtype: int64
```

**Q240.**

```python
d = movies[movies['vote_count'] >= 5000]
print(d.loc[d['vote_average'].idxmax(), ['title', 'vote_average', 'vote_count']])
```

Output:

```text
title           Fight Club
vote_average           8.3
vote_count            9413
Name: 383, dtype: object
```

**Q241.**

```python
m = movies.copy()
m['decade'] = (m['year'] // 10) * 10
print(m['decade'].value_counts().sort_index())
```

Output:

```text
decade
1970     18
1980    116
1990    335
2000    640
2010    356
Name: count, dtype: int64
```

**Q242.**

```python
m = movies.copy()
m['rev_vs_year_avg'] = m['revenue'] - m.groupby('year')['revenue'].transform('mean')
print(m['rev_vs_year_avg'].round(0).head(3))
```

Output:

```text
0    2.614517e+09
1    8.022839e+08
2    6.841736e+08
Name: rev_vs_year_avg, dtype: float64
```

**Q243.**

```python
d = pd.concat([movies.head(3), movies.tail(3)])
print(d['title'].tolist())
```

Output:

```text
['Avatar', "Pirates of the Caribbean: At World's End", 'Spectre', 'Rampage', 'Slacker', 'El Mariachi']
```

**Q244.**

```python
m = movies.set_index('title')
print(m.loc['Avatar', 'revenue'])
```

Output:

```text
2787965087
```

**Q245.**

```python
s = pd.DataFrame({'name': ['A', 'B', 'C'], 'marks': [80, 65, 90]})
print(s.loc[s['marks'].idxmax(), 'name'])
```

Output:

```text
C
```

**Q246.**

```python
s = pd.DataFrame({'dept': ['HR', 'IT', 'HR', 'IT', 'IT'], 'salary': [40, 60, 50, 80, 70]})
print(s.groupby('dept')['salary'].mean())
```

Output:

```text
dept
HR    45.0
IT    70.0
Name: salary, dtype: float64
```

**Q247.**

```python
m = movies.copy()
m['short_title'] = m['title'].apply(lambda t: t[:10])
print(m['short_title'].head(3).tolist())
```

Output:

```text
['Avatar', 'Pirates of', 'Spectre']
```

**Q248.**

```python
n = (movies['budget'] == 0).sum()
print(n)
print(round(n / len(movies) * 100, 2))
```

Output:

```text
136
9.28
```

**Q249.**

```python
wk = movies['day'].isin(['Saturday', 'Sunday'])
print(round(movies[wk]['revenue'].mean()))
print(round(movies[~wk]['revenue'].mean()))
```

Output:

```text
127793655
144301886
```

**Q250.**

```python
d = movies[(movies['year'] == 2009) & (movies['revenue'] > 500_000_000)]
print(d.sort_values('revenue', ascending=False)[['title', 'revenue']])
```

Output:

```text
                                   title     revenue
0                                 Avatar  2787965087
25   Transformers: Revenge of the Fallen   836297228
40                                  2012   769653595
500          The Twilight Saga: New Moon   709827462
215                      Sherlock Holmes   524028679
```

