# Score 20/20

Great work starting out your notebook with some basic data exploration.

I like how you use comments in your code. It really shows the thought process and helps me see where your head is at.

When doing a "log" transformation for statistics, consider using the `np.log1p()` function. When you have values that may be close to 0, it help address that by adding 1 to the number. Not relevant in this scenario, but I thought I'd mention it.

I recommend breaking up the amount of code in each cell a little bit more. You end up with lots of code to run all at once rather than iterating in smaller bits.

**Regarding your question about your alpha being "off by a factor of 100".** - I think the answer lies in scaling of your predictors, X. You applied a `scaler.fit_transform()` to scale some of those input variables. As a result, the penalty coefficient is going to be scaled, too.  You've got variables like "income" that are much larger than the scaled values centered around 0.
