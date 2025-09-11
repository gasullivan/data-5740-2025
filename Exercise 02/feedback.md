## Score: 20/20

### Section 1: Using SQL and Python in Snowflake

All good

### Section 2: Maniuplating Dataframes

* You used a design pattern where you created your manipulation function and then applied it the data frame. That obviously works great, but I want to share another, more natural pattern in Pandas:

```python
df.loc[df["STORE_ID"] % 2 == 0], "EMAIL"] = "joe.person@wustl.edu"
```

This is preferred because the `.apply()` operator in Pandas is not vectorized whereas `.loc()` is. Here's an article that describes this in more detail. https://towardsdatascience.com/speed-up-pandas-code-with-numpy-fdee76210794/

### Section 3: Visualizations

These are good visualizations. Feel free to branch out and try using Streamlit's built-in visualization libraries and Seaborn, too.

### Section 4: Analysis

Nice work drilling into the ANOVA and other statistical tests, too.  As we'll see later, however, some of these tests may not have been appropriate for this data set. When you go back and look at the distribution of revenue values, you'll notice that it isn't very normally distributed. There's a notable right-skew to the data.

It's interesting that my visual observation would tell me that Store 2 v Store 1 distributions do look different. For instance, they rent close to the same number of NC-17 movides, but there's a larger difference with G. At least based on my eye.  Your statistical test, though, tells us this isn't statistically significant (p<0.05)

### Section 5: Analysis

Nice analysis here.
