# pandas-challenge-1
AI Bootcamp challenge on Pandas 

# Pandas
Pandas is Python Data Analysis Library and is powerful tool to read, analyze and manage your data. 

# What is in this project?
This project is to use and showcase basic Pandas skills like data analysis and manipulation. A dataset of clients and their orders has been provided to perform this tasks.

[Here](https://pandas.pydata.org/docs/reference/frame.html) is the complete documentation of Dataframe from pandas. But below are some of the built-in fucntions/properties/methods used in this challenge.

### Data Analysis
First step is to understand about data provided. 

```
.shape - provides the structure of dataframe with rows and columns size.
.columns - lists out the columns in dataframe
.dtypes - list out data types of each column
.describe() - provides the basic stats of all the numerics columns in dataframe like count, max, min, std, mean.....
.isnull() - check if any of the column value is null
.duplicated() - displays rows which are same
.drop_duplicates() - delete rows which are duplicate
.value_counts() - get count of values by columns
```

### Manipulation
Next add some new columns based on calculation using other existing columns so that you can get more stats about your data.
Data manipulation/addition is done using built-in (like sum()) and also custom functions.

```
.apply() - method to apply changes/modifications of data across rows/columns

#snippet of custom function to calculate shipping price:
def get_shipping_price(row):
    total_weight = (row['unit_weight'] * row['qty'])
    
    if total_weight <= 50:
        return round((total_weight * 10),2)
    return round((total_weight * 7),2)
```

### Summarize
Created a summary of top 5 clients in the provided data, which included the revenue and profits from top clients. 
