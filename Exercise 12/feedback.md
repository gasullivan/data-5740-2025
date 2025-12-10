# Final Score 20/20

I like the way you built out the custom histograms showing the mean as a vertical line. Helpful for seeing skew. It probably would have been a good idea to go ahead and create a custom_hist function something like this...

```python
def custom_hist(axis, field, label, color='black', bins=30):
    axis.hist(df_pcard[field], bins=30, color=color, edgecolor='black')
    axis.axvline(df_pcard[field].mean(), color='red', linestyle='--', label='Mean')
    axis.set_xlabel(label)
    axis.set_ylabel('Frequency')
    axis.set_title('Distribution of ' + label)
    axis.legend()

fig, axes = plt.subplots(1, 3, figsize=(15, 4))

custom_hist(axes[0], 'avg_transaction_amount', 'Average Transaction Amount', 'steelblue')

custom_hist(axes[1], 'transactions_per_month', 'Transactions per Month', 'coral')

custom_hist(axes[2], 'pct_weekend_transactions', 'Percent Weekend Transactions', 'mediumseagreen')

```


Great K-Distance Plot with the percentiles on it. Very helpful.

Down at the 2D scatterplots, same note as above about creating a function to simplify the maintenance of your code.


Great sumary at the end. Nice way to wrap it up.

On this notebook, I felt like your comments and organization were a little bit sparse. Rather, it felt like a brief intro, a bunch of code, and a summary at the end. You've got comments regularly throughout, but I think it's helpful to have a little more commentary and explanation of your thought process throughout.
